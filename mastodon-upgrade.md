# Mastodon Upgrade Plan

This is a short writeup on how the [[social.coop]] [[tech working group]] could upgrade and improve our Mastodon instance as of [[Q4 2022]].

Canonical URL: https://anagora.org/mastodon-upgrade.

# Goals

- Detail how we plan to perform a Mastodon minor version upgrade safely, and how we plan to keep our instance up to date after that.
- Detail how we plan to experiment with new versions and mods without disrupting the social.coop community unnecessarily.
- Detail how we could adopt [[Hometown]], a promising [[Mastodon]] fork.
  - #todo There is a new promising fork that was recently boosted, look up the name and include it here as an option.
  
# Plan

## Organizational

- We will create a proposal in [[loomio]] to spend a monthly sum paying for a [[secondary server]] to  [[runko]].

## Minor upgrade

- Link to existing upgrade procedures here.
    - Mastodon Official.
    - Those gotten from our predecessors :)

## Recurring update schedule

It's a loop of: 

- Test backups.
- Maybe upgrade [[postgres]] or another dependency.
- Put the instance in [[maintenance mode]].
- Upgrade the instance proper.

#todo look at the Mastodon/Hometown update cadence and plan accordingly; if it's roughly monthly schedule a monthly run.

## Backups and restores

These are a prerequisite to safely running social.coop for the community. We must maintain a reasonable certainty that we would be able to bootstrap a replacement setup with minimal data loss in a bounded amount of time.

#todo Link to the procedures, stress the current source of truth.

## Hometown

We would like to run [[Hometown]] as a separate instance, as an experiment. Ideally this would still be done in a way that we can import our existing instance data into it without disrupting federation.