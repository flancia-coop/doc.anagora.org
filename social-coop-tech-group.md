## 2025-12-02
- [[Gabriel Garrido]] [[Calix]] [[Flancian]]
- Check ins
    - [[Dec]] to [[May]] is [[Summer]]
    - First winter in Switzerland


## 2025-11-12
- [[Dphiffer]] [[Flancian]] [[Steve]] [[Gabriel]]
- Round the table!
    - Welcome Steve!
        - Frontend engineer, interested in participating
    - Gabriel
        - In Costa Rica, interested in many things (including permaculture)
    - Dan
        - Full stack engineer, in upstate NY
    - Eduardo
        - Sysadmin type with interest in coding from Argentina :)
- Agenda setting
    - Documentation
        - How things should be (tm)
            - wiki.social.coop is the source of truth for ~all our documentation needs
            - https://wiki.social.coop/wiki/Tech_Working_Group should be the entry point to everything TWG
    - Onboarding process + stack at a high level
        - Overview of process
        - [[Ansible vault]] vs pass
            - Dan: they are similar
            - Unsure of pros/cons of either, but Dan trusts pass more and Flancian likes pass well enough
            - Could it make sense to consolidate on ansible vault?
                - Will track as a git ticket
        - Walkthrough of rhizome
            - Bare metal in Hetzner
        - Walkthrough of hypha
            - VPS in Hetzner
        - Walkthrough of pando
            - VPS in iocoop.org
        - Other services we depend on
            - Digital ocean for S3 buckets/backups
            - Cloudflare for DNS
            - Webarchitects for email forwarding
    - Possible starter tasks
        - Monitoring++?
        - Something else in git issues?
        - Whatever strikes your fancy :)
        - Schedule backup restore tests
        - Consider replication for S3 data overall?
            - Gabriel: backblaze has replicated buckets and it works pretty well
    - Andrew's asks
        - Budget related
            - Discretionary budget
            - Hosting budget
            - Stipends
        - Community contributions (to projects etc.)
            - Feel free to keep bringing up ideas in the chat
        - -> Let's answer in the form of a...
            - spreadsheet! https://share.mayfirst.org/apps/files/files/41330606?dir=/&openfile=true
    - Mastodon 4.5
        - -> next time
- Check outs
    - Thank you!

## 2025-10-29

- [[Calix]] [[Gabriel]] [[Dan]] [[Flancian]] (joined late)
- (we do some intros)
- Intro to TWG:
    - D: "middle amount of sophistication"
    - D: Policy risk: delta between code of conduct and Hetzner policy w.r.t. sexually explicit content, were exploring US VPS host.
    - D: Flancian set up a bunch of our stuff, often our representative to Organi(z/s)ing Circle
    - G: What sort of tasks is the working group responsible for?
    - C: Keep the Mastodon server running, upgrading the software, putting out fires occasionally. We have the wiki, used more and more. There's a SSO system associated with that. Goal for 2025: migrating Mastodon to use the SSO system.
    - D: Firefighting within Mastodon - performance issues with someone Going Viral™. Pretty rare! Updates - somewhat lax if there isn't a pressing security update to apply. Big update (minor release) with quote posts.
    - G: Would be happy to assist on both fronts. What are the expectations for TWG members? Processes? Commitment expected? Process of transition into working group?
    - D: Don't think there's any structure to that. Often when there's a problem we gather around the chat, figure out a solution there. Onboarding has a set of steps - granting access. Authorization from social.coop membership.
    - C: Also non-technical parts: meeting organizing, defining processes. We meet every 2 weeks, ideally (for security, and to know who is around) "active" participants would be coming to (or async catching up with) those meetings regularly. No on-call rota.
    - G: Experience hosting servers for clients, would be interested to help. Interested to shadow.
- We do a co-operative multiplayer update to 4.4.8, it goes Fine
- F: Next time we could do an interactive walkthrough of the repos we have, servers involved
    - C: We could give read-only access to git repos to make onboarding easier.
        - +1
- (a conversation about cloudflare, Andrew's calendar script)
    - C: If we're not using Cloudflare let's not start, fascism
    - F: We're using it for DNS.
    - C: So let's optimistically merge, find an alternative medium-term
        - +1
    - G: I've used bunny.net as an alternative to cloudflare 
    - Requisites for git access
        - Get an account in git.coop
        - Which requires a social.coop
- G: Using Ubuntu 22, upgrade?
    - D, C: Quite smooth
    - C: Supported til April 2027.
- Check outs!
    - How we're feeling/what we're doing next/what to improve (all optional)
    - Calix: feeling good, stressed about laptop situation but will decompress next. Hyped to be growing the TWG!
        - Maybe in a future instance we could have a dedicated/explicit facilitator role.
    - Flan: Glad to be here! No more summits this year ⛰️⛔. Looking forward to taking impetus of new members to review our processes, fresh ideas on how to improve, finish some things that have been on my plate.
    - Gabriel: Feeling good, excited to get more involved. Future: lentils, site launch / migration. Hurricane rain. 

## 2025-09-23
- [[Dan]] [[Andrew]] [[Calix]] [[Flan]]
- Email deliverability
    - https://git.coop/social.coop/tech/operations/-/issues/91
    - Our deliverability rates are fine, so we may not need to do anything
    - Dan looking at Cloudflare DNS, looks okay
    - Andrew to strengthen our DMARC, with assistance from TWG
    - Mailgun may be in a grandfathered plan
        - Andrew will take up talking to the finance working group about bumping our plan
- [[Andrew]] Moving bot to git.coop repo and shared cloudflare account
    - Would like to encourage the TWG to take a look
    - Dan: was curious about running on a different worker platform -- can it be run out of Cloudflare?
    - Andrew: no, just meant that it's running on my personal Cloudflare account; we could move this to the shared account and the shared repo.
    - Dan: happy to take on the migration but feel free to go ahead.
    - Andrew: happy to take this on. Also to make changes to make it more secure (like remove the frontend aspect of it, which was meant for testing.)
    - Dan: a feature flag for disabling/enabling the frontend/debugging feature would be a good idea.
- Dan: have a related RSS to ActivityPub project that has been stalled; the idea was to cross-post from Loomio to the Fediverse.
    - Andrew: interested / happy to take a stab at it!
- Upgrade next up!
    - https://git.coop/social.coop/tech/ansible/-/merge_requests/60/diffs by Dan
- Turns out that Datadog daemon does *not* restart after we reboot rhizome
    - file a bug? Done.
- Also some weirdness about /tmp being necessary for our backup process, potentially
    - Calix filed a bug
- Check ins
    - Dan has been having great success union-organizing!
    - Calix is enjoying getting back into Ruby, having fun! Went to a digital security training and found it interesting -- [[no tech for apartheid]].
        - [[H1B]] situation is stressful.
        - It seems it only applies to new applications though?

## 2025-09-09
- [[Dan]] [[Calix]] [[Flancian]]
- Long time no see!
    - We did do one upgrade in the intervening time
- Checkins
    - On work outages
    - On youtube-nocookie
    - On work visas in the US
- Topics
    - Upgrade Mastodon (Dan will make a Merge Request™)
        - Success!
        - After temporary failure with the systemd service failing after update (why?)
        - On retrying, we saw docker pulls taking place -- so clearly something hadn't run fully/properly.
    - Update Rhizome
        - It had security updates queued up
        - We ran into a scary GRUB warning but seemingly it was because of Hetzner not doing GRUB the modern way. https://www.sindastra.de/p/2694/hetzner-grub-efi-amd64-signed-update
    - Open house participation
        - Calix and Eduardo missed it
        - But Dan made it! \o/
        - And Dan will be hosting the next one! \o/
    - New LTS release for Hypha and overall maintenance
        - We rebooted today after 3y (!)
        - Next up: apt-get update/upgrade?
            - Done.
        - We're on 'jammy'
        - We still have support for >1y.
        - Next up: dist-upgrade some day?
    - Review other MRs
        - alpha.social.coop refresh: Flancian will try to take action on the open comments by next time we meet :)
    - Discuss Andrew's calendar change
        - Invite Andrew next time? And discuss further.
    
What's On Hypha

```
➜ abra app ls -s hypha.social.coop
┏━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━┓
┃  RECIPE   ┃         DOMAIN         ┃      SERVER       ┃
┣━━━━━━━━━━━╋━━━━━━━━━━━━━━━━━━━━━━━━╋━━━━━━━━━━━━━━━━━━━┫
┃ bonfire   ┃ bonfire.social.coop    ┃ hypha.social.coop ┃
┃ keycloak  ┃ auth.social.coop       ┃ hypha.social.coop ┃
┃ mediawiki ┃ wiki-alpha.social.coop ┃ hypha.social.coop ┃
┃ mediawiki ┃ wiki.social.coop       ┃ hypha.social.coop ┃
┃ traefik   ┃ traefik.social.coop    ┃ hypha.social.coop ┃
┗━━━━━━━━━━━┻━━━━━━━━━━━━━━━━━━━━━━━━┻━━━━━━━━━━━━━━━━━━━┛
```

Some pending updates on Rhizome:

```
3wordchant@rhizome:~$ sudo apt upgrade
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Calculating upgrade... Done
The following packages were automatically installed and are no longer required:
  docker-scan-plugin libio-pty-perl libipc-run-perl libltdl7 postgresql-client-15
Use 'sudo apt autoremove' to remove them.
The following packages will be upgraded:
  apt apt-utils containerd.io cryptsetup cryptsetup-bin cryptsetup-initramfs distro-info-data dmeventd dmidecode dmsetup
  docker-buildx-plugin docker-ce docker-ce-cli docker-ce-rootless-extras docker-compose-plugin ethtool
  gir1.2-packagekitglib-1.0 grub-efi-amd64 grub-efi-amd64-bin initramfs-tools initramfs-tools-bin initramfs-tools-core
  landscape-common libapt-pkg6.0 libcryptsetup12 libdevmapper-event1.02.1 libdevmapper1.02.1 libglib2.0-0 libglib2.0-bin
  libglib2.0-data libldap-2.5-0 libldap-common liblvm2cmd2.03 libmbim-glib4 libmbim-proxy libopeniscsiusr
  libpackagekit-glib2-18 libpq5 libseccomp2 linux-base lvm2 nginx open-iscsi packagekit pci.ids pollinate postgresql-client
  postgresql-client-15 postgresql-client-17 postgresql-client-common powermgmt-base python3-paramiko python3-update-manager
  sosreport ubuntu-advantage-tools ubuntu-pro-client ubuntu-pro-client-l10n update-manager-core xfsprogs
59 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
Need to get 0 B/121 MB of archives.
After this operation, 9,671 kB disk space will be freed.
Do you want to continue? [Y/n] 
```

## 2025-06-17
- [[Dan]], ..., [[Flancian]]
- [[Mastodon]] updates
    - Software
        - We're at current for the 4.3 branch: 4.3.8 ✅
    - Terms of service
        - Opt-in for instances: https://mastodon.social/@Gargron/114699805737874224
        - Complaint about IP termination clause: https://social.coop/@mcc@mastodon.social/114699202226271605
        - Git history: https://github.com/mastodon/mastodon/blob/main/config/templates/terms-of-service.md 
        - (New from Dec 2024)
        - There's an OC meeting this Thu, let's let them know?
- Merge requests/project updates
    - https://git.coop/social.coop/tech/ansible/-/merge_requests/41 for alpha.social.coop
        - Thanks for the review and comments!
        - Will take action as in the threads and then give it a shot (tm) on pando.
        - Might want to decouple secrets fully before we call alpha 'stable'.
    - https://git.coop/social.coop/tech/ansible/-/merge_requests/42 for rss
        - This needs to be dockerized
    - https://git.coop/social.coop/tech/join.social.coop/-/merge_requests/11 for Gitlab error reporting
        - Looks good, approved/merged!
    - https://git.coop/social.coop/tech/join.social.coop/-/merge_requests/10 upgrade node.js
        - needs freshening up? or not?
        - not high urgency
        - Dan will update it to use node.js v22

## 2025-03-10
[[Andrew]], [[Calix]], [[Dan]], [[Flancian]].
- Check ins
    - Flan: travel was great! Now in post-travel haze
    - Calix: good, will travel soon again to conclude the visa saga
    - Andrew: good, doing well -- in Toronto, CA. Interesting couple of weeks -- navigating "all this" (world's chaos).
    - Dan: OMINOUS SILENCE (because of the Bluetooth gods). Fine despite a cold; have a hard stop at :30. Will be in NYC tomorrow!
        - Calix: will DM.
- Cloudflare delegation
    - DMARC reporting/monitoring
    - Let's try to do this now?
        - Done!
        - In DNS settings, you can invite members in the burger menu
    - follow-up request after TWG meeting:
        - Admin. domain-scoped role is not enough; need Admin. account-scoped role
- domain: move to Domains.coop in 2026
    - cost is beneficial
    - also the support you can give to another coop
    - at which point should we write down a policy to try to support coops even if they come at some extra financial cost?
      - **we'll bring it up with the OC on Thursday**
- alpha.social.coop progress
    - or lack thereof
    - server live
    - ansible PR still pending
- maybe upgrade mastodon
    - No need as Dan did it last week! \o/
    - 4.3.5 is out but can wait, we'll adjourn early and likely do it next week

## 2025-02-10
[[Dan]], [[Edsu]], [[Flacian]].
- Check ins
    - F: AI
        - Flancian back on March 10 from travel
    - D: and thinking about encryption :)
        - (side projects :)
    - E: Washington, DC mood
    - C: mostly doing well
- alpha.social.coop progress
    - pando.social.coop exists!
        - https://git.coop/social.coop/tech/ansible/-/merge_requests/50 for the MR
        - Discussed how to bootstrap a new server, committed an update to README.md.
- maybe upgrade mastodon?
    - we did! 4.3.3
- and we succesfully re-encrypted pass!

## 2025-02-03
[[Dan]], [[Flacian]], [[Calix]]
https://git.coop/social.coop/tech/ansible/-/merge_requests/51
- (over at autonomic pad)
- next actions:
1. Write a draft summary of our conversations
2. With your joint approval, post it for others to read (Loomio?)
3. Read the wiki link above (!) and consider incorporating changes from our experiences
4. Make sure Calyx gets meeting info for our next CWG meeting. 

## 2025-01-20

[[Dan]], [[Flacian]], [[Calix]]

https://agriculturaljusticeproject.org/toolkit/resources/relations/soulfire-courageous-conversations/
https://srinathramakrihttps://seedsforchange.org.uk/downloads/conflictbooklet.pdf
shnan.wordpress.com/wp-content/uploads/2016/07/non-violent-communication-summary.pdf

### Timeline

- March 21, 2024: Meta announces that Threads ActivityPub integration is now available in the United States, Canada and Japan.

- Jan 8th 2025:

> dnlbrnds: Good day everybody — I think this has been discussed when Threads went live, but with the recent developments around Meta, do you think we shall reconsider de-federating it?

> 3wc: I have to say the previous decisions seemed like a textbook case of how decisionmaking processes are vulnerable to how the question is framed, and it would be great to try to correct that this time around
> it's clear to me that Threads should be defederated based on our existing policy, so I think the proposal should be framed as "Should we make an exception to our policy for Meta", which I think is the correct & fair allocation of "status quo" / "do nothing" voting

flancian suggests a vote would be needed for taking action and "I'd recommend interested people ideally get together to agree on the phasing and then start one"

dnlbrnds and 3wc discuss co-drafting a proposal

- Jan 9th, 2025:

> Flancian: Thanks for the context and sharing your view! FWIW Meta does have policies still and claims to enforce them, the question then seems to be whether the policies are good, mediocre or actively harmful (the "encouraging abuse" argument). Abuse to members of our instance has not materialized from threads.net yet AFAICT; I can review moderation reports to be sure if people think that would be an interesting data point.

> 3wc: [are you saying] that your interpretation is that if a server's policy only bans some hate speech (while explicitly allowing other types) then it does not "[lack] policies .. to deal with hate speech"?

> Flancian: [..] I was trying to say that Meta does seem to be defining hate speech and is apparently "just" choosing to exclude some classes of speech from this category, which is different than not caring about hate speech at all like e.g. nazi instances do.

> 3wc: I have read many Nazi instances' policies and a significant number are similar to Facebook's - some hate speech is disallowed, some is explicitly allowed
8HJYUNMMMMMrts a thread with the CWG
- Mastodon thread started by @FoolishOwl discusses Threads federation: https://social.coop/@foolishowl/113804616908267159

> 16:39 UTC foolishowl: It sounds like several of our moderators think it's best to have a vote on this, and I haven't seen any arguments against doing so. Unfortunately I'm bogged down at work, so I can't do a proper job drafting it at the moment, but I'll work on it when I can.

> 19:45 UTC Flancian: https://doc.anagora.org/against-meta, open to universal access, please review/edit :)

> 20:58 UTC Flancian: I will check back later tonight and run the vote by default, then we can go further in Loomio? I think it's a good opportunity for people to express their views on what is happening. I hope the community finds the time to participate widely.

> 21:25 UTC Flancian: PSA: https://www.loomio.com/d/u1OkUA6M/clarity-on-stance-with-regards-to-threads/30 is the vote. please vote at your earliest convenience, but also optionally take the time to consider what you would like to publish on such an occasion; I think history will likely look back on both corporations and the commons at this moment. We have six days as per our governance template.

> 22:00 UTC: flancian and 3wc have a 1:1 discussion about the vote

> 3wc: "as i said in DM, I will take you on good faith that that was your conscious intention. I will also observe that your choice of framing has made it more likely that the vote would reach your desired outcome and placed the burden on more-marginalised people to advocate for ourselves to maintain our existing defences - and encourage you to consider what subconscious bias might also have been a factor in this choice"

> 22:32 UTC 3wc: I have now proposed an alternative vote, "Grant an exemption to the social.coop federation abuse policy for threads.net" https://www.loomio.com/p/XsNQByhG/proposal-grant-an-exception-to-the-social-coop-federation-abuse-policy-for-threads-net
> 3wc: I apologise for the confusion caused by parallel votes. I hope we do not need to find out what happens if the results disagree with each other

- Jan 11th, 2025

> 12:44 UTC Flancian: 20% is also significant enough that, if it holds, we should probably discuss as a community how exactly we go through enacting the suspend to make sure people don't lose significant data (as per the message above; but that is only one particular implementation plan).

- January 14, 2025:

> Flancian: I've now called this out to the CWG and TWG so we can plan accordingly. the CWG is meeting on the 23rd and this is a topic of discussion (how to defederate if the vote holds). so people should not expect a suspend action before then, maybe before EOM. if anybody has any issues with this, please raise.

> 3wc:  85% of people who voted (in the second poll) have actively disagreed with making an exception to the policy based on scale. But you're pushing for an exception to the policy based on scale?
> if people want "how many 'follow' relationships exist between social.coop and the instance?" to be a factor in the implementation of the Federation abuse policy then let's get a proposal for it to be added?

> Flancian: "Pushing" is forceful language that does not represent what I feel.

> Flancian: Finally, can we acknowledge I voted to suspend and not to grant an exception to our policies and I'm acting under the working assumption the first vote will pass and the second will not? In which way do you think I am misreading, mishandling or worsening the situation 
3wc ~ they/them? Thank you for clarifying.

### Timeline highlights / overview

