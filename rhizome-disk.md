## [[2025-12-05]]
- Special session of the [[Social Coop Tech Group]] for adding disk space to [[rhizome]] and other disk related server maintenance.

## Finding
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
- We could try to rebuild the array with a new drive in a new maintenance window (or get a new server and move services there
