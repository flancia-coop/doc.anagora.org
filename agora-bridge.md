# Newer/Unanswered Questions

# Older Questions
- Are we currently using the interlay git repo/graph on the current agora?
    - It's my understanding that the agora is using gardens.yaml to build the agora. I feel like we need to make a decision on that before we can programatically add repos to the agora
    - Yes, we're *not* currently using git submodules or subtrees; we're still just using https://github.com/flancian/agora-bridge/blob/main/pull.py which clones each repo in a target dir.
        - We could move to git submodules, but I'm not sure it is blocking?
        - Yeah I guess it's not blocking we can just put in the current "garden" path into the config file and I'll leave out any sort of magic for now
            - totally, yeah -- 'target' in the yaml should actually be relative to the agora root, it's an easy fix to make that I can do independently in pull.py. feel free to assume target works like this :)
        - E.g. [[agora bridge]] could just write a file like `gardens.py` 'mounting' each of the git repositories it's serving so pull.py can then pull them in -- that way it seems like we can keep the complexity of 'mounting' all in pull.py
- Q: could you use [[go/agora-bridge]] repo (the one in github) to do development? maybe in a branch? I know it's a bit of a hassle as you started in -js but I think it's better if we use the same repo for now. wdyt?
    - Sure I just had the existing repo with the code, but we can move this to python if you want. See the stoa is useful. We weren't even working in the same language lol.
    - No, I mean, I think JS is the right language for this :) It's just that I think we should stick with one repo for all agora bridging :) wdyt?


# Agora Bridge
- Hello my **friend**!
- [[push]] [[hedgedoc]]
    - [[meta]] We should make [[wikilinks]] work :)
    - I actually really like how it supports a reasonable featureset out of the box, like images:
    - ![](https://doc.anagora.org/uploads/upload_c0f8839ace0a4b1a732fefacb0b928d9.png)
- Now about actual [[agora bridge]]:
  - api to add repo to agora
      - /repo/add (takes json?)
  - api to push content to agora using managed repos
      - /push/node? (takes arbitrary resource?)
if we push content via http how is this a benefit over just using an [[agora client]]
  - this is more generic, lets anyone say 'please add this URL or resource to this Agora at a certain place' -- it is resource-granularity instead of user granularity essentially
  - in a way it would feel more like people using the stoa: they need only care about a (resource, node) pair, no need to become agora users?
  - also this way people don't need to learn git :) 
interesting. i wonder if we should have a writable ui like we were working on so people can edit managed repo from the site

I'm on mobile so my formatting is shite lol
- haha, I was wondering! that makes complete sense :)
- I think yes, we need more write paths to the agora. the nice thing about this is that we keep clients super simple: an agora client becomes anything that 1. writes to a repo and tells us about it or 2. asks us to take something and put it in a repo for them. the second is more of a nice to have than strictly needed; if everyone was running things like promnesia, we wouldn't need this :) but IMHO this will make it more 1. diverse and 2. hackable
    - also I totally need this so agora bot doesn't need to deal with git repos. it seems like it'll be great to be able to 'just curl to an agora nearby' and get git repo management done by a server
    - i like this idea a lot
    - then again perhaps I'm old school and always thinking of the server side :) unsure.
what's old is new again
:)
    - [[meta]] also honestly I'm digging hedgedoc, this coloring thing actually kind of works? it'd be nice to have 'different colors for different users' as an option though, perhaps that's doable
yeah I'm liking it a lot actually
- (I probably have to go take a walk/deal with some packages, will be back later) 
- do you think /repo/add and /push/node make sense? if not in name/path, in essence?
i would use /repo with POST verb then we can use same url for GET
oh, that makes sense, yes. I did a few REST APIs once upon a time but I sort of became a fan of 'anything goes' Agora style :) I think you're right though
I would recommend same with /node
so /push takes a post which is a json payload with node=x and body=y?

no /node takes a PUT that updates or creates
SGTM :)

rest is for managing resources 


- about `gardens.yaml`: I think I'll rename it. or perhaps I already have :) need to check. in any case, I want to make it so that target: takes a path relative to the agora root. this way we can really map git repos to any agora path and have the agora mount them, essentially turning the agora into a layered filesystem.

i like this idea


let met check if I've already done the first part -- i want to do this and also add hedgedoc as stoa before leaving for vacation :) but if not I'll do it on some free moment in Italy, even though the plan is to disconnect as much as possible to fight against burnout :) do you think you will be able to give the api a shot? no pressure of course.

yeah that's why i wanted this doc lol

:D

also, when you said rest is for managing resources, do you mean that it applies here well or doesn't? I think you meant the earlier.

wait, hedgedoc is coloring the left hand side with user information! the line by the number

i meant it applies well because we are doing literal resource management. create/read/update/delete of nodes and repos

yes, I like that a lot. and then the pitch is: if you have CURL and are fine with a REST API, you can write to an agora without auth

later on we might want to solve hard things like file storage in special repos and such :) there's a git plugin/extension that is meant for large/binary file management, I forget the name


git lfs
large file storage


indeed :) I wonder if there's lfs in ipfs? :)

I'm not sure why ipfs would need it. large files are a failing of git internals

no, I mean the other way around -- like, store large files on ipfs. unsure if it makes sense though.

oh you mean use ipfs for lfs storage. that might be a thing already

yeah, true.

[[aside]] perhaps [[radicle]] is something close to this


radicle sounds familiar i need to check it out again





:)


