# Bonfire + Social.coop
- Attending: [[Ivan Minutillo]], [[Mayel de Borniol]], [[Flancian]]
- Intros
    - Ivan: a user of social.coop but not very active so far
    - Previously discussed with [[Eduardo Mercovich]] how social.coop could advance their experiment w.r.t. bonfire
- Flacian: a year ago we set up a test instance: http://bonfire.social.coop/ 
- maybe we could use it as Loomio replacement or complement (like the meta space for members to discuss the co-op)?
- could use SSO to log in which we have set up (bonfire supports oauth and openid connect)
- this would start as a local-users-only instance (without federation turned on) or at least ability to limit polls to members only
- the local-only approach would make sense also for the bonfire project
    - 'accepted answer' which was developed for the open science project (interesting) could also benefit social.coop
    - there's also reactions in the works
    - the [[decision making]] extension would be more sophisticated than polls
        - [[ukuvota]]: ukuvota.world, ukuvota.xyz
    - Q: would someone in social.coop be interested in helping build these features together?
        - facets: design and ux; coding
        - a researcher with experience in the social aspects as well would be great
        - last year a group of edumerco's students worked on the decision making extension for bonfire; they did prototyping based on some user research.
        - whoever picks this up could take the above prototype and run with it
        - **possible action: we could do a call for participators in social.coop.**
        - Ivan: one of the policykit devs is in social.coop.
            - risottobias@ :)
        - Mayel: this could be a from-first-principles project, or the focus could be 'what is missing/wrong in loomio for social.coop'.
- Federation testing is progressing in bonfire, but it's not considered ready yet, so an internal-only instance is a good fit.
    - campfire is now federation-enabled
    - using bounties to drive optimization
- On the potential dev project
    - [[elixir]] plus [[liveview]]
        - [[liveview native]] has os x / ios and soon windows/android targets
    - [[graphql]] api
    - a pure frontend prototype using tailwind would also help
    - extension generator lets people get the right scaffolding
    - demo (recent) extension, developed in a few hours: https://bonfirenetworks.org/posts/content_labelling_in_bonfire/
- Bonfire now implements a reddit-like threading model
- Next steps:
    - Bring up dev possibility with TWG
    - Update bonfire.social.coop and set up SSO for it
    - Bring up overall project with the OC
    - Ask Nathan w.r.t. governance modeling/research aspect
- The issue of use/participation mismatch in social.coop has been there since the beginning :)  
    - Bonfire's governance tool design is inspired (or more) by [[sociocracy]] and [[ukuvota]]

- Screenshots of decision extension prototype:
![](https://doc.anagora.org/uploads/upload_a4de741632f49cdc8237590f7d553d62.png)

![](https://doc.anagora.org/uploads/upload_5482f591d4da24a5ecb790e6cb9cec22.png)

![](https://doc.anagora.org/uploads/upload_4f4a14ccf46184ee4d1ffddc4fde5e28.png)

![](https://doc.anagora.org/uploads/upload_d41bf717838a4d5a55fd154bb9cd1e74.png)
- Q: how is the speed of bonfire nowadays?
    - A: that's our focus right now. There are bounties out for optimization. Financial support for more bounties could help.
    - https://www.loomio.com/p/IfnNLueo/please-allocate-funds-for-community-contributions-allocation-poll-from-fwg- took place and bonfire came in #8th