F: Feeling very invested in things going into the situation. Suggested vote on the 8th, saw people worrying. 9th read more reaction, started changing my mind from "limit" based on lack of practical impact, to "suspend" based on emotional impact. 10th felt like the issue escalated. My POV: asked to wait. Felt like people were not OK with that. Suggested foolishowl create a thread. Didn't see pushback against calling a vote. Started a vote 1.5 hours after sending draft. Felt like reaction that took place after was not as constructive as it could have been. Felt responsibility as CWG member to start the vote. Did not feel in a good position to manage the conflict. Assumptions about personal motivations. Led to feeling disappointed.

C: Felt disappointed as well when I saw the vote framed in this way. Felt that future at coop was uncertain. Suspicious about the shortness of the draft review. Felt unseen/heard.

- Clarifying questions
- About past proposals in this space and their issues
    - Multiple choice/non-bylaws one

### Next actions

- Discuss interactions with CWG

## 2024-01-13
- Here: [[Dan]] [[Flancian]] [[Edsu]] 
- Check ins
    - Dan
    - Ed
    - Flan
- Recap of recent coop news
    - Pros and cons of defederation
    - AIs for defederation
        - [ ] Back up relations that will go even as CSV
        - Hachyderm posted about their suspend and included some nice ruby queries to get better information about the relationships, maybe read/review
        - Related to follows and data (panacea) portability
- Topics of discussion
    - Data retention and archiving practices
    - https://cloud.digitalocean.com/spaces/social-coop-media?i=7e7429&path=backups%2Frhizome%2F
        - Our database seems to be doubling (!) ever year, is that... OK?
    - Maybe we should review what hachyderm.io or mastodon.social are doing database wise
        - Dan: maybe we could invite hachyderm to one of these meetings?
        - Definitely!
- https://doc.anagora.org/twg-2025
- https://anagora.org/go/twg/bugs 

## 2024-11-25

- Here: [[Dan]] [[Edsu]] [[Flancian]]
- Check ins
    - [[Dan]] moving jobs, excited; role is similar but maybe a bit more constrained/tighter scoped
    - [[Ed]] doing alright; coping with the changes that are upcoming
        - [[EDGI]] and related efforts for preserving government-provided datasets; thinking of helping out with such efforts
        - [[Dan]]: https://source.opennews.org/articles/data-rescue/
        - Some government sites are being exported to notion pages (!)
            - -> https://github.com/edgi-govdata-archiving/rule-scout
    - [[Eduardo]]: listening to Milei with Lex Fridman as of late (!)
- Priorities
    - Rebooting
        - Ed: https://docs.joinmastodon.org/admin/troubleshooting/index-corruption/ is a thing
            - -> doesn't affect us as per ldd --version (we're past 2.28)
        - Upgrade kernel first?
           - done, ran apt-get update && apt-get dist-upgrade first
        - Reboot done! 
    - Backups and restores
        - DB size
            - vacuum didn't succeed yet for lack of space
        - https://docs.joinmastodon.org/admin/tootctl/#statuses-remove
        - Trying this first with a very high threshold:
            - `sudo docker exec -it docker-web-1 tootctl statuses remove --days 2500`
    - alpha.social.coop
        - Next step here is still to choose a VPS size/configuration in iocoop.org
        - Maybe decouple from instance restore question in the following way
            - We could 'cook' a db restore that incorporates all tables but skips >90% of history, bringing down db size to something more manageable in a small instance?
     - Hosting costs 
         - Let the FWG cost what we're taking on (to budget for 2025)
         - And also try to move to a model in which we 1. have a good relationship with our hosting providers, which invoice us ideally on a known cadence and 2. have reduced risk of service disruption.
         - Dan: spreadsheet with different hosting costs, but it's partly how we chose iocoop: 
https://docs.google.com/spreadsheets/d/1h_gEnVagTZJi0WYWZE9oOKVYIM2WIGnpDHAolDItBz4/edit?gid=627262930#gid=627262930
     - Andrew's password store access
         - Or the delegated access question
         - On the loomio access poll: https://www.loomio.com/d/jrbG5tue/server-access/106
         - Do we need that? Given that other people already have access to some of the coop's admin resources without being part of the TWG group
         - It would be ideal to add delegated access whenever we have that (e.g. when the provider has that abstraction)
             - Cloudflare actually supports this
         - What we want:
             - [ ] Delegate social.coop cloudflare access to Andrew's account?
             - [ ] Document somewhere (e.g. in the README of the pass repo) who has delegated access to what (beyond what access to the pass store grants directly)
         - What we have already done:
             - trasnfered domain/Gandhi access to TWG; delegated access to TWG (admin@ and andrewe@) and FWG (andrewe@)
        
## 2024-11-04
- Here: [[Dan]] [[Flancian]]
- Check ins
    - [[Dan]] is stressed about the US elections, mild work chaos
    - [[Flancian]] working a half day, is going through some personal issues
- Agenda
    - VPS https://git.coop/social.coop/tech/operations/-/issues/89
    - Email SPF https://git.coop/social.coop/tech/operations/-/issues/87
    - [[coop cloud]] - Dan wants to upgrade MediaWiki https://git.coop/social.coop/tech/operations/-/issues/85
        - wiki-alpha.social.coop
        - the content of flancian's .abra/servers/hypha.social.coop is in git: 
            - git@git.coop:social.coop/tech/coop-cloud/hypha.social.coop.git
        - the content of flancian's ~/.abra/recipes/mediawiki is in:
            origin  https://git.coopcloud.tech/coop-cloud/mediawiki.git (fetch)
            origin  https://git.coopcloud.tech/coop-cloud/mediawiki.git (push)
            wiki.social.coop        ssh://git@git.coopcloud.tech:2222/flancian/wiki.social.coop.git (fetch)
            wiki.social.coop        ssh://git@git.coopcloud.tech:2222/flancian/wiki.social.coop.git (push)
    - spam response next steps: https://git.coop/social.coop/tech/operations/-/issues/90
        - iftas thread https://connect.iftas.org/forums/discussion/spam-wave-2024-11-04/
    - storage footprint / database size

## 2024-10-07
- Here: [[Dan]] [[Flancian]] [[Calix]]
- Check ins
    - [[Calix]] Weekend resting and also doing some project work
    - [[Flancian]]
    - [[Dan]] too the day off work for daughter's birthday
- Top priorities
    - Thanks Dan for solving the downtime the other day!
        - What should we do so this is not necessary again?
        - Dan: we should wait and see (tm) until the 15th, see if it auto-pays off the balance
        - F: how to solve systemic issue, "someone" should pay it? suggestion: Finance Working Group, Caitlin seems OK with that. Raised it but not spoken enough to fully decide. Should be able to resolve before next payment.
        - D: Can change card. First one with Paypal, second with card, put card on file. Required a second factor for setup, but authentication error paying it second time. So - autopay might not work. Is there a non-individual card we can use? Otherwise fine to continue.
        - F: Makes sense to have a card for the co-op but not yet. Finance working group on it.
        - D: SEPA and Bank Transfer are other options besides CC and PayPal 
            - A bank account could be easier for the coop as we have funds *somewhere* in OC?
            - Calix: experience from other projects is that, as long as we're with Open Collective, it's entirely up to our fiscal host. OC used to offer virtual cards but in a previous experience it just didn't work -- it wasn't for this kind of payment of services. So it wouldn't really help with the bureaucracy, and they don't offer it anymore. We probably don't have access to a bank account as a coop currently to be able to send a transfer directly. Any of the payment methods would be the same, individual pays and then gets reimbursed.
        - F: will report this to the organizing circle and report back in our next meeting. 
        - D: added a reminder in our group calendar \o/
    - wiki merge request? https://git.coop/social.coop/tech/ansible/-/merge_requests/40
        - LGTM, but let's do the mastodon upgrade first to limit changes we push through ansible to one at a time
    - alpha.social.coop next steps
        - (some git engineering occurs)
        - https://git.coop/social.coop/tech/ansible/-/tree/alpha.social.coop?ref_type=heads exists and now has commits also related to other alpha-like features
        - [ ] let's split other experiments off alpha.social.coop branch into e.g. an experiments branch (thank you Dan / sorry for the hassle)
        - [ ] Next action: get a small-ish new VPS to host alpha.social.coop safely and in a way that reproduces the rhizome environment optimally?
    - Mastodon upgrade?
        - Plan
            - We're currently on 4.2.10
            - We want to go to 4.3 by default
                - Release notes: https://github.com/mastodon/mastodon/releases/tag/v4.3.0
                    - Requirements
                        - Postgres: we're in 15
                    - Docker image has split, probably requires changes to our docker compose beyond the version bump
            - And then to 4.3.1
            - How much time do we have today?
                - Only about 20 minutes, so probably not enough to responsibly do all of this today/tonight :)
                - Let's start a branch and then reconvene next week: https://git.coop/social.coop/tech/ansible/-/tree/4.3?ref_type=heads
    - Open bugs triage
    - Placeholder

## 2024-10-07
- Here: [[Dan]] [[Flancian]] [[Ed]] [[Calix]]
- Check ins
    - Dan: life is busy but OK :)
    - Flancian: +1, making progress at work, but need to prioritize that over TWG this week, will only stay part of the call likely
    - Calix: still in visa limbo but enjoying being in Montreal :) OSM time
        - [[OSM]]: [[street complete]]: https://github.com/streetcomplete/StreetComplete/
    - Ed: <>
- Top priorities
    - [x] Fix meeting calendar entry
    - [x] Access for Dan
        - [x] pass encrypt
        - [x] pass decrypt (\o/)
        - [x] ansible push (to rhizome and hypha)
    - [x] Keys in pass (incl. edsu)
        - [x] reach out to calix for an up to date key?
    - [x] Branch for alpha.social.coop updated?
    - Any others?
- Other topics

## 2024-09-23
- Here: [[Calix]] [[Dan]] [[Flancian]]
- Check ins
    - Calix: still in Visa limbo but with progress
    - Flancian: OK, bit tired. just back from holidays in Mallorca.
    - Dan: doing good. Infected with Global Virus. Last time it took very long to get a negative test.
- High level agenda today
    - Standard TWG meeting at 18 UTC
    - OC joins at 18.30 UTC (some people might join earlier best-effort)
- Topics for the TWG meeting
    - ✅ Round the table (agenda building)
    - Next steps for onboarding new members
        - We need votes https://www.loomio.com/d/jrbG5tue/server-access/98
        - PRs in flight:
            - for Dan: https://git.coop/social.coop/tech/pass/-/merge_requests/10, https://git.coop/social.coop/tech/ansible/-/merge_requests/39
                - Dan will open a bug to track making sure the updated onboarding process is in the wiki somewhere
            - for Evan: (missing?) - Flancian is asking via matrix about continuing the process
    - Character limit
        - F: next step is to get alpha.social.coop going. WIP branch: https://git.coop/social.coop/tech/ansible/-/tree/alpha.social.coop?ref_type=heads
        - some commits pending
        - so far: cloned main server config, replacing URLs
        - question: how much to share (e.g. S3, mailgun)
        - could we do a coworking session next time to advance this?
            - most definitely; either advance the PR proper or do a sync review of what we have by then.
        - any follow ups from the long loomio?
            - good question
            - edumerco: we agreed to trial a bit higher a limit
            - https://www.loomio.com/d/C4HKmTOa/proposal-to-revisit-extending-the-character-limit-for-posts/82
            - -> https://www.loomio.com/d/C4HKmTOa/proposal-to-revisit-extending-the-character-limit-for-posts/32 1k was approved
    - Quick update on:
        - Bluesky bridge (more on the policy side) and supporting bluesky users
            - Nathan's intro: https://social.coop/@ntnsndr/113148877812139659 
            - On username validation proposal by Nathan Schneider, e.g. edsu.social.coop as username in bluesky
            - Maybe next step is opening a bug for this?
            - Flancian: will do that
        - Bonfire (meeting report)
            - https://anagora.org/bonfire+socialcoop with Mayel and Ivan
            - they are looking for contributors for implementing governance extensions
                - design
                - coding
            - edumerco: been helping them in the interaction design front. a group of students contributed last year. currently they are focused on fixing performance issues, are using bounties.
            - next steps:
                - announce to the community -> the OC could do this?
                - update bonfire.social.coop to latest version
                    - -> file bugs
    - Other pending bugs -> next time
- Introductions with the OC
    - Edumerco: studied biology, born and lives in Buenos Aires. Part of the Organizing Circle; part of an intentional community near Buenos Aires. A fan of cooperation :)
    - Caitlin Waddick: live in Vermont, part of the Finance Working Group. Part of a few cooperatives. Currently in more than one meeting context :)
    - Eduardo (Flancian): part of the TWF for ~2 years, social.coop for ~4. Joined the CWG, and take some shifts, and also involved in the organizing circle. Super into cooperatives, and work in big-tech as part of daily life (e.g. this is meeting no. 8 today). Also from Argentina.
    - Edsu (Ed Summers): worked as a software developer for... long :) Also studied libraries and archives at school, have a background in digital preservation. Working in Stanford U Library. Belonged to many coops throughout life, but this is the only one I'm currently active in. Live in Maryland.
    - Calix: pronouns they/them. Main gig is autonomic coop. Also part of a second worker coop, about to join a third. Part of a few coop federations. Super happy to be here. Been in the TWG for a ~year. Background is in development, science, infrastructure. Autonomic initiated [[coop cloud]], which we're using for some of our services. Usually based in NYC but currently in Canada.
        - Q (edumerco): do you know people from Sutty? We have them in common?
        - A: yes!
        - Edumerco is also at Sutty :) Would love to welcome in Buenos Aires.
    - Kathe Todd-Brown: in University of Florida. Been on Mastodon for 2-3y. Previously at Twitter for ~15y in academic Twitter. Geek out with collaboration and organizational structures. Run several groups in different modalities.
- Questions from/to the OC
    - Q (edumerco): how can we help one another? What do we need to know, how can we best support our work and serve our community?
        - Edsu: something that came up in the matrix chat ~2w ago. On how we organize communication and our meetings. E.g. this meeting we're having now is something we have been missing, as we haven't had as much visibility on what the OC is doing/working on.
        - Edumerco: currently the OC is a group that "catches" whatever doesn't fall to other working groups. It currently works as per [[sociocracy]]. We are not a board/it is not our place to mandate how working groups operate. We set out to organize but not make decisions for others. We can help with: determining which decisions must be made; who should take them.
        - Edumerco: this round of meetings is about understanding best what each group does and how we can support you.
        - Edsu: in terms of gaps, one that comes to mind is about payment of bills -- the hosting bill was left unpaid recently. Is paying the bill a TWG issue or a FWG issue? How to know?
        - Flancian: we can separate the bills in terms of what needs to be paid, from who is paying them. There are notes about this in OC meeting minutes in Loomio. 
        - Caitlin: posts can be posted to OpenCollective and members of the Finance Working Group can approve them.
        - Flancian: now that we are closer to establishing the co-op as a legal entity is it possible to have a co-op credit card which could be used?
        - **Caitlin: will look into this.**
        - Thank you Caitlin!!!
    - Edumerco: on the opportunity of defining our scopes, sociocratically. E.g. the TWG can say "we take decisions on technology, operate the services, but (propose that) we don't pay bills".
        - Together with defining scopes, we can define how we (working groups) interact.
    - Calix: on inter-circle communication, maybe we should raise the fact that we are at low capacity. The OC could maybe boost this and help with recruiting?
        - Edumerco: perfect example of how we can help with, yes. If we can describe the kind of knowledge and interests that a good candidate would have, we could go with that to the community.
        - **Flancian: we'll definitely discuss scope and role descriptions in the next TWG meeting.**
        - Edsu: +1 to Calix. We sometimes run a bit thin; although people come and go. E.g. Akshay did a lot of significant work and then had to take a step back. But still swooped in and purged docker logs in the middle of the night recently :) So it's difficult to estimate what our actual capacity is.
        - Edsu: there is a relatively large group of people who have access to servers but are not active. We need to determine when people lose access. 
        - Edumerco: this working group can decide that. Also, have you considered an oncall rotation/some sort of subgroup that could do small response tasks?
            - Flancian: +1 on the onduty/oncall group, similar to the CWG model. There is the issue of oncall-aversion for some as several of us are already oncall for our day jobs, and the fact that the response SLO for technical issues needs to be somewhat low.
            - This can go well with the task to review access lists.
        - Edumerco: question about documentation. Is it up to date?
            - Edsu: we dropped some things when we moved to wiki.social.coop. There could be more work on this area.
            - Eduardo: can help here.
            - Caitlin: +1 on this being important.
- Possible projects of interest
    - Signup/joining process
        - Edumerco: https://miro.com/app/board/uXjVLdZtJc0=/ is what we've been working with the CWG on
    - Bill tracking
        - Covered above organically :)
- Next time:
    - Let's pencil in: [[2024-10-21]] for the next shared session, then every few months?
        - Kathe: with the CWG we said quarterly cadence, let's default to that? I can make week of Oct 21 but need to get it on the calendar ASAP
        - Edumerco: recommend that the TWG works on scope and role definitions in your next session?
    - Single sign on


## 2024-08-26
- Here: [[Kathe T-B]] [[Eduardo Mercovich]] [[Flancian]] [[@andrewe]]
- Gandhi access for domain:
    - sent by: [[@andrewe]]
    - to: tech.group@social.coop
    - main account: passkey held FWG, but TWG is the listed email
        - delegated access: TWG team for tech; FWG team for admin

- Two Edus remain 
    - Corp woes
    - On the feasibility of revolutions 
    - [[Sutty]] and [[Confluencia]]
        - [[Empresa social]] como vehículo para un nuevo mundo
        - Escala:
            - Madre Teresa
            - ..
            - ..
            - [[Empresa social]] es como una bicicleta
                - Delantera: misión positiva
                - Trasera: lo que produce/vende que avanza su misión
            - [[Mondragon]]
            - ..
            - ..
            - Shell
            - Exon
        - [[TedX]]: 
            - [[cómo me enamoré de una lenteja]]:
                - https://www.youtube.com/watch?v=G5_OJhg-wu0
- social.coop
    - apropos del anti-meta fedi pact
        - a favor de un grupo en vez de contra de una corporación
        - frameworks:
            - [[governable spaces]]
            - [[fediversalist papers]]
        - relacionado:
            - https://mydata.org/
        - nombre provisional para el proyecto/grupo de trabajo?
            - grupo [[ecumen]], [[hainish]] coalition
                - aside: [[omelas]] :)
            - -> [[ecumen]] / [[ekumen]] as the starter nodes
    - [[bonfire]]
        - Reunión del lunes que viene?
    - join.social.coop
        - Edu desarrolló una propuesta
        - Documento en cryptpad
        - There is a 1st draft of the onboarding mail+wiki to be -very much- discussed in
https://cryptpad.fr/pad/#/2/pad/edit/jsMCRO8vrphpM8ZmZz2Qt5iF/

- recomendaciones
    - [[Everyday Utopia]]: What 2,000 Years of Wild Experiments Can Teach Us About the Good Life
    - [[keyboardio m100]]: https://shop.keyboard.io/products/model-100?srsltid=AfmBOoo14VYGQS2RV2tN3KegOsR_KJcCcCs_bY3iSpL-Tn4JK0Towthj

