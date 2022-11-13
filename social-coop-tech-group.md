## [[2022-11-14 19:00 UTC]]
- Location: https://socialcoop.meet.coop/dav-y3e-c21-sgv 
- Attending: x, y, z
    - These will be crossposted to [[go/twg/minutes]].
- Default agenda
    - [[check ins]]
    - suggested topics follow, please add more :)
        - [[documentation]] source of truth
            - default: [[go/twg/wiki]]
            - report back to https://www.loomio.com/d/2Rwh5z3H/time-to-consolidate-wikis- (as per [[nathan schneider]]'s request.)
        - [[mastodon upgrade]]
            - backup restores as a prereq for mastodon upgrade process? or is that too conservative?
        - second server for testing backup/restore

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


