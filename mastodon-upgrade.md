# Mastodon Upgrade Plan

This is a short writeup on how the [[social.coop]] [[tech working group]] could upgrade and improve our Mastodon instance as of [[Q4 2022]].

Canonical URL: https://anagora.org/mastodon-upgrade.

# Goals

- Detail how we plan to perform a Mastodon minor version upgrade safely, and how we plan to keep our instance up to date after that.
- Detail how we plan to experiment with new versions and mods without disrupting the social.coop community unnecessarily.
- Detail how we could adopt [[Hometown]], a promising [[Mastodon]] fork.
  - #todo There is a new promising fork that was recently boosted, look up the name and include it here as an option.
- Detail how the [[social coop tech group]] plans to run this project and others like it.
  
# Plan

## Organizational, meta

This section covers prerequisites for the work being undertaken below coming to fruition. Our intention is to do the needful to ensure that our community's well being and stated preferences are prioritized.

- We will create a proposal in [[loomio]] to spend a monthly sum paying for a [[secondary server]] to  [[runko]].
- We will define [[sources of truth]] for shared projects undertaken by the [[twg]], including [[channels]] to communicate with members of the [[social coop tech group]] and otherwise influencing the process.

## Mastodon upgrades

Our highest user-visible priority is to keep the [[Mastodon]] instance behind https://social.coop running smoothly.

- #todo Link to existing upgrade procedures here; then integrate them into a single source of truth, inline or linked.
  - Those we found in the [[twg]].
    -> https://git.coop/social.coop/tech/operations#mastodon-upgrade-notes
  - The Mastodon Official ones.
  - Those gotten from our predecessors through the social.coop thread :)

### Recurring update schedule

It's a loop of: 

- Test backups.
- Maybe upgrade [[postgres]] or another dependency.
- Put the instance in [[maintenance mode]].
- Upgrade the instance proper.

The [[work schedule]] we got from the previous members of the [[twg]] is at https://git.coop/social.coop/tech/operations/-/wikis/jobs.

Linking is sparse for now; https://git.coop/social.coop/tech/operations#mastodon-upgrade-notes exists, for example, but the link to [[mastodon upgrade]] in the link above leads nowhere.

#todo look at the Mastodon/Hometown update cadence and plan accordingly; if it's roughly monthly schedule a monthly run.

## Backups and restores

Our highest priority is to test backups and restores. These are a prerequisite to make any changes to our setup, and indeed for safely running https://social.coop for the community. We must maintain a reasonable certainty that we would be able to bootstrap a replacement setup with minimal data loss in a bounded amount of time.

#todo Link to the procedures, state the current source of truth for procedures.

## Experiments

In addition to keeping the lights out, we would like to explore possible [[improvements]] to the services run by and for [[social coop]].

### Hometown

We would like to run [[Hometown]] as a separate instance, as an experiment. 

We could do this by running something like https://alpha.social.coop, which would be the 'bleeding edge' (what we plan to ship to users by default at some later point). 

This would of course need to be done in a way that preserves instance data. Easier: run it as read only, federation off, off a database restore. import our existing instance data into it without disrupting federation. Ideally

### Matrix

There has been interest in running a [[Matrix]] instance (#todo link). If we had a secondary server and thus could achieve a reasonable primary/secondary hot spare setup for arbitrary services, we'd be more comfortable running more services for the community.