## 2024-08-06
- Here: [[je-ff]] [[Dan]] [[flancian]] 
- Onboarding
    - Get @social.coop email alias
        - Set up using [webarch.email](https://webarch.email/) (someone from the TWG needs to take this step)
        - Go to the Aliases tab
        - Add an alias for [name]@social.coop that forwards to a personal email address
    - Get a git.coop account -- probably at https://git.coop/users/sign_up
    - Communicate your account to a TWG member so they add you to the right Git.coop groups
        - That TWG member should add the username to the tech [Group members](https://git.coop/groups/social.coop/tech/-/group_members)
    - Add public keys:
        - SSH public key to ansible repo in roles/server/files
        - GPG public key to pass repo somewhere :)
    - Someone with existing access needs to re-encrypt [[pass]] files with the new GPG key
    - Once you have access you can get an overview of all the infrastructure:
        - `cd ~/.password-store/social.coop && pass`
    - To access any given `pass` secret: `pass show social.coop/path/to/secret`
    - Gotcha: `wiki` is actually for join.social.coop
- Git repos
    - [[pass]] contains all our shared credentials, either for logging in as a TWG member or for our systems to use when accessing resources
    - [[ansible]] configures the servers.
        - `rhizome.playbook.yml` configures the live server that runs social.coop
        - `hypha.playbook.yml` is for an experimental server
        - the `server` role has [public keys](https://git.coop/social.coop/tech/ansible/-/tree/master/roles/server/files/public-keys?ref_type=heads) for login access
- Possible AIs
    - Do a pass over https://git.coop/groups/social.coop/tech/-/group_members and see if we want to disable access for users that haven't been involved in very long
 

## 2024-07-29

- Here: [[flancian]] [[edsu]] [[je-ff]] [[calix]] [[Dan]]
- checkins:
    - [[flancian]]: awesome trip to the beach!
        - [[Ischia]]
        - lots of reading
        - finished several books!
    - [[edsu]]: doing well, not so hot currently in Maryland.
        - [[Lake Michigan]] for beach time
            - "Sweet Sea"
        - Nice to be back!
    - [[Dan]]: 
        - Missing these meetings!
    - [[je-ff]]:
        - brand new to the coop and to the group
    - [[calix]] (3wordchant): 
        - doing fine, still in NYC
        - trying to decide whether to attend dweb in the west coast
- Seed agenda
    - Done :)
- Follow-up about SSO wiki login
    - Dan: brought this up in Matrix, understanding is that there is a possibility of pointing mastodon at auth.social.coop as the SoT for auth
        - Happy to do exploratory work
    - Calix: yes, had a few discussions about how to do this properly
        - TLDR: 
            - it seems it wouldn't be possible for people to have people keep their passwords
            - we probably don't want to support both SSO and non-SSO at the same time
            - steps:
                - notify the whole coop that the change is upcoming
                - invite people to sign up at keycloak (auth.social.coop), before we do the switch
                - do the switch
                - fix issues
            - things to do:
                - build up that plan
                    - https://doc.anagora.org/twg-2024?edit may have something to get started, but the list above is probably better
                - test the setting, probably in alpha
    - Flancian:
        - +1 to that great list
        - unsure if we could support both sso and not sso but it might be worth it to let the long tail not lose access to the instance
    - Ed: +1 to needing support the long tail, unsure how we would even reach out to users or they would reach out to us
        - Calix: agree that designating contact channels is top priority in the plan. 
            - In terms of having both -- it's an interface issue. In Mastodon you get user/password and 'sign on with single sign-on'. People *will* confuse the both.
            - We need to decide how to get people to onboard to SSO.
            - Should we post to loomio about this/start a poll?
                - Dan: to which extent should this be coordinate with the community working group? 
                - **Flancian: will bring this up with the organizing circle and the CWG.**
- alpha.social.coop
    - alpha.social.coop branch in ansible: https://git.coop/social.coop/tech/ansible/-/tree/alpha.social.coop?ref_type=heads
    - Status: one commit in the branch, needs at least one more and an update to pass. Then we need to get a VPS to deploy, and set it up in ansible. 
    - Next steps:
        - **Flancian: set up coworking session**
        - **Flancian: get new VPS**
    - Projects the alpha would unblock
        - SSO
        - >500 chars limit
        - restores
- What happened with the 500 char limit?
    - Evan is interested, has the patch figured out
    - Blocking on alpha
    - https://github.com/mastodon/mastodon/pull/30091#issuecomment-2241565907 happened
    - Ed: it's unclear what this is blocked by, or when this will be reconsidered.
    - [[Fediversalist papers]] might help here. 🤞
- organizing circle pass-arounds
    - Meeting is now on Wednesdays (every other one, including this upcoming one) at 13 UTC.
    - Calix is in the rotation now
    - Calendar entry hasn't been updated yet but it will be at 13 UTC
        - Flancian will try to update or ping MarieVC
    - https://www.loomio.com/d/02Ms4iH8/organizing-circle-meeting-2024-31-july-wednesday-1300-utc
    - Meeting the Organizing Circle
        - Repurposing our next sync would be the easiest to organize
        - **Let's start half an hour earlier in 2w to cover tech topics, and invite them at the regular time**
        - When do we want to redo the "open house/office hours"
- loomio RSS announcements: https://git.coop/social.coop/tech/operations/-/issues/81
    - Ed: Nathan Schneider messaged us/some of us to onboard a script that is already on git.coop to cross-post loomio activity to mastodon
    - How much would we want to surface in socialcoop@social.coop? Activity for all WGs? Or only some?
    - Flancian: there is a question of how to do it, and where (e.g. hypha). Could start with it running it locally.  And then there is a question of what to post. This could be a good question to bring up to the organizing circle.
    - [[MLTSHP]]: https://github.com/MLTSHP/best-of-mltshp-bot/
    - [[Feediverse]]: https://pypi.org/project/feediverse/
    - [[MastoFeed]]: https://mastofeed.org/
    - [[rss-to-activitypub]]: https://github.com/dariusk/rss-to-activitypub
    - Next actions:
        - **Create test account in the instance to play with?**
        - **Bring up with the Organizing Circle in our meeting: what do we want to cross-post?**
        - **Decide on which approach to take here? From the N tools considered**
- onboarding new members
    - We could set up a session to discuss infrastructure?
        - Would love that!
        - Let's agree over matrix? Default to sometime next week.
- **are registrations working ok?**
    - They are ok-ish.
    - Sometimes work, mostly.
        - As we were meeting there was a question posted to Matrix "did you receive XXX signup? they are asking if we got it" and I think fixing this will create more assurance all around that we didn't lose any applications.
    - But there are rough edges:
        - Sometimes the spam trap over-triggers
        - The feedback is lacking even when it processes a registration; it just dumps the user in join.social.coop's root, and you go 'huh' / are unsure if it worked
        - Fixing this/upgrading would mean some project work in node.js

## 2024-07-15

- Here: [[calix]] [[flancian]]
- checkins
    - [[calix]] attended [[HOPE]]: https://hope.net/, was gr8
    - [[flancian]]: nice weekend. tax return! and divorce proceedings.
    - on how christianity sometimes makes for regressive social laws (e.g. in Argentina and the UK).
    - [[paulo freire]] reivindicates: [[pedagogy of the oppressed]]
- balancing within the group
    - [[organizing circle]] is meeting Wednesdays at... 12 UTC?
    - Flancian going this week
    - Would 13 UTC work better?
        - Yes.
    - [[Could we have a notifier bot]] to nudge people to come to this meeting/block it in their agendas mores?
        - Likely :)
- upgrades took place
- then the queue issue
    - https://social.coop/sidekiq
    - bumped concurrency
    - didn't find anything online about "push" queue. most info about smaller instances. would be nice to find "recipes". how can we investigate mastodon to try to find where sidekiq jobs might be coming from?
    - [[is there a way to get sidekiq data into datadog?]]
        - surely but I don't know it :)
    - https://leah.is/posts/scaling-the-mastodon/ - "The push queue is handling sending local posts to the instances of your remote followers."
        - how does this interact with federation? e.g. if someone's toot gets boosted a lot, would that lead to a bunch of push queue jobs?
    - https://hazelweakly.me/blog/scaling-mastodon/
    - for now things are truckin along
- we should be better at moving stuff to the wiki 🐶🥫
    - yep
    - this would also make it easier to onboard people 
- alpha.social.coop branch in ansible: https://git.coop/social.coop/tech/ansible/-/tree/alpha.social.coop?ref_type=heads
    - so far - replacing social.coop with alpha.social.coop
    - questions, what should be shared vs separate?
        - mailgun can probably be shared
        - what is paperclip?
            - ruby on rails file upload library
        - secret_key_base
            - rule of thumb - generate fresh ones for alpha? probably no downside cos we're not trying to migrate user DB etc.
    - S3 -> file-based for alpha?
        - sure
    - main Q - how to deploy in a way that doesn't interfere
        - not on rhizome
        - hypha - but co-op cloud, running traefik.
            - could be mix and match coop cloud and bare-docker?
            - in general yes, but...
            - https://docs.coopcloud.tech/operators/handbook/#proxying-apps-outside-of-co-op-cloud-with-traefik
        - easiest = third vps *our choice*
            - we have the budget. want to be responsible with resources. but probably a lot easier.
            - doesn't need to have a lot of resources to start with (e.g. until we import database etc., future brain)
     - Next steps:
         - Publish decision for getting third vps (smaller maybe) to the matrix room for review
         - Get VPS
         - Fork deployment/mastodon in pass to deployment/alpha.mastodon (or so)
         - Continue with PR
         - Deploy new VPS (integrate into ansible)

## 2024-07-01

- Here: [[flancian]] [[evan boehs]]
- [[evan boehs]] working:
    - on bookmarking software, Fediverse compatible
        - sounds like [[betula]] / in that space
        - but Evan is focusing more on the community aspects
        - 20k lines of code in!
    - actually joining a company soon, contracting
- [[flancian]] dealing with hardware issues as half the time
    - tied up with work as well
    - limited amount of time dedicated to social.coop
        - including CWG and organizing circle
- sustainability or this group
    - it would be nice to go back to a cadence of biweekly meetings, and finishing onboarding of new members
- shared projects
    - bump character limits
        - next steps: get alpha.social.coop on mastodon mainline
            - we could fix the [[coop cloud]] recipe for mastodon
            - we could move to deploying alpha.social.coop with ansible <- this seems like the best way to go probably
        - soft timeline: get alpha.social.coop running via an ansible recipe by the next meeting
            - -> flancian
        - get access to ansible
            - -> evan

## 2024-06-01
Here: [[flancian]] trying to bump to the latest security patch :)

- Reported by [[dphiffer]], thank you!
- Mastodon 4.2.7 -> 4.2.9
    - https://social.coop/@flancian/112542709489666310
    - PR: https://git.coop/social.coop/tech/ansible/-/merge_requests/new?merge_request%5Bsource_branch%5D=4.2.9
    - Then ran:

```
cd social.coop/ansible
vi roles/social.coop/files/docker-compose.yml
. .env
ansible-playbook -CD rhizome.playbook.yml  # check the diff in dry run
ansible-playbook -D rhizome.playbook.yml  # -D means diff, omitting -C makes it stick
```

## 2024-05-20

Here: [[Calix]] [[flancian]]

- Check ins
    - [[patio.coop]] meeting in spanish
    - doing the [[reverse theroux]]: https://www.goodreads.com/book/show/130515.The_Old_Patagonian_Express soon!
    - biking
- Recap https://www.loomio.com/d/C4HKmTOa/proposal-to-revisit-extending-the-character-limit-for-posts/32
- alpha.social.coop 
    - status
        - [[mastodon]] vs [[hometown]] recipes in [[coop cloud]]
        - mastodon recipe is less maintained because it has no known users. bit out of date.
        - side question about secrets not being generated by default
            - https://git.coopcloud.tech/coop-cloud/organising/issues/461
    - next steps
            - decide on way forward:
                - still go with the hypha + coop cloud plan and
                    - use hometown or
                    - upgrade/fix mastodon
                - set up a new alpha server and deploy a variation of the ansible role there
                    - (need a new server to still have the reverse proxy setup work without breaking hypha)
                - modify ansible recipe to deploy alpha to hypha without reverse proxy
                    - can we set up [[traefik]] to work as reverse proxy only and forward to a non-coop-cloud-managed container?
                        - [[calix]]: if you add traefik labels to the docker compose file, traefik would configure itself automatically https://git.coopcloud.tech/coop-cloud/mastodon/src/branch/main/compose.yml#L19-L20
                        - you can also provide a traefik configuration file to the coop cloud traefik https://docs.coopcloud.tech/operators/handbook/#proxying-apps-outside-of-co-op-cloud-with-traefik
- Result of the 1k chars poll
    - Q: if we're 'hot patching' the character limits, are we OK with the extra build time for the frontend?
        - [[calix]]: it's a `yarn build` that might add a minute or so to every container start
        - we're 'up two weeks' currently
        - but any time we restart the container during [[twg]] operations, we'll be more disruptive
- Git.coop API key
    - ![](https://doc.anagora.org/uploads/upload_d18b0a750f7762179948fcaa71edeb63.png)
- Other topics
    - onboarding new members

## 2024-05-06 -- Long time no see! (at least with notes?) :)

Here: [[flancian]], [[dphiffer]], [[evan boehs]]?

- Introductions
    - Welcome Evan!
    - Dan in his nth, probably 2-3rd meeting
- Check ins
    - Dan: doing good, although got reported for some toots! some infosec discussion about e2e encryption and metadata.
        - Flancian: interested
        - https://social.coop/@dphiffer/112382733287207301
    - Evan: spent the last week playing with [[docker]] containers :) 
    - Flancian: work, biking and trying to get from planning to doing
- Patching mastodon (for now mainly for the character limit)
    - Evan is proposing having a modified entrypoint script that hot-patches the character limit in two files and recompiles js
    - e.g. `/bin/sh -c "ls && sed -i -e 's/500/1000/g' app/javascript/mastodon/features/compose/components/compose_form.jsx && sed -i -e 's/500/1000/g' app/validators/status_length_validator.rb && RAILS_ENV=production rails assets:precompile && /start.sh".`
    - questions:
        - does the community want this? (let's see)
            - running a poll in the thread for the character limit would be the next step
            - [[evan]] will start one
        - is it technically feasible? (yes)
        - can be removed/simplified once Mastodon supports the backend setting
        - do we want to support patching for arbitrary features?
            - maybe, but moving to [[glitch soc]] or [[hometown]] is overkill and has downsides 
            - [[flancian]] would like social.coop to contribute to shipping features all the way to mastodon upstream -- at least as options?
        - [[dphiffer]] is 1000 the right number?
            - [[evan]] has seen instances with a billion :)
            - never gotten why mastodon doesn't want to produce long posts by default even though they have to manage them
            - [[evan]] https://gist.github.com/shleeable/101b131653c0ff0e21a81bf99a31c7f0 shows the max char distribution
                - [[flancian]] 5000 seems better maybe?
- Accessibility day recap
    - https://stefanbohacek.com/blog/fediverse-world-sight-day-global-accessibility-awareness-day/ is the known proposal
        - discussion about the proposal
            - [[evan]] "none in its current form".
            - alternate proposals:
                - [[evan]] replace images with their actual alt text instead, more representative
                - host/offer bounty on accessibility features for mastodon as a coop
                - [[dphiffer]] inject UI code instead of messing the backend
                - file a proposal, any proposal, to the mastodon project -- e.g. 'disable images' as a setting, or disable posting images without alt text? or prompt users to do it in every case.
                - TLDR: may 16 is too soon to ship any of this, or even test the proposed breakage safely currently -- but we could "commit" to doing *something* for the October date
    - It seems more likely we can get community + tech stack agreemend with such an effort by October (the second day proposed)
    - Pros and cons of breaking this feature for this campaign; S3 complications likely.
        - We need alpha.social.coop first to test anything like this
    - Also, Alternatives
- alpha.social.coop
    - one server: hypha.social.coop
    - two ways:
        - fork ansible recipe or otherwise just deploy the mastodon role to hypha
            - downside: potentially trickier/dangerous if we mess up anything in the fork
        - use [[coop cloud]] to deploy the mastodon recipe in hypha
            - requires abra install
    - both require server access
        - hypha: can give server access earlier/more informally
            - -> first step here would be to get git.coop access, which can take place before the ritual signing-of-the-keys and the full proposal below
        - rhizome/full access; requires a vote to add members to the working group and showing up to the weekly meetings for a while 
            - [[flancian]] will find a past proposal so you can see the model/reuse

## 2024-04-13 -- Tech Working Group Open House!

Here: [[Calix]], [[flancian]], Melissa (ansate), Jamie, Caitlin
    
- Intro
    - BBB vs Jitsi
- [[Check ins]]
    - [[flancian]]
        - Eduardo from Argentina, now in Switzerland
        - social.coop since... 2020?
    - Melissa
        - ansate "to have a handle", silly puns 😍
        - joining from the US west coast
        - appreciation
    - Jamie
        - joining from the US east coast
        - figuring out online meeting stuff, jitsi / BBB
        - interested in the working group / maybe contributing later
    - [[Calix]]
        - they/them 
        - worker-owner at [[autonomic]]
        - lurking in social.coop since 2020, when we launched [[coop cloud]]
        - calling in from [[buenos aires]] currently
    - Evan
    - Billy
        - Billy based in London, GMT+1. :facepalm. :D 
        - 
- This is https://www.loomio.com/d/oPHKpefm/tech-working-group-open-house-saturday-13-april-1600-1800
- Objectives:
    - To share with the community how the group works and what we're planning on tackling going forward
    - To listen to the community on feature requests/needs
    - To get to know each other :)
- Draft agenda (add topics here as top level items, optionally tag them with your name)
    - [[TWG 2024]] roadmap (draft): https://anagora.org/twg+2024
        - [[wiki]]: considered stable, not a lot of work planned on it proper.
        - [[single sign on]]: we have a way forward to move the instance to it... but it would require people resetting their password
            - [[ansate]] would everybody need to reset their password or only people who want to have SSO for other services?
            - [[flancian]] in principle everyone... but great question, is that true? maybe we could have two login paths, one legacy and one with sso.
            - [[calix]] IIUC we could have two login paths, although it could prove confusing to users. Possible but maybe worrying?
            - [[jamie]] wonder: can we reuse e.g. federated identity as used in the semantic web? 
                - [[calix]] e.g. indieauth.net?
                - J: https://lescommuns.org/ also uses [[keycloak]]
                - calix :https://git.coopcloud.tech/user/login?redirect_to=%2f 
                - calix: specific example of adding other logins to Keycloak: 
