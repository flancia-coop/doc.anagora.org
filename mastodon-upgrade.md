# Social Upgrade Plan

This is a writeup on how the [[social.coop]] [[tech working group]] could upgrade and improve our Mastodon instance, and potentially offer the community new services, as of the time of writing ([[Q4 2022]]).

Canonical URL: https://anagora.org/mastodon-upgrade.

For more documentation from the working group, please refer to node [[TWG]].

# Goals

- Detail how we plan to perform Mastodon minor version upgrades safely, and how we plan to keep our instance up to date after that.
- Detail how we plan to experiment with new versions and mods without unnecessarily disrupting the [[social.coop]] community.
- Detail how we could evaluate and potentially adopt [[Hometown]], a promising [[Mastodon]] fork, or some other like .
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

We would like to run [[Hometown]] as a separate instance (defining this), as an experiment.  

We could do this on e.g. https://town.social.coop, bootstrapping a parallel instance. This could be done in two ways:

- Set up a read only instance off database restores, read only meaning also with federation off. Let users play with it and reach a conclusion on whether they are interested in the change.
- Set up a new instance where users can sign up for independent profiles to fully test drive [[Hometown]] also as a writing/local collaboration/governance platform.

In the medium term (after a set experimentation phase) users would vote on whether they want to move to [[Hometown]] as the software serving their social.coop [[Fediverse]] profiles.

### Matrix

There has been interest in running a [[Matrix]] instance (#todo link). If we had a secondary server and thus could achieve a reasonable primary/secondary hot spare setup for arbitrary services, we'd be more comfortable running more services for the community.