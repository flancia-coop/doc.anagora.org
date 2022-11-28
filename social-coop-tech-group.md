## $NEXT
- Location: https://socialcoop.meet.coop/dav-y3e-c21-sgv 
- Attending: 3wc, edsu, protean, flancian, davidvasandani, dphiffer
- Check ins
    - Edsu: working from home every day
    - Flancian: working from home *today*
    - Ian: playing with monitoring
        - added live process monitoring
        - hooked up logging
    - dphiffer: is here :) was lurking during updates
        - welcome!
        - in NY north of Albany
        - WFH for a non profit
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
        - what should go into tech/operations, and what into ansible?
            - [ ] check now, per directory, and make a call? :)
    - revisiting last week's upgrade
        - what should we do differently last time?
        - have we updated documentation sufficiently? where? :)
    - next steps for Mastodon upgrades
        - v3.5 -> ?
    - [[backups]]
        - either they were happening some other way, or they weren't happening
        - postmortem
            - backup timer didn't have WantedBy=timers.target
    - [[postgres]]
        - shouldn't be listening on the external network?
        - we should revisit .env in docker directory.
    - [[reliability]]
        - how having two servers increases reliability, and having three servers increases it more :)
    - [[cloudflare]] / [[dns situation]]
        - [[mayel.space]]
    - [[cloud grants]]
        - have we considered or previously applied for the annual grants that AWS and Azure offer?


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


