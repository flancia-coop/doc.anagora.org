## [[2025-12-05]]
- Special session of the [[Social Coop Tech Group]] for adding disk space to [[rhizome]] and other disk related server maintenance.
- Check ins!
    - Sun is out in CR! Happy to have reached the weekend
    - +1 on weekend!
    - Looking to catch up with rest
        - ... and a crampon enabled run!
    - RAID activities emotional support

## Findings
- We are running on one disk, RAID is degraded!

```
flancian@rhizome:~$ cat /proc/mdstat 
Personalities : [raid1] [linear] [multipath] [raid0] [raid6] [raid5] [raid4] [raid10] 
md1 : active raid1 nvme0n1p2[0]
      1046528 blocks super 1.2 [2/1] [U_]
      
md2 : active raid1 nvme0n1p3[0]
      465370432 blocks super 1.2 [2/1] [U_]
      bitmap: 4/4 pages [16KB], 65536KB chunk

md0 : active raid1 nvme0n1p1[0]
      33520640 blocks super 1.2 [2/1] [U_]
      
unused devices: <none>
flancian@rhizome:~$ lsblk
NAME        MAJ:MIN RM   SIZE RO TYPE  MOUNTPOINTS
nvme0n1     259:0    0 476.9G  0 disk  
├─nvme0n1p1 259:1    0    32G  0 part  
│ └─md0       9:0    0    32G  0 raid1 [SWAP]
├─nvme0n1p2 259:2    0     1G  0 part  
│ └─md1       9:1    0  1022M  0 raid1 /boot
└─nvme0n1p3 259:3    0 443.9G  0 part  
  └─md2       9:2    0 443.8G  0 raid1 /
```

- This makes us more vulnerable to data loss in the form of losing live postgres, so good thing we're copying that data to a new array with this maintenance window!
- We should try to rebuild the array with a new drive in a new maintenance window.

## Creating new disk array
- I plan to shut down the server at 16:59:30 UTC as Hetzner wanted it down before 17:00 UTC.
    - Done!
- Then wait for it to come back 
    - Done!
- And create a 1TB RAID 1 mirror.
    - fdisk for creating two Linux RAID partitions
    - mdadm for creating the mirror proper
    - then mkfs.ext4
    - See generated instructions below.


```
flancian@rhizome:~$ lsblk                                                                                 
NAME        MAJ:MIN RM   SIZE RO TYPE  MOUNTPOINTS                                                        
nvme0n1     259:0    0 476.9G  0 disk                                                                     
├─nvme0n1p1 259:1    0    32G  0 part                                                                     
│ └─md0       9:0    0    32G  0 raid1 [SWAP]                                                             
├─nvme0n1p2 259:2    0     1G  0 part                                                                     
│ └─md1       9:1    0  1022M  0 raid1 /boot                                                              
└─nvme0n1p3 259:3    0 443.9G  0 part                                                                     
  └─md2       9:2    0 443.8G  0 raid1 /                                                                  
nvme1n1     259:4    0 476.9G  0 disk                                                                     
├─nvme1n1p1 259:5    0    32G  0 part                                                                     
├─nvme1n1p2 259:6    0     1G  0 part                                                                     
└─nvme1n1p3 259:7    0 443.9G  0 part                                                                     
nvme3n1     259:8    0 953.9G  0 disk                                                                     
nvme2n1     259:9    0 953.9G  0 disk        
```

## Fixing the old disk array
- Discuss?
- This would involve identifying the missing disk and asking Hetzner to replace it, then doing a live rebuild.
- The alternative (or complement) is to get a second server (with more disk out of the box) and migrate to it, getting newer hardware in the process; and it might not turn out more expensive when compared against the current one + two extra drives.
- Or the clever/fancy option, which would be:
    - Add one of the 1TB disks to the 500GB array, repair the array
    - Add the other 1TB disk as spare.
    - *Remove* the working 500GB disk.
    - Grow the array to 1TB.
    - Resize the filesystem.

## Detailed instructions
- I asked Gemini about best practices for RAID setup on Debian in 2025 and it's the same as 15y ago: partition the disks then create the array with mdadm then sync source of truth.

```
lsblk

sudo fdisk /dev/nvme2n1

sudo fdisk /dev/nvme3n1

sudo mdadm --create /dev/md3 --level=1 --raid-devices=2 /dev/nvme2n1p1 /dev/nvme3n1p1

sudo mkfs.ext4 /dev/md3

sudo mdadm --detail --scan | grep "md3" | sudo tee -a /etc/mdadm/mdadm.conf

sudo update-initramfs -u

sudo blkid /dev/md3

in fstab: UUID=YOUR-UUID-HERE    /mnt/new_storage    ext4    defaults 0    2

sudo mount -a
```

## Remaining tasks

1. Bring down containers
2. Run rsync again
3. `umount /opt/social.coop-temporary`
4. Rename `/opt/social.coop` (to `/opt/social.coop_old_2025-12-05`)
5. Rename `/opt/social.coop-temporary` to `/opt/social.coop`
6. Edit `fstab`
7. `mount -a`
8. Reboot
9. Pray
10. ???
11. Done
12. (Lol or rebuild the RAID array)