https://tv.undersco.re/plugins/auth-openid-connect/0.1.1/auth/openid-connect
                - it seems with [[keycloak]] we could set up some sort of 'manual federation' with other coops, although it would require manual intervention
                - F: will ask Darius etc. (fediverse service) about identity federation.
                - F: making a secondary path without a cutoff makes it easier to test
                - J: love or hate Bluesky, but nice review of ID protocols: https://gitlab.com/bluesky-community1/decentralized-ecosystem/-/blob/master/topics/identity.md
           - On self-hosting loomio with SSO
               - [[calix]] it might actually turn out that self-hosted loomio is harder to use, as some people may log in to loomio for more than one community
               - F: current default is to not run other services
               - [[jamie]] it might be useful to pin these to [[user journeys]] for members of the community. Would love to join that.
                   - [[flancian]] we can try to keep a map of project:person who is interested and notify when there's activity.
                   - [[flancian]] [[twg]] meetings are on Mondays at 6pm UTC by default every other week, but they can be moved :)
               - F: organising circle, started thinking about this 2 meetings ago.
                   - [[flancian]] AI: to talk to the organizing circle about the mapping of user journeys to ways to engage with the coop.
            - In general, given current TWG capacity, our position is: we shouldn't run anything we don't have to run. So loomio/nextcloud: better to get it hosted, like we do currently (either through the main instance of loomio or mayfirst in the case of nextcloud)
            - On ways forward for Mastodon
                - Character limits vs moving to hometown
                - [[calix]] bumping character limits would up the maintenance cost; but the cost of switching to hometown would be high upfront.
                - [[flancian]] +1, unclear what would be better for TWG members of the future if this generation disappears. Maybe moving to hometown and reducing the maintenance cost upgrade-to-upgrade would be preferable. But then again hometown would eventually 'fade away'.
                - [[calix]] fair but it might be preferable to assume there will be *some* TWG continuity; which is likely to be the case given the number of members.
                - [[flancian]] true!
            - [[Evan Boehs]] joins! :)
                - [[Evan Boehs]] there's the issue of Hometown not being updated in the last few months.
                - On the character limit: looking at the codebase, if the only thing we really want is the possibility of increasing the character limit, that seems to be just one file to update.
                - [[Calix]] we believe it's two files -- but still not a lot of files. The issue is that making customizations to the instance would require us to build our own docker images, which would increase the work that the TWG needs to do (even for an e.g. security update, of which Mastodon has quite a few).
                - [[Calix]] on the path to move to Hometown: it'd mean holding in the 4.2 branch but we could still update (apply security fixes).
                - [[Evan Boehs]] the docker arguments makes a lot of sense. One question about that: could we just 'hot patch' the image? Another: glitch soc could be an alternative?
                - [[flancian]]
                    - proposal: let's use one of the existing threads, or start a new one, to discuss the alternatives we have here for character limits.
                    - to the two mentioned, let's add trying to get the PR for adjustable limits in Mastodon reactivated :)
                    - AI: do the above.
            - [[Billy Smith]] joins
    - (five minute break!)
    - [[check ins continue]]
        - [[caitlin]] joining from vermont! interested in constructive procrastination ;)
        - [[billysmith]] woke up recently, far away from UTC :)
    - BBB access
        - F: comes via meet.coop membership
        - mayfirst membership
    - Expanding character limits
        - As per above and Evan's question
        - next step is to designate a loomio thread to continue the discussion
    - Moving to [[Hometown]]
        - same as above, plus the glitch alternative
    - Offering other services beyond Fediverse
        - [[Matrix]]?
        - [[Nextcloud]]?
        - [[round the table]]?
            - [[calix]]: 
                - can't think of any except nextcloud, and we already get that from mayfirst (as per above discussion).
                - [[matrix]] seems hard to host. but we could consider a coop host? https://cooperative.computer 😉😉
            - [[caitlin]]: interested in this but at this point don't know the possibilities.
                - [[flancian]] thank you, we should survey these and tell the community.
            - [[jamie]] 
                - authentication service/sso and tools in that space
            - [[flancian]]
                - maybe a pad? etherpad. could generate more collaboration by virtue of being there.
                - [[matrix]] -- but I agree with Calix's comments.
                    - but we currenty do support mostly through matrix, so it seems making it easier and unproblematic to use matrix is worth it.
                    - [[billysmith]] never been able to make matrix worth properly :)
            - [[billysmith]] more specialized in hardware over here -- interested in enabling a space for people with similar interests.
                - http://resiliencemaps.org/ 😄 
                - https://wiki.london.hackspace.org.uk/view/Equipment
                - [[flancian]] will bring it up with the [[CWG]] as there was recent discussion about [[meatspace]] gatherings; this seems related. I could also see the [[FWG]] being interested in having a list of projects that can be funded for different purposes, although the focus so far was closer to supporting digital-first efforts.
        - [[Evan Boehs]]:
            - what is going on with bonfire.social.coop?
            - what is the twg’s opinion on the feasibility of patching mastodon to increase the value of StatusLengthValidator::MAX_CHARS 
            - [[flancian]] if we apply a patch, or modify the instance  in any way, the next step would be to set up alpha.social.coop. A good starter task for a new member ;)
       - next steps
           - join the TWG matrix: https://matrix.to/#/#socialcoop-tech:matrix.org
           - element is a safe default if you don't have a client
           - https://fluffychat.im/ is also recommended
- [[checkouts]]
    - questions:
        - should we do this again?
        - any suggestions on what to do next time?
    - [[jamie]]
        - to clarify: this was an open house that is distinct from the weekly?
            - yes
                - for regular meetings in the coop: https://share.mayfirst.org/apps/calendar/p/KG92DPwX3ww442AD
            - really appreciated this format
    - [[caitlin]] good to see you!
    - [[billysmith]] nice to put faces to the names!
    - [[calix]] really cool that you came
        - interested in doing this again -- I wonder about the frequency
    - [[flancian]]
        - https://share.mayfirst.org/apps/calendar/p/KG92DPwX3ww442AD
        - yes, would love to do this ~quarterly by default
    - [[evan]] it was great!
    

## 2024-03-25

Here: [[Calix]] [[flancian]]

- [[check ins]]
    - [[flancian]] - no more layoffs! agreement signed after 6mo of work. positive reactions. happy to return to dayjob 🥳
    - [[Calix]]
        - Back in Buenos Aires
        - Inspiring experience in the día de la memoria ([[24 de marzo]]).
        - Waiting on US Visa application.
- announce [[open house]] in loomio? if it hasn't happened yet
    - oh right!
    - **saturday 13th April, 1600-1800**
    - Calix will post in the general loomio space today
- [[twg roadmap]] updates
    - come back to this at open house
    - [[flancian]]: was interviewed for the [fediversalist papers](https://write.as/fediversalist-papers/) interview -- touched on some technical proposals
        - asked to maybe get in contact with other instances having their own TWGs
        - discussed [[meta federation]], meaning federating moderation actions/blocks/limits/etc. within activitypub proper
- organizing circle requests / passdowns
    - notes:
        - https://www.loomio.com/d/xMeTqRsg/organizing-circle-meeting-2024-27-february-tuesday-1300utc
        - https://www.loomio.com/d/K4ybf7I1/organizing-circle-meeting-2024-12-march-tuesday-1300utc
    - TLDR:
        - some concern about wiki access
            - they brought up the possibility of setting up a namespace that the organizing circle can write to/access
                - it seems fair but [[flancian]] and [[calix]] have no personal interest in setting this up
                - would rather use version history and protect the very few pages that need to be protected
                - configuring mediawiki ACLs is a bit annoying
        - some asks related to calendar management
            - would rather give them the keys to mayfirst admin instead of having to set up stuff for other groups
            - C: would be nice if mayfirst could find a way to allow SSO to their hosted nextcloud
            - we could set up our own nextcloud on top of our SSO as an alternative, mid-term, but it comes with extra admin overhead (does it?)
            - Q: is anyone using nextcloud filestorage?
                - A: we don't know.
            - Maybe it's worth signing into the admin console and checking it out.
            - Update: [[flancian]] looked it up in the Mayfirst admin interface, and it's at 15% of our quota (243 MB / 36 GB). 
        - interest in the open house
- spam response preparation
    - on hold -- maybe something to add to the roadmap?
     
## 2024-02-27

Here: [[Calix]] [[edsu]] [[flancian]]

- [[check ins]]
    - [[Calix]] in [[Rio de Janeiro]] \o/
    - [[edsu]] welcoming spring
    - [[flancian]] still dealing with layoffs but trying to also go back to the technical day-to-day job
- [[last episode]] 📺
    - dealt with the Mastodon upgrade (thanks!)
- this time!
    - open house, mid-April
        - poll https://crab.fit/socialcoop-tech-working-group-open-house-175110
        - meet and greet
        - welcoming new contributors, or returning comrades
        - next actions:
            - fill this ourselves ;)
            - determine 1-2 best slots
                - 1700 UTC wednesday
                - 1600 or 1700 saturday
            - share (again?) in the chat(s) (also the open room?)
            - (next time) share slots/announce in loomio
    - [[fediverse spam]] 🥫🌊
        - [[meta spam]] ;)
            - we hit our mailgun quota again by virtue of notifying all admins of all reports (ha)
        - a script that auto-resolved reports matching a regex would have been great
            - open (or find) a bug report against [[mastodon]] to improve this in some incremental way.
            - it would be nice to federate instance-level blocks
            - is there an API endpoint we could use to automate this or do we need to go to the database?
                - https://docs.joinmastodon.org/methods/admin/accounts/#action seems like it could be it! it takes an account ID (fully qualified hopefully?) and allows for a report id to be attached.
            - does `tootctl` have something?
                - seems not: https://docs.joinmastodon.org/admin/tootctl/
            - next action: give it a stab / share if we get something working, maybe a python/requests program?
        - the spam might have been trying to 'make a point' this time
        - it seemed quite targeted/singled out certain users
        - we could have a mastodon release announcement bot in matrix?
            - maybe there's a release bot for github CI?
    - single-sign-on
        - there's interest in SSO in the organizing circle
            - F: great place for us to get a feel of what other working groups need. requests may naturally flow through org. circle, instead of needing full-graph connectivity between working groups
            - F: next steps? auth.social.coop working, open. test logging in as admin (deets in `pass`)
            - E: open reg?
            - F: no approval flow
            - C: tried plugin, but didn't work so great at autonomic. were trying to combine with email domain allowlisting, maybe doing approval by itself would be easier. https://gruchalski.com/posts/2021-06-06-extending-keycloak-required-action-providers/
            - C: the only flow which we've tested and works is invite links, using keycloak-collective-portal https://git.autonomic.zone/autonomic-cooperative/keycloak-collective-portal
            - F: invite link could work well for new users. currently we send invite link (CWG) by email which isn't really secure. could replace signup screen with hardcoded "reach out to admins". low-tech solution. CWG also brought up that it would be nice if some part of the wiki could only be edited by people in a working group.
            - E: the organizing circle was asking about the calendar, and how to restrict editing to some people.
            - Our position: we prefer [[trust but verify]]. Meaning: we'll check 'is in social coop' programmatically; but everything else is up to group trust/human protocols.

## 2024-02-13

Here: [[flancian]] [[Calix]] [[andrewe]]

- [[check ins]]
    - [[calix]]
        - burnout adjacent
        - still nice to be in Buenos Aires
        - been doing some videogame dev, nice break
            - trying [[haxe]]
    - [[Flancian]]
        - fighting work nonsense. layoffs, stress from withing group. mediation is hard. missing actual dayjob.
        - doing some writing that hopefully can help navigate this process within the company
    - [[andrewe]]
- hotpatch! well done gang
- schedule for this meeting?
    - we did a vote, only one participant. what 2 do?
    - F: let's do both: keep regular meeting slots. also poll for a one-off meeting. we can make regular time a topic of that.
    - C: date poll?
    - F: make sure we post it as widely as possible
    - C: crab.fit? https://crab.fit/
- [[bug bash]]!
    - https://anagora.org/go/twg/bugs
    - great progress on some, like the domain issue!
- peering at some bugs (https://anagora.org/go/twg/bugs)
    - https://git.coop/social.coop/tech/operations/-/issues/71
        - F: good first ticket. unrelated to day-to-day ops. will try to work on it to define it more.
    - [x] set up backups (cron) for [[mediawiki]] 
    - [x] set up backups (cron) for [[keycloak]] 
    - [x] upload new backups to digital ocean
    - [x] test restores for social.coop instance
    - [x] test restores for wiki and keycloak
- [[cwg]] passdowns
    - F: main thing: boost bot!
- organising circle
    - F: attended first meeting, missed second, hoping to hit next one. carried question of running more services. want to get a sense from community about what folks are interested in having.
    - shared https://anagora.org/twg+2024 with them, suggestion to poll the community for which services they would like to see take shape
    - Andrew: this should be bidirectional, a shared discussion
        - More generally the interaction between working groups must be n-directional
        - Andrew is interested in the interface with the 'real world' of laws and finance
- Shared calendar stuff
    - F: nextcloud is a bit unideal because access 
    - C: used Radicale but no SSO https://radicale.org/
- Next actions:
    - Set up one-off wider call
        - What is the scope of this? What should we call it?
        - F: "goalsetting" sounds good. but what about new people? "call for contributors" / "call for feedback". "open day"
        - C: really like "open day" / "open house"
        - C: Shoot for March deadline for poll, mid-late April for meeting?
        - F: align priorities in next month. come up with tasks. community call: these are the tasks up for grabs. make it concrete for people to see how they could contribute.
        - https://crab.fit/socialcoop-tech-working-group-open-house-175110
    - Update the shared calendar if we make any changes to the cadence


## 2023-12-18 .. [[2024-01-01]] .. [[2024-01-15]]
Here: [[flancian]] [[Calix]] :)

Wish you all a great holiday season! Some topics:

- [[check ins]]
    - [[calix]] in [[Buenos Aires]] 🤘
        - on the [[three word chant]] pattern  
        - https://facttic.org.ar/
        - https://patio.coop/
        - the [[network of cooperatives]] or federation pattern
    - [[Flancian]]
        - one hand: doing great, excited to be in this historical / physical context. interesting projects!
        - bedbugs 😔 ethical and practical horror. Google layoff round ∞, stress, lots of work
        - maybe some parallels between the two? :D
        - writing as [[catharsis]]
    - [[cooperative journals]]
- [[2024]]
    - F: how can we serve social.coop. how can s.c serve greater purpose? in the fediverse, in international tech coop movement.
    - [[twg 2024]]
        - [[single sign on]]
            - F: even though migration to SSO seems like a bit of would be cool to write docs on it to benefit the federation.
        - other services/more integrations?
            - this seems like it could be a good cooperative effort with [[coop cloud]]?
            - F: would love to run new services on [[coop cloud]]. examples of recipes where you can optionally compose containers. ideally would love to base mastodon SSO on keycloak. what else? people have been asking for other services. could do a poll?
            - C: other platforms like [[cloudron]] [[sandstorm]] have a little more integration between apps but not much, would also be a great opportunity for documentation / collaboration. gaps: mastodon-to-archive, mastodon-to-other-instance, matrix on top of SSO.
                 - F: [[beeper]] interactions -- messaging as the next social platform. pidgin, libpurple, moa.party (need to pay Elon Tax™ tho -- although could be an option for smaller communities).
                 - F: anti-fedipact position is based on wanting to help users get out. corporation which interops is offering ways to defeat walled gardens. give users an option.
                     - success stories in this space
                         - [[pixelfed]] importing Instagram GDPR archives
                         - [[bookwyrm]] does something similar with [[goodreads]]
                     - related communication on the instance w/[[calix]], [[ntnsndr]], [[flancian]] et al
                         - [[meta]] it is quite a bit better than loomio for this kind of conversation...
                         - C: TWG could work on importing Twitter / Facebook archives into mastodon, on behalf of social.coop.
                         - F: Like the bidirectionality where it encourages companies to add interoperability. Also usability of logging in is better than e.g. Twitter Takeout.
                         - Let's try to do both? :D
                     - F: Moderation and federation actions should be federated within activitypub, multi-software. Federation within groups not just within instances. Threads is the next iteration of scaling. Maybe reasonable to model as sub-networks; reasonable people, fascists -- saying we won't federate with fascists. A lot of the work of fediverse is banning fascists. That needs to be automated; that's a lot of work.
                     - C: this seems like something worth exploring; it seems like it would require support by threads.net and/or other large instances, like for example mastodon.social. Also have hope that we can achieve this on a cultural and technical level to make it easier to host smaller servers than large monolithic ones overall (vs current reality where it's kind of the opposite).
                     - F: If fediverse ends up being decentralised; improving the toolchain so people can mostly be on small instances, that would be the best outcome. We should hedge and try and do both. As long as there's a motivation under capitalism to centralise it will continue to happen. In 5-10 years there will be new platforms, formats, which could again see capitalist entities trying to centralise for profit. Fediverse could be more resilient. Idea: write an addendum to Fedipact which says "this is how Threads could federate". FRom a point of view of the company, harder to push back on specific technical demands.
                     - C: they certainly find it easy to push on ethical arguments; trying to get them on a technical argument might make sense.
                     - F: Hedging, we can see which of the toolchains / approaches we invest most in, happy to start with 50:50. Personally wany to try the corporation negotiation approach. Would take any chance to push FB in the right direction. Also full respect to people who say the safest thing is to not federate for now. Happy to help on both fronts.
        - backups
            - at first glance unexciting but so necessary :)
                - we probably want to cut bugs for what remains?
                    - https://anagora.org/go/twg/bugs redirects to the component
                - for sure:
                    - [x] test restores for social.coop instance
                    - [x] set up backups (cron) for [[mediawiki]] 
                    - [x] set up backups (cron) for [[keycloak]] 
                    - [x] test restores for wiki
                    - [x] test restores for keycloak
                - **calix** will make some bug reports
        - etc.
    - [[meta]] do we want to poll for a new time/day?
        - F: seems worth doing?
        - C: +1 -- we talked about this back in September. Would suggest:
            - Plan A: we do a one-off date poll for a [[social coop tech working group goalsetting]] session. People commit to attending that; then we discuss further engagements there.
            - Plan B: we work on a roadmap ourselves and we announce the roadmap at the same time as the poll.
                - There is a roadmap draft at [[twg 2024]]: https://anagora.org/twg+2024
            - Plan C: do a date poll for recurrent meetings straight.
            - F: will share these options and these notes in the room, and then let the room choose the plan using emojis :D
- [[organizing circle]] update
    - [[flancian]] will attend the kickoff tomorrow 15 
    - anything to relay?
        - F: could bring up fedipact, authorized fetch, for awareness. group is in a good position to drive in a more organised way than loomio thread
        - C: how frequent are meetings? wondering about raising Q of other services.
        - https://www.loomio.com/d/iobhRrMZ/oc-meetings-thread-when-and-how-to-meet- -- will discuss cadence I think
- https://git.coop/social.coop/tech/wiki.social.coop/-/merge_requests/9
    - We could simplify the static site and insert references to wiki.social.coop.
    - [[edsu]] deployed!
        - \o/ awesome!
        - some possible further changes:
            - first link should go to the instance proper
            - join 'call to action' could go straight to the form
        - [ ] We have to set up automatic backups for wiki.social.coop.
            - as per the above
- [[ntnsndr]]'s bot
    - https://git.coop/social.coop/socialcoop-govbot
    - would be nice to run in our infra
    - would like to discuss with ed
- [[authorized fetch]]
    - F: currently not into it because it would lock some implementations (non-mastodon) out?
    - C: IIUC it's part of standards but if it's difficult to implement it might result in this
    - F: Maybe we should have an alpha.social.coop to experiment with such things?
        - It could run on SSO? ;)
        - C: agreed, lot of information missing from docs
- [[fedipact]]
    - already covered partly above

## 2023-12-04

Here: [[edsu]], [[Flancian]]
- Check ins
- Our mission: upgrade to Mastodon 4.2.2
    - https://github.com/mastodon/mastodon/releases/tag/v4.2.2
    - question: do we go to https://github.com/mastodon/mastodon/releases/tag/v4.2.1 first or go straight to 4.2.2?
        - both migrations are straightforward, no migrations involved, so it seems we could go straight to 4.2.2
    - let's try going to 4.2.2
        - let's make sure backups are running
        - they are: https://cloud.digitalocean.com/spaces/social-coop-media?i=7e7429&path=backups%2Frhizome%2F -- last backup 7h ago
    - https://git.coop/social.coop/tech/ansible/-/merge_requests/33
    - ...and it worked!

