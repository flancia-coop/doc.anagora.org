
## 2023-10-09

Here: [[Akshay]], [[edsu]], [[Calix]]

- Check ins
- Mastodon 4.1 upgrade report
    - A: was chill!
    - E: search improvements?
- Tech roadmap? (from previous meeting)
    - we think Flancian created a draft?
    - https://anagora.org/twg-2024 
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


