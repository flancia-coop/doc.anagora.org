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

- It's a loop of: 
  - Testing backups.
  - Maybe upgrading [[postgres]] or another dependency.
  - Bri


## Backups and restores

- Link to those procedures as well.

## Hometown

We would like to run [[Hometown]] as a separate instance, as an experiment. Ideally this would still be done in a way that we can import our existing instance data into it without disrupting federation.