## 2023-10-09

Here: [[Akshay]], [[edsu]]I'll b, [[Calix]], [[Flancian]]

- Check ins
- Mastodon 4.1 upgrade report
    - A: was chill!
    - E: search improvements?
- Tech roadmap? (from previous meeting)
    - we think Flancian created a draft? https://anagora.org/twg-2024 
    - A: would like to do SSO sooner vs later, then fewer people will need to go through migration steps
    - E: Concerns about doing things just because we can (unless we're tightening up things we're already doing), e.g. bringing new services online -- does someone other than us want them?
    - A: there has been interest in SSO, as well as some interest in Hometown
    - A: Hometown has been stuck on v4.0.x so it's of some concern
    - C: another concern is that there isn't a docker setup, so we would have to build our own, or move away from Docker at social.coop and lean more on Ansible
    - C: do we want to add something to our roadmap about the Organizing Circle, to help us to communicate with other working groups better? e.g. how we rotate our representation there, what we should tell them, what we should ask
    - C: SSO does seem like a priority, for users to be able edit wiki they need to ask for a SSO account
    - E: Agree, it's a little better than what we had before, but not good that it's still gate-kept by the extra signin. Is the question whether to use SSO for social.coop mastodon?
    - A: Yes. wiki already uses it. Loomio we can't unless we selfhost. So just mastodon. Saw a similar migration done on another instance, was a bit of work.
    - A: we had good communication channels with our users via email about the change, and letting them know the change to the login
    - C: I've only set up SSO for hometown, not sure how to hide the login button but it is important
    - C: You can pay Loomio more money to get SSO working. Agreed communication would be key, we would frustrate and potentially lose users if we didn't communicate properly.
    - C: We did talk about migrating passwords, but we established that we couldn't because mastodon and keycloak use a different hashing algorithm
    - F: backups and restores are high priority still
    - F: we could extract email addresses from Mastodon, email them to create a new username and password, and give them a month, and then have a cutover. This would allow us to handwave migration.
    - C: if there's an ordering to the roadmap we could have SSO first; I think it would be confusing if you could login to mastodon with either approach (local vs sso). 
    - F: agree
    - A: we also did not have both, it was switched over on a particular day
    - F: we can generate a CSV of usernames and generate accounts for them, and then email them links to complete the setup
    - We should probably use a test instance to verify SSO/Keycloak is working with Mastodon.
    - C: might be an opportunity to better integrate Ansible and coop.cloud tooling (abra)?
    - https://git.coopcloud.tech/coop-cloud/mastodon is the coop cloud recipe that we could use for this testing instance.
    - C: switching to hometown will need additionally planning since downgrading would be difficult/tricky ; we would need to slowdown updates to social.coop to let it catch up
    - F: we should leave in the roadmap in case people want to discuss, but not a priority
    - C: probably should put behind the wiki and SSO; we also should prioritize organizing circle involvement
    - F: still is a question about Bonfire, but we can postpone discussion
    - C: I wanted to ask about blip to access, on Sunday Oct 1. I didn't get around to seeing if datadog would be helpful to check what happened, also it's not clear if we are getting alerts about availability. I could ssh to it at the time.
    - A: I did look at it and couldn't find any evidence; the Datadog credentials are in the password store. We don't monitor a bunch of things, and maybe we should talk about that. Should we include Datadog/Grafana plans as part of the roadmap?
    - C: at coop.cloud we were using uptimerobot for a bit; we are doing self-monitoring, uptime-kuma at the moment; even signing up for a free service like pingdom.
    - F: we should get it (monitoring) into the roadmap and make a request
- Notes to future selves
    - Issues raised from CWG
        - TWG could take a look at the governance update proposal https://www.loomio.com/p/OI8kEjVz/social-coop-organizing-circle-proposal
        - NextCloud calendar doesn't seem to really notify by email -- could we raise to Mayfirst?
            - Some reports of NextCloud jankiness in general, sometimes it just sping (tm) -- maybe we can work with Mayfirst to improve this?
            - meet.mayfirst.org seems lower quality than other jitsi instances maybe?
                - ping from CH to galeano.mayfirst.org is only 83ms
                - might be a 360p default
        - Some email issues, but not many?
            - 5.7.23 <jag@mail.mayfirst.org>: Recipient address rejected: Message rejected due to: SPF fail - not authorized.
        - There is some desire to have a bot that automatically boosts in-instance #introduction posts
    - Wiki next steps
       - We need to set up and test backup/restores


## [[2023-09-26]]

Here: [[Akshay]] [[Flancian]] [[Calix]]

Mastodon upgrade party!

- checking update path
    - https://github.com/mastodon/mastodon/releases/tag/v4.1.5 looks good
    - https://github.com/mastodon/mastodon/releases/tag/v4.1.6 looks good
    - https://github.com/mastodon/mastodon/releases/tag/v4.1.7 looks good
    - https://github.com/mastodon/mastodon/releases/tag/v4.1.8 looks good
    - https://github.com/mastodon/mastodon/releases/tag/v4.1.9 looks good
    - upgrade plan: go 4.1.4 -> 4.1.9 direct 
        - PR: https://git.coop/social.coop/tech/ansible/-/merge_requests/31
    - then go 4.2
        - https://github.com/mastodon/mastodon/releases/tag/v4.2.0 non trivial
        - PR: https://git.coop/social.coop/tech/ansible/-/merge_requests/32

## [[2023-09-25]]

Here: [[Akshay]] [[Flancian]]

- Check ins
    - [[Akshay]] super busy, finding a house
    - [[Flancian]] busy with + layoffs, but trying to keep optimistic
- Notes to future selves
   - [[flancian]] Proposal to seed a roadmap to track projects at a high level and request comments from the community
       - [[twg 2024]] is the default work in progress, meaning https://anagora.org/twg-2024.
   - Wiki next steps
       - Pretty stable/usable.
       - our position on [[coop cloud]]
           - interesting
           - [[akshay]] concerns with putting stuff in the home directory.
           - [[reproducibility]] seems maybe a fuzzy area
           - how does it compare with:
               - [[ansible]]
               - [[nix]]
                   - high barrier to entry
                   - on [[functional heads]] ;)
           - ranked by ease-of-use
               - if you use docker, [[coop cloud]]
               - if you don't or want to do host-level stuff, [[ansible]]
               - if you want full reproducibility, nix -- but that's not ease of use
   - SSO next steps
       - Backup/restore of users
       - Keeping users in sync with other sources we have currently:
           - loomio
           - social.coop instance (Mastodon)
   - Mastodon next steps (main instance)
       - Move to Hometown: yay or nay?
   - Bonfire next steps (for a second instance)
       - Configure SSO (Mayel sent a build to try)
           - We need to try this
           - Find the build/incantation?
       - Test federation fixes once they're there
       - This can be run at a lower SLO until the community finds it critical
       - Potential: we could potentially move governance to it if the collaboration features land.
       - Would we want to ever move the 'primary' instance to it?
   - We need to exercise backup/restores in general
       - [[Flancian]] tested backups for the wiki, restores come next :)
       - next action: cronjobs? those could be in ansible?
           - [[Akshay]] does coop cloud have cronjobs?
   - Can we model moderation using [[ActivityPub]]?
       - Instances could federate moderation decisions, optionally also ranking.
       - e.g. social.coop and autonomic reciprocally trust each other
       - extending/generalizing #fediblock
   - On [[Open source governance]]
       - [[Codeberg]] and [[Forgejo]] might have this solved
       - [[Concourse]]
       
## [[2023-09-11]]

Here: [[Flancian]]

- Check ins
- Notes to future selves
   - [[flancian]] Proposal to seed a roadmap to track projects at a high level and request comments from the community
       - [[twg 2024]] is the default work in progress, meaning https://anagora.org/twg-2024.
   - Wiki next steps
       - Pretty stable/usable.
   - SSO next steps
       - Backup/restore of users
       - Keeping users in sync with other sources we have currently:
           - loomio
           - social.coop instance (Mastodon)
   - Mastodon next steps (main instance)
       - Move to Hometown: yay or nay?
   - Bonfire next steps (for a second instance)
       - Configure SSO (Mayel sent a build to try)
       - Test federation fixes once they're there
   - We need to exercise backup/restores in general
       - [[Flancian]] tested backups for the wiki, restores come next :)
 
       
## [[2023-08-28]]

Here: [[Calix]] [[Flancian]]

- Check ins
    - Calix met Akshay in Berlin!
- Notes to future selves
    - Issues raised from CWG
        - TWG could take a look at the governance update proposal https://www.loomio.com/p/OI8kEjVz/social-coop-organizing-circle-proposal
            - Default plan:
                - [[flancian]] attends the first few meetings as representative if nobody else volunteers (by default) :)
                - we rotate as people want/can, [[Calix]] volunteered whenever time frees up :)
    - Issue of attendance
        - Low attendance to these meetings as of late
            - Common after summer breaks, but we want to make sure we keep critical mass going forward
            - Idea: start writing a roadmap document with possible next steps for the group, good opportunity to converge on plans *and* get them reviewed by other working groups and the social.coop community
   - Wiki next steps
   - We need to set up and test backup/restores
       - [[Flancian]] tested backups for the wiki, restores come next :)
 
       
## [[2023-08-14]]

Here: [[Flancian]]

- Check ins
    - Just chillin' in https://meet.mayfirst.org/social-coop-tech :)
- [[abra backups]]
    - Started experimenting with `abra app backup`.
    - first finding: abra app backup auth.social.coop worked as expected I think -- it left me with a (quite small) auth_social_coop_db tarfile in ~/.abra/backups. this is nice :)
    - second finding: abra app backup wiki.social.coop says 'no backup configs discovered for wiki.social.coop' -- maybe the recipe doesn't support this yet?
    - same for bonfire.social.coop.
    - oh, but https://git.coopcloud.tech/coop-cloud/mediawiki/commit/3018af938260691337bdf34da5a42d41e330894a makes me think upgrading the wiki recipe should be enough to get us backups though
    - trying updating wiki-alpha first with: abra app deploy -C wiki-alpha.social.coop (after git pull in ~/.abra/recipes/mediawiki)
    - success -- after this update, abra app backup wiki-alpha.social.coop worked :)
    - updating wiki.social.coop with: abra app deploy -C wiki.social.coop
    - now `abra app backup` works for wiki.social.coop \o/
- Notes to future selves
    - Issues raised from CWG
        - TWG could take a look at the governance update proposal https://www.loomio.com/p/OI8kEjVz/social-coop-organizing-circle-proposal
        - NextCloud calendar doesn't seem to really notify by email -- could we raise to Mayfirst?
            - Some reports of NextCloud jankiness in general, sometimes it just sping (tm) -- maybe we can work with Mayfirst to improve this?
            - meet.mayfirst.org seems lower quality than other jitsi instances maybe?
                - ping from CH to galeano.mayfirst.org is only 83ms
                - might be a 360p default
        - Some email issues, but not many?
            - 5.7.23 <jag@mail.mayfirst.org>: Recipient address rejected: Message rejected due to: SPF fail - not authorized.
        - There is some desire to have a bot that automatically boosts in-instance #introduction posts
    - Wiki next steps
       - We need to set up and test backup/restores
 
       
## [[2023-07-17]]

Here: [[Akshay]] [[Flancian]] [[Calix]]

- Check ins
    - Travel plans
        - Akshay: Barcelona!
            - Montjuic
                - MNAC
                - Miró
        - Eduardo: Swiss Jura / Anarchism tour
        - Calix: Glasgow! Then Berlin
            - Akshay: would be great to catch up!
            - Mid-Aug to Mid-Sep
                - CCC Camp Tickets still around: https://tickets.events.ccc.de/camp2023/
            - September sounds good
    - Calix: getting over a cold but also had a super productive day \o/
    - CCC Camp in Berlin around the same dates
- Notes to future selves
    - Mastodon update (thank you Akshay!)
        - Do we want to hold for Hometown?
        - They haven't upgraded yet? Still on 4.0, we're on 4.1
        - https://github.com/hometown-fork/hometown -- how long did they take to pick up the security fix? July 7th (4.0 series) and 9th (3.5 series)
        - They patched same day-ish, so it seems like a healthy situation
        - If we want to move, either we wait for them to bump to 4.1 or we look into a 4.1 -> 4.0 downgrade?
        - Default is we wait, they seem to be working on moving to 4.1.
        - What about [[glitch-soc]]?
            - [[Glitch]] was brought up by [[jonny]] as an alternate ([[glitch-soc]]).
            - But we didn't look into it deeply yet.
            - It's unclear what their last release is.
            - Actually it runs on main/seems very bleeding edge by definition/intent: https://github.com/glitch-soc/mastodon
            - Probably not a good idea for social.coop at this point in time, not for the main instance.
    - join.social.coop update (thank you Ed!)
        - https://git.coop/social.coop/tech/wiki.social.coop/-/merge_requests/8
        - https://git.coop/social.coop/tech/ansible/-/merge_requests/28
        - Waiting for these to be merged.
    - Issues raised from CWG
        - TWG should choose an emissary to the [[organizing circle]], mechanism up to us.
            - This comes from https://www.loomio.com/d/txYOWJ4q/organizing-a-growing-social-coop-an-idea-for-a-proposal
        - TWG could take a look at the governance update proposal https://www.loomio.com/p/OI8kEjVz/social-coop-organizing-circle-proposal
        - How do we choose? How often do we rotate?
            - Let's first gauge who could be interested in this
            - Actually let's all volunteer at https://www.loomio.com/d/GhC8oEcK/organizing-the-social-coop-organizing-circle/2 if interested and take it from there.
        - There is some desire to have a bot that automatically boosts in-instance #introduction posts
            - Additionally some desire to have a bot that automatically publishes loomio activity
            - Maybe let's open some bugs and link them here: X, Y
    - Wiki and SSO next steps
       - We need to set up and test backup/restores
       - We need to decide an onboarding flow -- maybe it should just be added to the registration process currently handled by the CWG?
           - [[Calix]] there is an invite-like flow developed for keycloak by someone else in autonomic
           - https://git.autonomic.zone/autonomic-cooperative/keycloak-collective-portal / https://git.coopcloud.tech/coop-cloud/keycloak-collective-portal
       - Let's also move these items, ideally well scoped, to bugs?
           - Z, A :)
    - Possible Hometown update next?
       - There is maybe a fork in the road leading to bonfire.social.coop for governance
           - https://github.com/bonfire-networks/bonfire-app/tree/main/flavours/cooperation
           - Thanks Akshay and Calix for navigating the mailgun dashboard and finding the right place to add a new mailgun login :)
           - It's in https://app.mailgun.com/app/sending/domains/mg.social.coop/credentials
       - Or Hometown plus self-hosted loomio?
 

## [[2023-07-05]]

Here: [[Akshay]] [[Ed Summers]] [[Flancian]]

- Check ins
    - [[Flancian]] just back from travel in Greece with mum :)
    - [[Akshay]] very nice summer in Berlin
    - Ed stuck at work but following :) 
        - On ansible key
        - Akshay merged :)
        - Docs in new wiki: https://wiki.social.coop/wiki/Update_pass
    - On [[atproto]] and the issue of 'algorithm permission' / ACLs for data federation
        - Akshay: what do people actually want to do with algorithms?
        - The issue of sorting/ranking, not to lose your friends' content
- Notes to future selves
    - Mastodon update (thank you Akshay!)
        - Will be done tomorrow around 3pm CET / 1pm UTC
        - Patchset should be small, no migration needed
        - #mastoadmin is a good hashtag to follow
    - join.social.coop update (thank you Ed!)
        - https://git.coop/social.coop/tech/wiki.social.coop/-/merge_requests/8
        - https://git.coop/social.coop/tech/ansible/-/merge_requests/28
    - Issues raised from CWG
        - TWG should choose an emissary to the [[organizing circle]], mechanism up to us.
        - TWG could take a look at the governance update proposal https://www.loomio.com/p/OI8kEjVz/social-coop-organizing-circle-proposal
        - There is some desire to have a bot that automatically boosts in-instance #introduction posts
    - Wiki and SSO next steps
       - We need to set up and test backup/restores
       - We need to decide an onboarding flow -- maybe it should just be added to the registration process currently handled by the CWG?
    - Possible Hometown update next?
       - There is maybe a fork in the road leading to bonfire.social.coop for governance
           - https://github.com/bonfire-networks/bonfire-app/tree/main/flavours/cooperation
       - Or Hometown plus self-hosted loomio?
       
## [[2023-06-19]]

Here: Akshay, Flancian, 3wc/calix

- Check ins
    - [[akshay]] back in Berlin, trying to find time to do more social.coop things
    - [[flancian]] before holidays, enjoying the handoffs
    - [[calix]] meeting with [[big brother watch]]
- Notes to future selves
    - Issues raised from CWG
        - Meet.Coop discussion
            - "evolution" thread about handing off to [[webtv]] coop in Canada
            - offered to review migration plan and maybe do sysadmin work if we know what to do
        - TWG could take a look at the governance update proposal https://www.loomio.com/p/OI8kEjVz/social-coop-organizing-circle-proposal
        - NextCloud calendar doesn't seem to really notify by email -- could we raise to Mayfirst?
            - Some reports of NextCloud jankiness in general, sometimes it just sping (tm) -- maybe we can work with Mayfirst to improve this?
            - meet.mayfirst.org seems lower quality than other jitsi instances maybe?
                - ping from CH to galeano.mayfirst.org is only 83ms
                - might be a 360p default
        - There is some desire to have a bot that automatically boosts in-instance #introduction posts
    - wiki next steps
       - set up and test backup/restores
           - [[calix]] if mediawiki has a docker label for the backup and restore paths it should be straightforward
               - if not, we could add them
               - [[wordpress]] recipe is the right template
       - PR for simplifying join.social.coop
           - https://git.coop/social.coop/tech/wiki.social.coop/-/merge_requests/8 says draft, check next time
    - keycloak
        - backups and restores
            - as per the above
            - we would need to also add logic to upload backups to s3
            - we can reuse the s3 upload logic from rhizome and add it to hypha
                - **next action: file a bug for this?**
    - what's big and next? :)
        - reddit exodus
            - how to help the fediverse
            - would social.coop like to run [[lemmy]] or [[kbin]]?
                - e.g. [[merveilles]] runs both [[hometown]] and [[lemmy]]
                - next action: start a loomio thread to gauge interest in running a message board
                - note [[lemmy]] is on [[coop cloud]]
        - bonfire.social.coop -- mike hales seemed interested and wanting to give a try, other people mentioned in the past as well on matrix
            - already up on [[hypha]]
            - next step here is to set up the mailer flow so registrations work
            - OR to hook it up with keycloak?
        - moving social.coop to keycloak all in all
        - moving to [[hometown]]
            - would require us to sit back on updates and wait for hometown to catch up (probably only about a month)
            - [[akshay]] there's also the [[glitch]] fork
            - how to choose:
                - motivation based
                - or what's more featureful
                - or what's best for the ecosystem
        - [[akshay]] maybe this section is all motivation-based mainly
        - Main takeaway: next actions for several of these seem to be to discuss on loomio to gauge what the community thinks/wants/needs
        - [[Calix]] another member of the coop cloud federation was asking if social.coop would be interested in being a member of the federation.
            - social.coop seems like a more experimental user of coop cloud, maybe it's too quick?
            - what would being a member of the federation entail?
                - paying either 10 or 20/e a month
                - participating in decision making w.r.t. the direction of the project
                - that's it so far :)
            - formal step would be to discuss on loomio
                - technically it makes most sense if social.coop is using coop cloud day-to-day
                - it's not too much money so we should be able to join earlier rather than later
                - let's bring it up in loomio
    
       
