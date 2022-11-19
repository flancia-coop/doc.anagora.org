# Mastodon Upgrade Plan

This is a writeup on how the [[social coop tech group]] plans to upgrade and improve our Mastodon instance, and potentially offer the community new services, as of the time of writing ([[Q4 2022]]).

For more documentation from the working group, please refer to node [[TWG]] or [[social coop tech group]].

- Canonical URL: https://anagora.org/mastodon-upgrade.
- Authors: [[flancian]], [[edsu]], your_name_here (this document is open to the public).

# Goals

- Detail how we plan to perform Mastodon minor version upgrades safely, and how we plan to keep our instance up to date after that.
- Detail how we plan to experiment with new versions and mods without unnecessarily disrupting the [[social.coop]] community.
- Detail how we could evaluate and potentially adopt [[Hometown]], a promising [[Mastodon]] fork.
  - Extend this to other promising forks like [[Smalltown]], or alternate codebases such as [[Pleroma]] or [[Bonfire]].
- (Meta) Communicate to the community how the [[social coop tech group]] plans to run this project and others like it.
  
# Plan

## Organizational, meta

This section covers prerequisites for the work being undertaken below coming to fruition. Our intention is to do the needful to ensure that our community's well being and stated preferences are prioritized.

- We will create a proposal in [[loomio]] to spend a monthly sum paying for a [[secondary server]] to  [[runko]].
- We will define [[sources of truth]] for shared projects undertaken by the [[TWG]], including [[channels]] to communicate with members of the [[social coop tech group]] and otherwise influencing the process.
- We will report back to the community on progress, by default [[monthly]].

## Mastodon upgrades

Our highest user-visible priority is to keep the [[Mastodon]] instance behind https://social.coop running smoothly.

- #todo Link to existing upgrade procedures here; then integrate them into a single source of truth, inline or linked.
  - Those we found in the [[twg]].
    -> https://git.coop/social.coop/tech/operations#mastodon-upgrade-notes
  - The Mastodon Official ones.
    -> https://github.com/mastodon/mastodon/releases
      - As of the time of writing, https://social.coop is running version [[3.4.6]] (eight months old). Latest is [[3.5.3]].
  - Those gotten from our predecessors through the social.coop thread :)
    -> https://social.coop/web/statuses/109080658507991367 points to https://git.coop/social.coop/tech/operations#mastodon-upgrade-notes, so we found what we have it seems :)

### Recurring update schedule

It's a loop of: 

- Test backups.
- Maybe upgrade [[postgres]] or another dependency.
- Put the instance in [[maintenance mode]].
- Upgrade the instance proper.

The [[work schedule]] we got from the previous members of the [[twg]] is at https://git.coop/social.coop/tech/operations/-/wikis/jobs. Linking is sparse for now; https://git.coop/social.coop/tech/operations#mastodon-upgrade-notes exists, for example, but the link to [[mastodon upgrade]] leads nowhere currently.

We should look at the Mastodon/Hometown update cadence and plan accordingly; if it's roughly monthly on average, schedule a monthly run. As detailed in the section above, we are currently eight months behind on releases.

## Backups and restores

Our highest overall priority is actually to test backups and restores. These are a prerequisite to make any changes to our setup, and indeed for safely running https://social.coop for the community. We must maintain a reasonable certainty that we would be able to bootstrap a replacement setup with minimal data loss in a bounded amount of time (low *Time To Restore*.)

Tech procedures are kept mainly in [[go/twg/wiki]].

## Experiments

In addition to keeping the lights out, we would like to explore other possible [[upgrades]] and [[improvements]] to the services run by and for [[social coop]].

### Hometown

We would like to trial [[Hometown]] as an improvement over the default [[Mastodon]] experience. We could start by running it as a separate instance. The rest of this section tries to detail how we would go about this as an experiment. 

The proposal is to do this on a designated subdomain e.g. https://alpha.social.coop (if we would like to reuse this approach for testing upgrades/new software packages in general) or https://town.social.coop. We would be bootstrapping a parallel ActivityPub instance. This could be done in two ways:

- Set up a read only instance off database restores, read only meaning also with federation off. Let users play with it and reach a conclusion on whether they are interested in the change.
- Set up a new instance where users can sign up for independent profiles to fully test drive [[Hometown]] also as a writing/local collaboration/governance platform.

In the medium term (after a set experimentation phase) users would vote on whether they want to move to [[Hometown]] as the primary software serving their social.coop [[Fediverse]] profiles.

### Matrix

There has been interest in running a [[Matrix]] instance (#todo link). If we had a secondary server and thus could achieve a reasonable primary/secondary hot spare setup for arbitrary services, we'd be more comfortable running more services for the community.

# Alternatives considered

## [[Coop Cloud]]

We could build on top of https://coopcloud.tech/ instead of running our own stack. This requires further exploration.

If we go this way, it could be a good idea to experiment first on this stack with one of the additional services being considered, like [[Matrix]], instead of trying to upgrade or replace already-core functionality like Mastodon.

## [[VPS]]

For the purpose of running a secondary server, it might very well be that VPSs as offered by Hetzner or Digital Ocean are sufficient and more cost-effective. We need to explore this as an option and report back to the community.