## [[2023-06-05]]

Here: edsu, Akshay, Flancian, (a late Calix)

- Check ins
    - [[edsu]]
        - Summer time -- enjoying :)
        - 
    - [[Akshay]]
        - +1, Berlin is looking like a nice place
        - Justifies being there
        - Every winter brings up the question :)
    - [[Flancian]]
        - Also enjoying Zürich
            - [[edsu]] [[ministry for the future]] takes place there significantly!
                - enjoyed it
                - liked how he tried to write a different kind of book from the usual doom-and-gloom (paraphrasing)
                - [[near future scenarios]] for how we could deal with challenges technologically and politically
                - https://anagora.org/@neil for cool reading club material ;)
        - Except the pollen
    - [[Calix]]
        - Super happy to be back after time lost in The Matrix! Currently in the UK, surprisingly enjoyable time. Very Excited about Autonomic's recent launch of https://cooperative.computer/ – masto post https://sunbeam.city/@autonomic/110458431661481012
            - Maybe a 'keepalive' for federation could be worth implementing?
            - Congrats on the announcement!
            - Further services are wishlist-based, join matrix for proposals :)
            - What about social?
                - For now would probably recommend social.coop
                - Moderation is an open question
            - Moderation for Matrix even is an unknown
                - Good platform for bridges!
                - [[matterbridge]], etc.
                - [[maubot]] also has plenty on offer
                - bridges.coop
- Notes to future selves
    - TWG could take a look at the governance update proposal https://www.loomio.com/p/OI8kEjVz/social-coop-organizing-circle-proposal
    - Issues raised from CWG
        - Excitement about the wiki :)
            - [[wiki builders]] room has a feed https://matrix.to/#/#socialcoop-wiki-builders:matrix.org
            - in the social.coop space: https://matrix.to/#/#social.coop:matrix.org
        - The idea about a bot to auto-boost the #introduction hashtag
        - NextCloud calendar doesn't seem to really notify by email -- could we raise to Mayfirst?
            - Some reports of NextCloud jankiness in general, sometimes it just sping (tm) -- maybe we can work with Mayfirst to improve this?
        - Some email issues, but not many?
            - 5.7.23 <jag@mail.mayfirst.org>: Recipient address rejected: Message rejected due to: SPF fail - not authorized.
        - There is some desire to have a bot that automatically boosts in-instance #introduction posts
            - Fl: we'd need to add a key to the social.coop account
            - edsu: And track which people had posted #introductions already
            - Fl: Maubot runs a lot of our integrations already. Or we could roll our own with a Mastodon (pipe(?))
            - edsu: maybe an issue ticket for it?
                - https://git.coop/social.coop/tech/operations/-/issues/71
    - wiki progress
       - [[wiki alpha]]:
           - could make sense to keep it as a staging environment?
           - do we want to set some kind of expectation for data permanence?
               - no expectations :)
               - Fl: adding a Giant Red (if possible) note about this 🔥
       - keycloak up with social.coop realm
           - Akshay: is it totally open?
           - Fl: Yes! Intended to close it down, so we don't have spam issues. Now is a good time.
           - Ed: Did we want self-registration off?
           - Fl: Another member was surprised it was on. "What we want" is the right topic. How to integrate with registration form? How could you allow people to "sign in with X"?
           - Ak: Better in the long-run to go the other way - logging in with Keycloak into mastodon.
           - Fl: General direction of "what is next".
       - pending:
           - [[backups]] and [[restores]] is pending
               - open an issue
           - email auth / hooking up keycloak to mailgun
               - open an issue
           - figuring out signup flow/user verification
               - [[calix]] tried figuring out approval flows and couldn't understand the steps involved
               - 'sign up using google and get verified' is something that others on The Internet have set up though
               - more immediately, maybe just import existing users using csv or something and add new users using an extra step for our signup flow
               - Ak has experience w/ another co-op importing users from Mastodon into Keycloak
           - figure out if we want to enable logging into keycloak using mastodon as a provider as a migration step
               - although we would want to have mastodon/the instance use keycloak in the medium term
       - cleanup of wiki.social.coop now join.social.coop repo: https://git.coop/social.coop/tech/wiki.social.coop/-/merge_requests/8
           - \o/
           - meet.coop is maybe back from almost dead, so we need to keep the meet.coop signup flow for now
           - ca.meet.coop is likely the next meet.coop
           - Ed will update merge request to bring back meet.coop registration
 
## [[2023-05-22]]
Here: Akshay, Eduardo, Ed ...

- Notes to future selves
    - API access issues
        - https://social.coop/@judell/110370271304116328 
            - No action needed for now?
    - spam in registrations
        - is it getting worse? the last week was bad
        - Eduardo will check in the next CWG meeting if this is an issue for others
    - wiki-alpha progress
        - issues with openid auth -- troubleshooting live :)
            - Fixed by Calix!
        - next steps
            - [[flancian]]
                - started branch for join.social.coop: https://git.coop/social.coop/tech/ansible/-/commit/5ec71ead1a1cadd95d7a74326f74fe0aae875c9e, 
                - -> https://git.coop/social.coop/tech/ansible/-/merge_requests/27
            - https://git.coopcloud.tech/coop-cloud/mediawiki/pulls/31 for coop cloud / working on it
            - [[akshay]] ideally we'd run the instance in mastodon.social.coop and do "domain magic" to have accounts still be @social.coop, but that ship has sailed
                - maybe let's try once we run bonfire or something else?
            - www is off the table
                - join.social.coop
            - user: registrations? maybe instead of site
    - sysadmin commons
        - https://anagora.org/collective-tools
        - Meeting this Thu: https://forum.meet.coop/t/commons-hour-specials-upcoming/1364
 

## [[2023-05-15]]

Here: Akshay, Eduardo, ...

- Notes to future selves
    - Started https://www.loomio.com/d/jrbG5tue/server-access/39 proposal to grant [[Calix]] server access \o/
        - This passed!
    - Mastodon upgrade
        - Akshay did it!
    - API access issues
        - https://social.coop/@judell/110370271304116328 
            - we probably need some tuning of rate limiting in general?
            - Flancian and Akshay tried to reproduce with https://gist.github.com/judell/fc50a0eb14017adb78249c941556758a and couldn't -- until actually making 300 requests
            - judell@ reported hitting this way waaay earlier though
            - Mastodon still hardcodes this: https://github.com/mastodon/mastodon/blob/46ad7fea9d67631f54dd1ef45114a08cd2c5db73/config/initializers/rack_attack.rb#L49
            - Hypothesis:
                - Maybe they're reusing the API key *or* they're making a lot of requests for the web interface?
                - And Mastodon really should handle this better, but it doesn't -- maybe all the other instances are backed by multiple servers and load-balance so the user takes way longer to hit this condition
            - Q: Is there any way to have per-user request logs in Mastodon?
            - A: no, there is not -- but we could change mastodon_log_level in roles/social.coop/defaults/main.yml to debug (it's info)
            - Next action (Flancian):
                - report back to the user, tell them what we found
                - ask optionally for an IP address so we can skip nginx logs to check how many requests the server is actually handling for them
    - wiki-alpha progress
        - issues with openid auth -- troubleshooting live :)
            - Fixed by Calix!
        - next steps
            - [[flancian]]
                - skin choice :) maybe
                - https://git.coopcloud.tech/coop-cloud/mediawiki/pulls/31 for coop cloud / working on it
                - I still need to test the latest changes in wiki-alpha; I will try to do that before the meeting tonight, or else we could do it live (tm) :)
                - if those work we'd be ready to set up wiki.social.coop using the same stack/steps. the only remaining step at that point would be to either special case the registration form path within wiki or (my preferred option) move the form to e.g. join.social.coop out of wiki.social.coop, which IMHO would make more sense?
    - sysadmin commons
        - https://anagora.org/collective-tools
 
       
## [[2023-05-08]]

Here: Eduardo, ...

- Notes to future selves
    - Started https://www.loomio.com/d/jrbG5tue/server-access/39 proposal to grant [[Calix]] server access \o/
        - This passed!
    - wiki-alpha progress
        - issues with openid auth -- troubleshooting live :)
            - Fixed by Calix!
        - next steps
            - [[flancian]]
                - I still need to test the latest changes in wiki-alpha; I will try to do that before the meeting tonight, or else we could do it live (tm) :)
                - if those work we'd be ready to set up wiki.social.coop using the same stack/steps. the only remaining step at that point would be to either special case the registration form path within wiki or (my preferred option) move the form to e.g. join.social.coop out of wiki.social.coop, which IMHO would make more sense?
    - AOB?
 

## [[2023-03-27]]

Here: Eduardo, Akskhay, Calix

- Notes to future selves
    - [x] Check that certbot is actually running in rhizome successfully if we didn't do it back in February.
        - The certificate expires [[2023-04-17]] so there's plenty of time, but certbot is not running -- certbot.service expects it in /usr/bin/certbot but it's installed in /usr/local/bin/certbot  
        - [[Flancian]] Wrote small fix that should take care of this: https://git.coop/social.coop/tech/ansible/-/merge_requests/23
        - Finally pushed this fix to rhizome tonight :)
    - Started https://www.loomio.com/d/jrbG5tue/server-access/39 proposal to grant [[Calix]] server access \o/
    - [x] Retire [[runko]], see [issue](https://git.coop/social.coop/tech/operations/-/issues/69).
        - [[Flancian]] Ed was working on it. Any concerns with decomissioning? 
        - [[calix]] since it's been down for a few weeks and nobody has complained it seems safe to tear it down
        - We actually went and cancelled it tonight -- this will take effect by April 14.
        - We thank runko for its service!
   - wiki-alpha progress
       - keycloak up with social.coop realm
       - dump restored, including images
       - issues with openid auth -- troubleshooting live :)
       - https://www.mediawiki.org/wiki/Extension:OpenID_Connect shows that the recipe needs an update to support the new way of passing parameters to pluggableauth
 
## [[2023-03-13]]

Here: Eduardo, Akskhay, Calix

- Note to future selves
    - [ ] Check that certbot is actually running in rhizome successfully if we didn't do it back in February.
    - [[flancian]] Hello from the future as of [[2023-03-11]] :)
        - The certificate expires [[2023-04-17]] so there's plenty of time, but certbot is not running -- certbot.service expects it in /usr/bin/certbot but it's installed in /usr/local/bin/certbot  
        - [[Flancian]] Wrote small fix that should take care of this: https://git.coop/social.coop/tech/ansible/-/merge_requests/23
    - [ ] Retire [[runko]], see [issue](https://git.coop/social.coop/tech/operations/-/issues/69).
        - [[Flancian]] Ed was working on it. Any concerns with decomissioning? 
        - [[calix]] since it's been down for a few weeks and nobody has complained it seems safe to tear it down
    - [x] Should we retire the [sauce](https://git.coop/social.coop/tech/sauce) repo?
        - Is there anything remaining there of interest?
        - Some canned SQL queries
        - [[calix]]: proposal: archive the repo
        - [[Flancian]]: yes!
        - [[Akshay]]: Let's add a link to the ansible repo in a README first?
        - [[Flancian]]: yes!
        - https://git.coop/social.coop/tech/sauce/-/merge_requests/20
        - ARCHIVAL COMPLETE 🎉
    - [ ] Port wiki-dev to our shiny new coop cloud mediawiki instance [wiki-alpha](https://wiki-alpha.social.coop/) see [issue](https://git.coop/social.coop/tech/operations/-/issues/66) for details.
        - [[Flancian]] I discussed migration paths with the [[wiki builders]] chat and the easiest way forward is probably to declare maintenance for our wiki (including registrations?), bring it down and bring up mediawiki on wiki.social.coop during that window.
        - Please review https://git.coop/social.coop/tech/ansible/-/merge_requests/24
        - calix (they/them) dice: https://doc.traefik.io/traefik/routing/routers/#priority
        - calix (they/them) dice: https://doc.traefik.io/traefik/routing/overview/
    - Now that we have [[coop cloud]] on [[hypha]], which services would we like to run there as experiments?
        - Matrix?
        - SSO?
            - Bonfire?
            - Do we want a dedicated SSO provider or to piggyback on a Fediverse instances?
            - [[keycloak]] would be the go-to here probably: https://recipes.coopcloud.tech/keycloak
            - Could we have a migration path were we move people gracefully from Mastodon to some other auth provider?
                - [[Calix]]: Possible, bit long shot!
    
## [[2023-02-27]]
- Note to future selves
    - [ ] Check that certbot is actually running in rhizome successfully.
    - [ ] Try to get something running on coop cloud in hypha if we haven't by now.
    - [ ] Restore a backup from s3 somewhere, or at the very least decrypt it!
    - [ ] [hetzner console] Decommission runko.

## [[2023-02-13]]
- Location: https://meet.mayfirst.org/social-coop-tech
- Time: 19:00 – 20:00 UTC
- Attending: Akshay, Tod, Eduardo, Ed
- Check ins
    - Eduardo: originally from Argentina (near Buenos Aires), now in Zürich
    - Akshay: originally from India, now in Berlin
    - Tod: based in Utah
- Cleanup: 
    - [x] [runko] Run certbot commands to revoke the previous certificates.
        - Not needed, actually could be harmful as we copied the certificates.
        - Instead we should check that certbot is successfully renewing, moved to future agenda.
    - [x] check that backups work
        - They don't :)
        - Trying to fix it now, got all the way to setting up timer and fixing pg-dump-to-s3.service (prune was failing as we have a new server which means a new path in s3).
    - [ ] [hetzner console] Decommission runko.
        - Any blockers? None known?
        - It's been off for a week.
        - Let's proceed.
    - [ ] remove sauce from git.coop?
- Maybe upgrade to 4.1?
    - Let's try to use [[tmate]] to share terminal and do this together?
    - Flancian sharing terminal
    - Let's accept Ed's pull request in [[ansible]] repo: https://git.coop/social.coop/tech/ansible/-/merge_requests/22
      - Done!
      - Open question is whether we need the assets:precompile step or, as the release notes seem to imply, we can skip because we're using the prebuilt images?
      - We removed the precompile in the end.
    - Done!
        - Always run `--check -vv --diff` before going live
        - This time it prevented us from having another DEEPL outage because of a mismatched collection version in [[ansible galaxy]]
    - Issues we ran into
        - Had to run `export PASSWORD_STORE_DIR=~/.password-store/social.coop` (this depends on where you put your password store)
        - Had to run `ansible-galaxy collection install -r requirements.yml` in ansible directory
- Tod: what about mediawiki migration?
    - Next steps
        - Make sure that [[coop cloud]] is running successfully in server [[hypha]]
        - Install [[mediawiki]] using coop cloud in [[hypha]].
            - https://recipes.coopcloud.tech/mediawiki
        - Take a database dump in wiki-dev (Flancian and jonny have access for now)
        - Restore database from wiki-dev.
        - Or alternatively rsync the whole thing ;)
        - Install extensions (which should be a matter of syncing the [`LocalSettings.php`](https://www.mediawiki.org/wiki/Manual:Configuration_settings) file)
            - Ed: maybe coop cloud has a way to manage plugins in mediawiki?
    - Open questions
        - Does abra make it so that we don't need ansible?
            - Likely.
        - Cloud init should be able to seed a machine with docker/docker swarm.

## [[2023-01-30]]
- Location: https://meet.mayfirst.org/social-coop-tech
- Time: 19:00 - 22:00 UTC
- Attending: Flancian, Akshay, Ed, Calix

We agreed on 2022-01-23 to schedule a maintenance window to test the database restore on Hypha (our new Hetzner server). If all goes well with the restore and testing we may decide to leave it running there.

- Join [[tmate]] for watching: (elided)

This checklist was copied from a comment that Akshay put in a GitCoop [issue](https://git.coop/social.coop/tech/operations/-/issues/65#note_20050).

- [x] [cloudflare] Reduce TTL for `A` record for `social.coop` to something like 300. 
- [ ] [runko -> rhizome] perform manual copy tasks not covered by ansible 
    - [x] /etc/letsencrypt/*
- [x] [runko] Put social.coop in maintenance mode.
    - 2023-01-30 19:18 UTC social.coop in maintenance mode
- [x] [runko] Stop sidekiq and mastodon containers on runko.
- forking paths :)
    - path 0: full backup and restore
        - [ ] [runko] Backup postgresql.
            - wiki says `systemctl start pg-dump-to-s3.service`
        - [ ] [runko] Backup elasticsearch.
        - [ ] [runko] Backup redis.
    - path 1: down services and try rsyncing everything
        - [x] down services
        - [x] rsync everything :)
            - rsync -avh /opt/social.coop/var/ /opt/social.coop/var/
            - rsync -avh /opt/social.coop/sauce/docker/elasticsearch/ /opt/social.coop/var/lib/elasticsearch/
- [x] commented out sidekiq, web and streaming
- [x] [localhost] Run rhizome playbook from https://git.coop/social.coop/tech/ansible/-/merge_requests/21. (Mastodon will most likely not come up due to DB not having been setup.
- [x] [rhizome] explicitly stop mastodon and all sidekiq containers. 
- if we did path 0:
    - [ ] [rhizome] Restore postgresql.
    - [ ] [rhizome] Restore elasticsearch.
    - [x] actually did path 1
- [x] [rhizome] Start all containers
- [x] [cloudflare] Change `A` record for `social.coop` to point to rhizome, make sure TTL is small to help us revert if needed.
    - [ ] done at 2023-01-30 21:06 UTC
- [x] [localhost] See if social.coop works.
- [x] [localhost] See if wiki.social.coop works.
- [x] down runko
- [x] merge https://git.coop/social.coop/tech/ansible/-/merge_requests/21/commits

Cleanup: 
- [ ] [runko] Run certbot commands to revoke the previous certificates.
- [ ] check that backups work
- [ ] [hetzner console] Decommission runko.
- [ ] remove sauce from git.coop?

### log
- If postgre
 
## [[2023-01-23]]

- Location: https://meet.mayfirst.org/social-coop-tech
- Attending: Flancian, Akshay, Ed, David Vasandani, A Late Calix
- Check-ins
- Issue with emails bouncing?
  - https://git.coop/social.coop/community/operations/-/issues/1212
  - It looks like an issue with zoho?
  - Or it could be we need to update an SPF record in DNS, we should look for updated instructions from Zoho.
  - Try: https://www.zoho.com/mail/help/adminconsole/spf-configuration.html
  - Done, maybe this works?
  - Also try: https://www.zoho.com/mail/help/adminconsole/dkim-configuration.html
      - Maybe next time?
- Mediawiki deploy in hypha
  - [[mediawiki bug]] https://git.coop/social.coop/tech/operations/-/issues/66
  - F: `sneakers the rat` is working on this
  - David: is there an answer to the question of whether the mediawiki install was done with ansible/coop cloud or full manual?
  - Ed: unsure but he was interested in changing how we do the setup.
  - Flancian: happy to sync with jonny about how this was done and how we could move forward with e.g. coop cloud.
  - Calix: happy to help!
- Registrations flow / cross dependency with wiki
    - Easiest might be to just leave the node.js app running now, maybe move it to e.g. forms.social.coop and post there
    - We could run the whole thing -- just the form and the handler in registrations.social.coop
    - ... and remove the existing wiki content once the new wiki is up a wiki.social.coop
- Rhizome deploy?
    - Next action?
        - Akshay: we need to figure out how we're going to do the database migration
        - Default: dump, maintainance window, restore. Yes, let's do this.
    - Care for not double-federating?
        - We could start just with postgres and not bring up mastodon web interface in rhizome for now; this seems like the first step and it should be safe
    - Can we bring up only postgresql in rhizome with ansible?
        - Maybe it's best to disallow outbound/inbound traffic and just use the standard docker compose file?
        - Could also just configure mastodon not to federate.
        - We can just make sure that docker-compose only brings up postgresql.
        - **New open question ^**
        - Let's do this next Monday slightly earlier by default?
        - Let's do Monday [[2023-01-30]] at 19 UTC
    - David: are we going to run postgresql in docker?
        - Yes, same as currently

## [[2023-01-09]]
- Location: https://meet.mayfirst.org/social-coop-tech
- Attending: Akshay, edsu, David Vasandani, Calix, Flancian
- ...agenda items here...
- Check-ins
    - Happy New Year! 🎆
    - Akshay: doing well, worked today. Had call with friends, cooked, busy day :)
    - edsu: doing well, had a few weeks off which was really nice. Happy to see progress! Went to the dentist today.
    - David: California is experiencing very crazy weather. It's getting pretty bad (power cuts, 90% under flood). Focusing on family time and movies.
        - Akshay: can recommend [[Glass Onion]].
        - David: can recommend [[Knives Out]].
    - Calix: doing OK, quiet New Years. Half Marathon on New Years even, then pushed it a bit far and got injured :(
        - Just got another round of funding for [[coop cloud]]. A benefactor has funded fixing usability issues and the federation component.
        - Moving to a more participatory decision making process with other parties.
        - Started with [[autonomic]], but there are several other groups collaborating.
        - #push [[coop cloud]]
            - https://coopcloud.tech/blog/new-year-status-update/
            - https://coopcloud.tech/blog/federation-proposal/
    - Flancian:  
        - Nice NYE social event after many years not feeling like that. Refreshing!
        - Big milestone in getting Agora chapter finished https://anagora.org/go/agora+chapter
        - 6am page today but at least interesting. Early night tonight!
- Aside: quality issues with meet.mayfirst.org
    - Pixellation, disabled feeds 
- [[Akshay]]'s work on [[Ansible]] for rhizome: https://git.coop/social.coop/tech/ansible/-/merge_requests/21
    - can @3wordchant be added to the repo please 🙏
        - (edsu added them 🎉)
    - +1 from davidvasandani
    - [[akshay]] 
        - on the [[sauce]] repository:
            - meant originally for things that were to be copied to runko, e.g. systemd services.
            - focusing on applying the right components to bring up mastodon and postgres.
            - while doing this realized that sauce was *not* up to date, so did a sync.
        - on [[ansible]]:
            - automated deployment of sauce!
            - PR above does that.
            - includes certbot and certbox specific nginx config.
            - moved datadog password from ansible vault to pass store, `lookup('passwordstore'...)`. we can use this for everything, instead of needing 2 systems
            - social.coop/defaults/main.yml is where a lot of the parameters for our configuration now are, including everything mastodon (database, s3 buckets, etc.)
            - replaced 'docker-compose' with 'docker compose' invocations, as the earlier is deprecated/removed in new versions.
            - added datadog logs parameters to docker-compose, but they aren't used by default (require further configuration)
            - created an env file for postgres (to pass the password)
            - a certificate is generated first, that is needed so nginx can start; this runs once as it's set up to check for existence of a file
            - also added wiki.social.coop configuration.
            - nginx is a *module* -- actually a git submodule which is in roles-external (need to `git clone --recurse-submodules`)
            - rhizome.playbook.yml exists
        - [[open questions]]
            - whether to use secrets the way the wiki has them in the rhizome playbook, or the other way (which risks people using prod secrets in their test environments)
            - whether to use PASSWORD_STORE_DIR or include a social.coop/ prefix for every pass.
            - how to do the actual migration to rhizome once it's set up.
        - [[calix]] would any of these changes affect the mastodon upgrade process?
            - [[akshay]] we'd need to automate some of the migration steps; currently docker compose config doesn't include this.
            - when we restart mastodon, we restart everything -- including elastic search, postgres. we need a more granular way to restart things.
        - [[next steps]]
            - set up alpha.social.coop in rhizome using this?
            - it would use a distinct s3 bucket, Akshay 
            - write a shell script or 'manual playbook' of the ansible commands we'd run
- Experiments with coopcloud.tech (davidvasandani, 3wc, protean)
    - David:
        - abra is the coopcloud cli
        - after you have a server set up, you add it to the abra inventory
        - then through the CLI you add [recipes](https://recipes.coopcloud.tech/) -- you can get these from a page. docker-compose files but set up for docker swarm.
        - these commands are all run locally. it's an ansible-like model; we could probably migrate away from ansible.
        - David would like to point a config to a server and have it be end-to-end setup.
    - Flancian: so abra could replace our use of ansible?
    - Akshay: we would still need to install docker-swarm?
    - David: yes & no; abra has a provisioning step.
        - it uses [[cloud-init]] -> https://cloudinit.readthedocs.io/en/latest/.
        - we could still use ansible though -- and ansible is very good at e.g. user management
    - Flancian: maybe we could run this in [[hypha]]?
        - David: would highly recommend we do this
        - We wouldn't be 'locked in' based on the recipes -- and the recipes are high quality and we could contribute back!
        - [[calix]] in autonomic we were using ansible for provisioning services and users and using coop cloud for app deployment and maintenance, but there is a project to move away from the abra cli even: [[wiki cafe]] ~ https://wiki.cafe
        - [[calix]] how much do we need to consider the "beach factor" (how many people does it take to go to the beach before you forget how to do things) when thinking about the approach. there's been some turn over in TWG people, and knowledge transfer has proven difficult. 
        - David: running an experiment with the abra CLI should be straightforward; biggest issue was how abra installs everything in a single machine.
        - We could work with a 'share development' setup.
        - Calix: https://docs.coopcloud.tech/operators/handbook/#sharing-abra
        - Calix: the other alternative is to have abra installed in the server, but there's a footgun: people might forget to commit to git more easily.
- Mediawiki experiments (edsu)
  - Maybe use coopcloud? https://git.coopcloud.tech/coop-cloud/mediawiki/
      - Definitely :)
  - [[social.coop wiki builders]]
      - [[nathan]] and [[sneakers-the-rat]] started experimenting with mediawiki.
      - it's running on a server somewhere: wiki-dev.social.coop
      - running [[semantic media wiki]]
      - -> [[hypha]]
- On the complexity of running databases in containers (Akshay)
    - David: agree but the tradeoff (flexibility) might be worth it
    - We might also just want to special case database even if we go with [[abra]]
- For next time:
    - Identity management with keycloak?
    - moa.party early-stage proposal (flancian)
    - Nextcloud access for other [[working groups]] (flancian)
      - Possible alternative policy: we batch create accounts for all WG members proactively and DM them their passwords? ideally over Matrix
      - This is old, maybe not needed anymore? As the current way of creating accounts seems to be working.

## [[2022-12-19]]
- Attending: Dan, David Vasandani, Akshay, Eduardo (flancian), Ed (edsu), LibreEquity, Calix (3wordchant)
    - Dan: upstate New York
    - (round of introductions)
- Check ins
    - Dan: wrote a draft on Mastodon Verification for the publication they work with. [[rel equals me]].
    - Akshay: been away for >1mo, was in vacation (to India!) and travelling (now in Italy!). One more week of holiday left! May have time to dedicate to social.coop.
    - Ed: been kind of sick / with the flu. Otherwise going well and into vacation mode until EOY! Open to do coworking.
        - Nextcloud calendar for coworking?
    - LibreEquity: doing well, very interested in the Twitter -> Mastodon move. Read Nathan Schneider's book in 2014-2015, followed him back then and had this in the back of our mind.
    - David: life is good, kids are healthy :) Getting warmer (in US). Diving into monitoring. Grafana, using docker, learnt a lot.
    - Calix: doing alright :) Neat people starting at autonomic.
    - Eduardo: entering production freeze, feeling nice about it :) also re-re-finishing (THIS TIME FOR REAL (tm)) [[agora chapter]].
- Location: https://meet.mayfirst.org/social-coop-tech
- [Grafana](https://grafana.com/) analysis (davidvasandani)
    - Sharing screen.
    - Hacked around for the last few weeks. Last experience with monitoring/debugging/logging was a few years back. Main intent was to explore modern options in the monitoring/debugging/logging space.
    - Loki: tool for logging.
        - Taskfile is like a Makefile but in YAML.
    - Prometheus: Borgmon-like :) Gathers data.
    - Grafana: UI layer? Frontend for Prometheus.
    - docker-compose files for the whole stack. Will add this to a repo in git.coop.
    - statsd, fluentd.
    - Open question: homegrown docker-compose long time or [[coop cloud]]/[[abra]]? Is this a choice or are they complementary?
    - Akshay: use the same stack pretty much at work. You can configure loki to store logs somewhere -- like an S3 bucket -- (and that way you do not need extra indexing infra?).
    - David: we pipe things through fluentd to consolidate logs.
    - David: [[datadog]] can get expensive with one wrong logging statement :)
    - [[Calix]] https://git.coopcloud.tech/coop-cloud/monitoring https://git.coopcloud.tech/coop-cloud/monitoring-lite is the coop cloud
    - Flancian: is this the kind of stack that we could run in Rhizome now?
    - Akshay: would recommend we run monitoring in a separate server, because.
    - Ed: is the goal of this to be able to detect emergencies?
    - David: Grafana supports setting up alerting.
    - Akshay: Alert Manager is provided by Prometheus as well as an alternative.
    - Next steps?
        - Flancian: could we install this monitoring stack in [[hypha]]? ;)
            - Seemingly yes, seems like a good idea.
            - David: any concerns with network traffic? Would like to have someone else try it out, and then work on deploying it. We would need something installed at the system level and/or docker level (on runko)
                - Let's monitor it ;)
            - Next action: **open a bug in [[go/twg/bugs]]**
- New server [[Rhizome]]! (flancian)
    - rhizome.social.coop
    - ubuntu 22
        - plus: `addgroup wheel`
        - everyone should have access, if not reach out
    - reach out for server access or raise hand
    - Flancian: unclear on whether we want to target coopcloud.tech
    - David: I don't think we should hold up the upgrade when exploring coopcloud.tech
    - Akshay: on the RAID 0 -> 1 change
        - Discussed pros/cons of RAID 1
        - Any negative impact should be negligible
    - **Next action: continue to bring up docker/docker-compose services as per runko**
    - **Cut bug**
- Single Sign On experiments / future work? (edsu)
    - Mastodon SSO discussion
    - David: Mastodon does not by default surface your email, but with a simple change in a test this was surfaced
        - But if you change your email in Mastodon, the other services do not know that you are the same user and consider you a new one.
        - Flancian: do other SSO providers not have this issue?
        - David: unclear.
        - Akshay: [[SCIM]] calls are sometimes used to ping around this kind of data/event.
            - -> [[scim for keyclub]]
            - Not all software supports it. Does [[dokuwiki]] even actually support email changes?
        - Edsu: dokuwiki uses the email and it might not support this.
            - Nathan Schneider came to the conclusion that we might want a stand alone SSO provider?
            - But we already have >1.7k users in Mastodon.
            - Calix: +1. This might be a limitation of dokuwiki -- other wiki systems have a username in the schema. Mediawiki for example.
                - Short term paths:
                    - 1. provide a fake email address to dokuwiki?
                    - 2. pick another wiki software?
                - Edsu: +1, there was a lot of uncertainty in the wiki software discussion. dokuwiki is still at the experiment phase.
                - https://git.coop/social.coop/tech/operations/-/issues/53 is the source of truth for this.
        - Next actions:
            - David: Decide if we want SSO, and if we want a *stand alone* SSO. 
            - David: [[keycloak]] might provide a way to have a separate SSO
        - Akshay: have some friends who migrated from Mastodon to Keycloak :)
        - Calix: would like to pick your brain sometime :) Were password resets required?
        - Akshay: no.
    - Calix: screensharing.
        - Issue with the sign in dialog in Hometown/Mastodon when two login providers are enabled.
        - We should go all-in, no dual login.
    - Flancian: question about the issue we're trying to work around.
        - Patch is one line to add the email field in responses, could be mounted as a volume patch in docker-compose.
        - But it would increase maintenance.
        - Calix: note that dokuwiki doesn't use this email field except for sending notifications, could we poll folks on preferences between disabling that vs. login system churn.
        - It might indeed make sense to patch dokuwiki instead of patching xMastodon, given that the earlier is less critical (and a newer service).
        - David: does this maybe depend on which other services we want to run?
        - Calix: yes, not only the number but also whether they use the email field the same way, or if they are based on username.
        - LibreEquity: is social.coop running an email server?
            - Flancian: nope, using webarchitechts forwarders set up on request
- NEXT EPISODE:
- Nextcloud access for other [[working groups]] (flancian)
  - Possible default policy: we batch create accounts for all WG members proactively and DM them their passwords? ideally over Matrix
- Experiments with coopcloud.tech (protean)
- Chat log dump follows:
Dan says:I like jitsi better than bbb 
David Vasandani says:( * ^ *) ノシ 
calix (they/them) says:dang this is a pleasantly large group! 🥰 
me says:
https://doc.anagora.org/social-coop-tech-group?edit for notes 😃 
Dan says:I'm on Firefox! 
Dan says:(I use the Nightly build) 
calix (they/them) says:it's -9°C here today 🥶 
Dan says:wow that is v cold! 
calix (they/them) says:👍 
David Vasandani says:👍 
Dan says:a previous Mastodon article I helped out with 
https://themarkup.org/the-breakdown/2022/11/21/we-joined-mastodon-heres-what-we-learned-about-privacy-and-security
calix (they/them) says:
https://git.coopcloud.tech/coop-cloud/monitoring
calix (they/them) says:
https://git.coopcloud.tech/coop-cloud/monitoring-lite
calix (they/them) says:think it's the same stack? 
David Vasandani says:@calix it does look to be the same! 
David Vasandani says:I believe the only difference is I put fluentbit between the service and loki. 
calix (they/them) says:👍 
calix (they/them) says:👏 
me says:
rhizome.social.coop
edsu says:👏 
Dan says:unrelated but I have some affiliation with an NYC org 
rhizome.org
LibreEquity says:RAID0? 
edsu says:brb 
edsu says:Here's an issue where I wrote down some notes on the dokuwiki/mastodon sso experiment: 
https://git.coop/social.coop/tech/operations/-/issues/53
Dan says:"hey are you talking about mastodon?" –my 3yo 
calix (they/them) says:🤣 
edsu says:lol 
LibreEquity says:👍 
edsu says:😀 
LibreEquity says:😀 
David Vasandani says:Great point! 
edsu says:I disabled that dual login in the dokuwiki -- agree 
David Vasandani says:Thank you for that call out. 
edsu says:💯 
calix (they/them) says:oh and for completeness we hid the username/password fields in CSS 🕵 
calix (they/them) says:
https://github.com/cosmocode/dokuwiki-plugin-oauthdoorkeeper/compare/master...edsu:dokuwiki-plugin-oauthdoorkeeper:mastodon
David Vasandani says:Never be sorry! 
David Vasandani says:Not everyone has an alias. 
David Vasandani says:It by request. 

## [[2022-12-05]]
- Attending: jotaemei, edsu, protean, davidvasandani
- location: https://meet.mayfirst.org/social-coop-tech
- protean: bonfire instance
  - https://magpie.place
  - running bonfire community; some upstream issues w/ bonfire (e.g. mail + mailgun)
  - good support in bonfire chat
  - goal is to find something that has more governance built into the same plaform; we have difficulty getting everyone on all the platforms (loomio, matrix, git, etc) would be good to have governance folded in. 
  - there doesn't appear to be voting built in, but since it is modular it should support writing an extension
  - if anybody wants to take an account feel free ; just look for confirmation link in your spam
      - ~~@davidvasandani just created an account but didn't get an email.~~
      - @protean shared and link and @davidvasandani was able to access.
  - participation rate is like 15%-30% of people who are loomio, and people who are on loomio is 50% of active mastodon
  - did a poll for translation feature, some people said thank you for doing it that way
  - jotaemmei: sometimes I don't vote because I see that something is going to pass
    - if loomio is asking people to jump through too many hoops we should re-evaluate
    - how do we make sure we accomodate people's attentional needs
    - this is a larger issue with the larger confederation of co-ops, but it is an issue even internal with social.coop
    - some people have signed up to do bridging work, but it's unclear how to manage it going forward    
- [[flancian]] should we reboot runko at some point? :)
-- [ ] Yes we should! let's schedule that for Friday 2022-12-10
- follow up on issues in [bug tracker](https://git.coop/social.coop/tech/operations/-/issues)
    - [#52](https://git.coop/social.coop/tech/operations/-/issues/52) - Datadog Agent
        - Do we have an account? Yes, info is in the pass.
        - Plan size?  
        - Access?
        - protean: there was no systemd service to start datadog,
          - got it working again, and added logging
          - not connecting to redis and elasticsearch because it's not running in those docker containers
              - @davidvasandani can help configure if we'd like to mornitor.
        
          - we need to decide whether we want to keep using it, someone mentioned prometheus?
              - @davidvasandani is testing Prom, Grafana, and Loki locally for monitoring Mastodon.
              - We can discuss the pros and cons of build vs buy and what our objectives are without getting too technical. 
    - [#56](https://git.coop/social.coop/tech/operations/-/issues/56) - Experiments Server
        - Currently setup on Hetzner (hypha)
        - Is there interest in full E2E automation and testing of new versions and restoring from backups?
        - Does the group use or have experience with Terraform?
        - If there's interest @davidvasandani would like to run point on creating the automation and running some pairing sessions.
    - [#53](https://git.coop/social.coop/tech/operations/-/issues/53) - Setup Dokuwiki
        - Test setup on hypha? (Hetzner experiments server)
        - Has someone picked up this ticket? Can @davidvasandani pick this up? (might want to touch base with @flancian) 
- new server!
-- we have the go ahead to use up to $250 per month
-- should select a server and put to a quick loomio checkin/vote
- protean: opened the log retention issue on loomio
  - https://www.loomio.com/d/kXMdf0ZW/privacy-policy-log-retention-and-anonymization
  - jota: what do we have now for a privacy policy?
  - protean: it links to the code of conduct at the moment
  - jota: there are questions of jurisdiction that I was hoping the legal working group could help address
  - protean: i want the lawyer people to provide guidance here
  - protean: i posted a draft text about what we are currently doing
  - protean: there is .env configuration to scrub login information we could think about doing 
- david: would there be interest in moving to using something like terraform for provisioning the Hetzner machines? that way we could bring up experiments and tear them down easily.
  - there was general agreement that this sounded like a worthwhile thing to look at
  - david is going to set up a time for the TWG to discuss how we want to evolve our infrastructure code
- schedule and announce the next meeting time
  - moving to bi-weekly meetings, that meet a bit later for Bo, and hopefully are still doable by flancian?
- re: AWS/Azure 501c3 grants
    - social.coop is not a 501c3 and the overhead of creating one or using someone elses didn't seem feasible

## [[2022-11-28]]
- Location: https://socialcoop.meet.coop/dav-y3e-c21-sgv
- Attending: edsu, protean, flancian, davidvasandani, dphiffer
- Check ins
    - Edsu: working from home every day
    - Flancian: working from home *today*
    - Ian: playing with monitoring
        - added live process monitoring
        - hooked up logging
    - dphiffer: is here :) was lurking during updates
        - welcome!
        - in Troy, NY north of Albany
        - WFH for a non profit
    - david vasandani: member of social.coop for a long time but now looking to get more involved :)
        - as long as he can with two kids ;)
        - software engineer with a focus on aws
        - has set up a local dev environment with docker
- Agenda seeded from last time / during the week
    - [[ian]] logging and monitoring
        - we may want to spend money here ([[datadog]])
        - security logging, log retention come with a charge
        - may offer plans for non profits
        - we could:
            - add the feature, run it for a month, then write a proposal with the actual numbers in hand
    - [[edsu]] emails from [[logcheck]]
        - they look somewhat noisy/useless
        - [[ian]] the software is sort of ancient, we should probably get rid of this
        - [ ] let's open a bug to disable it
    - 'sauce' git repo
        - https://git.coop/social.coop/tech/sauce
        - what should go into tech/operations, and what into ansible?
            - [ ] check now, per directory, and make a call? :)
            - systemd services -> ansible role
        - maybe we want to keep in the ops repo what we want to bring into the server (with a git clone/pull)
        - maybe there is some utility to it? anybody wants to make an argument in that direction?
            - none known
        - [[ian]] systemd services and timers which were in ansible were all broken when found last week during updates; now are fixed
            - two issues hit us
                - backup: bad dependency -- timer services was wanted by pgbackup target, but there was no such target
                - the ones in the sauce repo: you need to make sure that a timer is 1. enabled and 2. started -- one of those was missing
        - [ ] open bug to track this action
    - [[ian]] let's revisit how we add documentation so we're all in the same page
        - social.coop/general?
        - [[edsu]] that's the idea, yes.
            - put a revision history for the ops wiki in a [git bundle](https://git-scm.com/docs/git-bundle)
        - pending: 
            - merge request
            - delete old wiki pages
            - leave a README behind that points to the One True Wiki
            - remove duplication within the pages we moved
    - revisiting last week's upgrade
        - what should we do differently next time?
        - have we updated documentation sufficiently? where? :)
            - this has not happened and it should -- where should it go?
            - somewhere in social.coop/general? or along with the code?
            - let's go with along with the code, and leaving a pointer to it in the general wiki.
            - [ ] retire (or update) https://git.coop/social.coop/general/-/wikis/tech-working-group/Deploying-Runko
    - next steps for Mastodon upgrades
        - v3.5 -> ?
        - this has already been done by protean :) we're on v4
    - [[backups]]
        - either they were happening some other way, or they weren't happening
        - postmortem
            - backup timer didn't have WantedBy=timers.target
    - [[postgres]]
        - shouldn't be listening on the external network?
            - we were binding to localhost though
            - we are using other processes that connect to the database directly
        - [ ] can we go back to password auth?
        - [[david vasandani]] where are the processes running that are connecting to the postgres instance?
            - [[ian]] they are running locally in runko
            - these are not public to the internet -- they are just on the 'external' docker network
        - [[david vasandani]] should we set up a separate meeting to talk about tech roadmap level things, or use this meeting?
            - this meeting should be a good forum.
            - [[ian]] also a lot of this discussion is advancing well in the matrix chat rooms.
            - [[edsu]] a lot of these are bound up with what social.coop (the larger group) wants to do, we should take care not to over-focus on the tech aspects only
            - [[david]] thinking mostly of incremental improvements to our current stack
                - [ ] testing database restores
                - test environments
                - which improvements do we want to prioritize?
                    - https://anagora.org/mastodon-upgrade might be reusable / something to bootstrap on for a roadmap level document
        - we should revisit .env in docker directory.
            - why did we write this? :)
            - no obvious issue here
            - security model: only root can read
    - [[reliability]]
        - how having two servers increases reliability, and having three servers increases it more :)
        - [[ian]] going to start a new instance, run it as an experiment and report back
        - [[flancian]] was thinking of the same / similar
        - [[david vasandani]] what's the advantage of these experiments w.r.t. reliability? also, two servers might not affect reliability in the positive direction.
            - (...)
            - [[ian]] on the parallels between the fediverse now and email 20+ years ago. Things got hard with running your own email because of spam. There's no reason to believe that this won't happen with the fediverse, if we just let it go. People will start to demand more moderation policies, if people don't want to be on your instance because people aren't federating with you, there will be re-centralization.
            - on Ian's experiment: if we're going to combat the previous, we need some way of maintaining the distributed aspects of the network. This requires instances to agree on codes of conduct, standards for handling signups.
                - aside: could social.coop scale up to ~50k people with loomio?
                - -> we need an instance that can self-govern.
            - [[dphiffer]] proposed to union local that they run an instance.
                - but what does it mean for one coop to be a member of another coop?
                - [[ian]] it might or might not make sense depending on how the instances operate; for example higher level coops could vote on higher level rules on how associated instances federate.
                - lack of good tools for content moderation is a problem.
                    - the fediverse currently has only hashtags to have distributed decision making on e.g. blocking
                    - a coalition of federated instances could do better; they could agree for example
                    - [[flancian]] we could also imagine extending the ActivityPub protocol to support sharing this information between instances; this is something the fediverse needs to solve if it's going to scale
    - [[cloudflare]] / [[dns situation]]
        - [[mayel.space]]
        - solved \o/
    - [[ian]] posted a poll about translation feature
        - are people interested?
        - we would fit in the free tier of [DeepL](https://www.deepl.com/translator)
            - plan:
            - add a couple of new variables in the env file
    - [[david vasandani]] on [[cloud grants]]
        - have we considered or previously applied for the annual grants that AWS ($1k) and Azure ($3.5k) offer?
            - never happened as far as we can tell
            - loop in Nathan Schneider
    - [[flancian]] should we reboot runko at some point?


## [[2022-11-21 18:00 UTC]]

- Location: https://socialcoop.meet.coop/dav-y3e-c21-sgv 
- Attending: 3wc, edsu, protean, flancian

- Mastodon upgrade!
    - led by protean@
- Check in
    - @Flancian: Happy after weekend playing with containers. Way fewer (late) meetings because of thanksgiving.
    - @Edsu: starting week happily.
    - @Protean: working on not taking down the site today ;)
    - @3wordchant / @3wc / Calix: doing well, happy to have an individual account in social.coop now :) ran in the rain yesterday (pleasantly) and have had an interesting day so far (ethical wise).
- Meta
    - Should we use the raise hand button today?
        - Yep
        - Yep
        - On it :)
    - Do we want to screenshare?
    - Where do we want to put learnings from today?
        - Currently we had some instructions in https://git.coop/social.coop/tech/operations/-/wikis/infrastructure-overview#mastodon-upgrades
- Open questions
    - How to copy static assets so they can be served by nginx
        - protean@ might have found the right incantation
    - Should we be concerned about disk space?
    - How to put mastodon in maintenance mode
        - touch /opt/social.coop/var/www/maintenance_mode_on

- Steps that @protean put together for the upgrade

```
sudo touch /opt/social.coop/var/www/maintenance_mode_on

sudo docker-compose stop web streaming sidekiq sidekiq-scheduler sidekiq-default-q sidekiq-push-q sidekiq-pull-q es

sudo systemctl start pg-dump-to-s3.service

sudo docker-compose exec db vacuumdb  -U postgres --all --full --analyze --verbose

sudo systemctl start pg-dump-to-s3.service

# validate that the backup is in the bucket and that we are able to retrieve it, otherwise move manually to [[hypha]]

sudo docker-compose exec db pg_dumpall -U postgres > ../../var/lib/postgresql/9.6.backup

sudo docker-compose down --remove-orphans

sudo git checkout 3_5_upgrade

sudo docker-compose up -d db

sudo cat ../../var/lib/postgresql/9.6.backup | docker-compose exec -T db psql -U postgres

sudo docker-compose logs -t db

sudo docker-compose run --rm -e SKIP_POST_DEPLOYMENT_MIGRATIONS=true web rails db:migrate

sudo docker-compose down --remove-orphans

sudo docker-compose up --scale sidekiq-pull-q=4 --scale sidekiq-default-q=12  --scale sidekiq-push-q=4 -d

sudo docker-compose run --rm web bin/tootctl cache clear

sudo docker-compose run --rm web rails db:migrate

sudo docker-compose down --remove-orphans

sudo docker-compose up --scale sidekiq-pull-q=4 --scale sidekiq-default-q=12  --scale sidekiq-push-q=4 -d


Done


==ROLLBACK==


sudo docker-compose down --remove-orphans

git checkout rebuild

sudo docker-compose up --scale sidekiq-pull-q=4 --scale sidekiq-default-q=12  --scale sidekiq-push-q=4 -d
```

## [[2022-11-14 19:00 UTC]]

- Location: https://socialcoop.meet.coop/dav-y3e-c21-sgv 
- Attending: 3wc, edsu, protean, flancian
    - These will be crossposted to [[go/twg/minutes]].
- Default agenda
    - [[check ins]]
        - (done, all well)
        - welcome back [[ian]] ~ [[protean]] was last active in 2018, tuning back into fediverse 
            - Ian brings back a big chunk of context from the time were Mayel and Victor (sp?) were calling it quits
            - Ian and the Two Nicks, did a transition already -- knows where are the things that you need to know if you want to get anything done.
    - suggested topics follow, please add more :)
        - [[documentation]] source of truth
            - [[big documentation reorg]] took place thanks to Ian, Nathan also did some improvements
            - default: [[go/twg/wiki]]
            - how we understand how wiki works:
                - [[edsu]] [[ansible repo]] checks out [[general.wiki]] and [[wiki.social.coop]] repos, massages them and deploys them to [[runko]]?
                - [[edsu]] there's a web hook (in one or both? unclear) when you commit to the wiki, documented
                - [[flancian]] I keep not remembering what goes in general.wiki and what goes wiki.social.coop
            - report back to https://www.loomio.com/d/2Rwh5z3H/time-to-consolidate-wikis- (as per [[nathan schneider]]'s request.)
                - how we understand the proposal:
                    - option one: consolidate (move) twg.wiki (tech/operations repo), cwg.wiki (community/operations) into general.wiki, which gets processed and deployed from ansible?
                    - option two: change [[ansible playbook]] to also check out the twg and cwg wikis and somehow integrate them at deployment step
                - pros/cons of these approaches
                    - do we want to keep anything in the wiki secret?
                        - [[ian]] there might be a grey area for things like management interfaces (URLs), but by and large the right default option is public
                        - things that keep your logs clean
                    - some documentation lives with the ansible repo as well
                    - any pros to option two?
                    - cons: makes linking between repos more difficult, [[edsu]]: it's nice to think of it as one knowledge base
                    - **[[default]]: we'll report back that we'll consolidate into [[general.wiki]]**
        - [[operations]] source of truth for our tech group work
            - nine repositories currently, counting three wiki
            - [[flancian]]: I'd like to designate one repository as 'clone this first' and add a ./bootstrap-local.sh script which clones all social.coop repos to begin with.
            - [[flancian]]: then work on ./bootstrap-prod.sh :)
            - [[flancian]]: what's the best repo for that? is it [[ansible]] because of how we want to use automation for this, in particular for ./bootstrap-prod.sh?
            - flancian: originally thought tech-operations but maybe ansible?
            - [[protean]] ~ [[ian]]: as he was doing the documentation revamp he leaned towards *not* putting everything in ansible
                - the setup we have may be partly influenced by the lack of group wikis in gitlab at the time of design
                - question: when you want to use the ansible repo, the way it's intended to be used:
                    - you have your ssh key in your local machine that you're working on
                    - you clone the ansible repo
                    - you run the playbook locally and that connects and alters the server
                    - we could make a playbook for things currently in the sauce
                - [[ian]] if we want to go to the server and clone something there, that workflow (which comes more natural to some) just doesn't fit the above a lot
                    - unclear if there is a big advantage of moving [[docker compose]] stuff to [[ansible]], it's mostly one file
                    - [[ansible repo]] should indeed install docker, docker compose though
                    - [[flancian]] ansible did feel like a learning curve when starting
                    - [[edsu]] should we use [[ansible]] to do upgrades? maybe we could tackle [[mastodon upgrade]] this way and learn from that?
                    - [[ian]] even at work, ansible manages the stages from bare metal to deployment ready.
                    - [[edsu]] how do you deploy?
                    - [[ian]] customized git clone/symlinking in the server.
                    - [[ian]] what he would suggest is getting [[cicd]] on [[gitlab]] running
                    - [[ian]] the big thing with ansible is that it keeps the configuration in code
                    - [[edsu]] talking about the [[second server]] (see [[mastodon upgrade]]), we can take that same playbook and just go with it
                    - [[calix]]
                        - in [[autonomic]] they also tried using ansible for deployments and they gave up
                        - autonomic does the same, with [[coop cloud]]:
                            - using [[ansible]] to provision servers
                            - for deployments you use the [[coop cloud]] command-line interface, `abra` which uses [[docker swarm]] to do [[zero downtime deploy]]
                            - mastodon upgrades are still done by humans though :) but it's done somewhere standardized
                        - excited about consolidating documentation - definitely want to document things before trying to automate them
                    - [[flancian]] when I needed to fix the spam trap, it is deployed by ansible, found myself undoing some of the safety mechanisms
                - #push [[twg]] todos
                    - report to Nathan on wiki consolidation with a yes :)
                    - keep tech/operations as the One Repository to clone if you're a new member of the twg
                    - fold [[sauce]] general scripts into [[tech operations]]
                    - fold [[systemd unit]] files in [[sauce]] into [[ansible]]
                    - fold [[tech operations]] wiki into [[general.wiki]]
                    - [[redoak]] did the last mastodon upgrades, we could ask how long of a maintenance window we should call
                    - Announce maintenance window for upgrades: **Let's shoot for Monday 21 at 18-20 UTC**
                - [[ian]] with this setup, you can push a branch (pr) that updates the dockerfile; then pull it from the server; then run [[docker compose up]]
                    - database migration extra :)
        - [[mastodon upgrade]]
            - backup restores as a prereq for mastodon upgrade process? or is that too conservative?
        - second server for testing backup/restore
            - [[flancian]]: not comfortable doing upgrade without having done the restore; at some point we are going to have a problem and it will take us a few days to get back up; how was this done previously?
            - [[protean]]: when we moved from [[trunk]] (digitalocean vps) to [[runko]] (hetzner colocated) we had two servers
                - might be able to either
                    - A. do a test restore in a droplet
                    - B. run two compose instances on [[runko]], on different ports, there is a risk if you mess up.
            - [[calix]] [[coop cloud]] uses a mix of physical hardware and [[vps]]
                - does the process to get approval to get a new server or "just a droplet" vary?
                - if it's only a week or two to get approval for a new server, would recommend that
            - [[protean]] open question about the second instance
                - since we're offloading a lot of the assets to the [[digital ocean s3]] bucket -- how would the secondary instance setup look like?
                    - three options:
                        - configure a different bucket (empty)
                        - configure a different bucket (read only copy, somehow with an s3 feature?)
                        - use the bucket from prod (hmm)
                - looked into [[postgresql]] migration
                    - seems like all the steps are safe and have rollbacks
                - [[flancian]] how much downtime do we usually announce?
                    - [[protean]] has been a long time since he did one
                    - [[redoak]] did the last ones probably, we could ask
        - [[edsu]]: should we set up some time for live collaboration to work?
            - [[flancian]] let's try to do one upgrade? :)
            - [[ian]] late at night on a wednesday could be a good time
            - [[calix]] would agree with this -- but as a group of volunteers, it's fine to accomodate for active members' preferences
            - **Let's shoot for Monday 21 at 18-20 UTC**
        - [[protean]] how to do the hometown+mastodon setup cleanly?
            - [[flancian]] default: separate subdomain

## Several past instances had notes only on [[loomio]]
- See https://www.loomio.com/d/UwAeiBgE/tech-meeting-minutes for source of truth.

## 2022-05-27
- [[2022-05-27]]
    - [[flancian]]: OK with taking notes in doc.anagora.org/social-coop-tech-group? will cross-post to the minutes thread as usual.
    - attending: [[giacomo sansoni]] [[flancian]] [[akshay mankar]]
    - [[akshay]]
        - long holiday in Berlin, very nice!
        - don't work on Fridays, and yesterday was a holiday
        - [[wire swiss gmbh]]
        - [[mls]]
            - open standard
            - wire's implementation is based on [[haskell]]
            - tree based optimization to group encryption
    - [[flancian]]
        - working for Google, [[meet]]
    - [[flancian]] wdyt about [[matrix]]?
    - [[agenda]]
        - [[flancian]]
            - updates on ongoing work/learning
                - did admin task for user who wanted to reactive account
                    - [[akshay]] did you document?
                    - **[[flancian]] not in git.coop, will do that next :)**
                - learning containers, got a container up nicely yesterday
                - will keep poking at our setup and trying to understand the ansible recipes
        - stuff we could do next
            - **[[akshay mankar]] file bug in mastodon bug tracker for extra fields in the mastodon sign up form**
                - how do we handle user data in the long term? user data handling policy, etc.
                - started writing the issue but then stopped to better understand how the solution would look like
                - perhaps we should have an instance to experiment with
                    - [[flancian]] we might have this -- need to check containers and docs
                    - if not we should create it :)
                - mastodon already probably supports a good way to store information you got in the signup request, we could adapt it -- perhaps encode
            - [[akshay]] the idea here would be to send a PR to upstream instead of forking/applying our own path.
            - **[[flancian]] this seems to raise the priority of updating the instance to latest mastodon**
    - [[later]]
        - media issues?
            - one user reported them
            - [[akshay]] tusky sometimes show images as attachments
            - [[flancian]] get 500s relatively often when trying to upload
            - **[[akshay]] images go to [[s3]] in [[digital ocean]]**
            - **how do we look at logs?**
        - [[backups]] and [[restore]]
            - related to [[data management]] as well as we want to be careful/responsible with our user's data
            - where can we put these backups in? how do we extend the list of acceptable servers?
            - currently backups go to a [[s3]], but where to restore?
            - **how to make sure we don't mess up with the fediverse if we test restores?**
            - also related to the issue of [[failover]] in mastodon -- how is it supposed to work?
                - [[akshay]] you fail over the database, then frontends can all use the new primary
                - you need to solve balancing for the frontend or manually fail over that as well
    - [[akshay]] not attending the next one
        - attending [[zurihack]]!
        - let's meet!
    - [[flancian]] sent update in chat room: ![](https://doc.anagora.org/uploads/upload_ad643dbf540e732ff8232559bb9973dd.png)


## 2022-05-20
- [[2022-05-20]]
    - [[tech group]] session on [[password store]]: https://git.coop/social.coop/tech/pass


