From discussion in [[agora development]] in [[2022-04]], thank you all participating!

4/10/2022, 11:41:41 AM - charismatic_shell 🍄: By the way, why is there the Google copyright in the code?

4/10/2022, 2:00:21 PM - flancian 🍄: ahoy! yeah, so I went through the internal process to retain copyright on the Agora as a side project and I didn't get it. so all code (repos [[agora server]], [[agora bridge]]) has Google copyright notices.

4/10/2022, 2:00:39 PM - flancian 🍄: the [[agora]] root repository does not as it's configuration + writing only. the same for [[flancia org]].

4/10/2022, 2:01:11 PM - flancian 🍄: IIUC it doesn't make a difference as I don't personally care about copyright. it only affects contributors as they need to sign a [[cla]] (one time only) to contribute to [[agora server]] or [[agora bridge]].

4/10/2022, 2:01:18 PM - flancian 🍄: please let me know if it bothers you though! I want to know more.

4/10/2022, 4:40:30 PM - charismatic_shell 🍄: <@flancian:matrix.org "ahoy! yeah, so I went through th..."> This is so [[Babylon]]

4/10/2022, 4:41:10 PM - charismatic_shell 🍄: Yes, it bothers me, I do not want the good stuff and the personal stuff to be associated with Google

4/10/2022, 4:42:51 PM - charismatic_shell 🍄: So, if I want to contribute to you, I have to sign a document with Google?

4/10/2022, 5:06:50 PM - flancian 🍄: <@charismatic_shell:matrix.org "This is so [[Babylon]]"> you say [[babylon]], I say [[moloch]], I believe

4/10/2022, 5:07:10 PM - flancian 🍄: together we'll defeat [[babylon]], we'll defeat [[moloch]]

4/10/2022, 5:07:18 PM - flancian 🍄: that's what I believe and what I say

4/10/2022, 5:07:52 PM - flancian 🍄: knowing this, I'd love to 1. understand your issues with the licensing/copyright scheme for the Agora, and 2. try to improve

4/10/2022, 5:10:50 PM - flancian 🍄: this is what I think summarizes my position w.r.t. the [[entaglemente]] between [[google]] and the [[agora]]:

4/10/2022, 5:11:18 PM - flancian 🍄: how many flancians are there working for \[\[google\]\]? -- I can prove there is at least one, and I think I can prove there are many

4/10/2022, 5:14:03 PM - moonlion.eth (vera) 🍄: the reason my github name is `fuck-capitalism` is so google has to accept code from that username heh

4/10/2022, 5:38:08 PM - moonlion.eth (vera) 🍄: >DONE hmm, but there is low hanging fruit: the per-worker cache should not all expire in unison (!)

>also I wasn't caching calls to G.node() (?).
AND, much more importantly, the Agora was restarting all the time due to 500s in URLs hit by bots -- so none of the performance work I was doing was taking effect. Now that that's fixed it feels much snappier! I am happy about this development.

4/10/2022, 6:11:28 PM - charismatic_shell 🍄: yes, exactly. I wanted to note that before, I'll do it now. UPD: done, see melanocarpa.lesarbr.es/hypha/babylon
4/10/2022, 6:14:40 PM - charismatic_shell 🍄: <@flancian:matrix.org "knowing this, I'd love to 1. und..."> 1. I do not want the good stuff (and I classify Agora as good stuff) to be related to Google, that's my only issue with Agora's licensing.
2. I guess only you can do that. Agora should be liberated from Google somehow. I do not know how does it work and why is it related in the first place.
4/10/2022, 6:16:00 PM - charismatic_shell 🍄: <@vera:fairydust.space "the reason my github name is `fu..."> I see. That's a way. But I do not like the insult in the name nevertheless. If I ever to list you somewhere on GitHub, I'd rather to refer to you as Vera.
4/10/2022, 6:17:27 PM - moonlion.eth (vera) 🍄: i understand
4/10/2022, 6:17:38 PM - moonlion.eth (vera) 🍄: its that way on purpose
4/13/2022, 10:55:26 AM - flancian 🍄: <@charismatic_shell:matrix.org "1. I do not want the good stuff ..."> thank you for your feedback! sorry for the delay in my response -- which was, wait for it, mostly because of my work at Google :)
4/13/2022, 10:55:43 AM - flancian 🍄: on 1: I think I'd like to explore what 'related to' means.
4/13/2022, 10:55:55 AM - flancian 🍄: on 2: same for 'liberated'.
4/13/2022, 10:56:57 AM - flancian 🍄: a priori I think I understand why you are concerned, and I've probably had a lot of the same thoughts before. but in the end I didn't find the relationship or entanglement that serious; then again, I am biased to see this as a non-issue, as it makes my life simpler while keeping the Agora presumably viable.
4/13/2022, 10:58:06 AM - flancian 🍄: by this I mean: as far as I can tell the only outcome from Google holding copyright for the Agora code ([[agora server]], [[agora bridge]]) is that 1. they choose the license, 2. they choose where the primary repos are to be hosted, 3. they require me to check for a signed [[cla]] before accepting contributions.
4/13/2022, 10:58:09 AM - An Agora: https://anagora.org/agora-server
https://anagora.org/agora-bridge
https://anagora.org/cla
4/13/2022, 10:58:43 AM - flancian 🍄: for 1, the license is [[apache]] -- which honestly is good enough for me. I have historically been a fan of GNU, but MIT/BSD style seems fair enough and probably more flexible for some.
4/13/2022, 10:58:43 AM - An Agora: https://anagora.org/apache
4/13/2022, 11:00:31 AM - flancian 🍄: for 2., they want [[github]] to be the hosting platform. I would probably have moved elsewhere by now (somewhere open source!) if this wasn't a requirement, so it does bother me a bit; but it also has upsides, mostly due to the fact that Github is so popular (I know there's a self-fulfilling prophecy scenario here maybe).
4/13/2022, 11:00:32 AM - An Agora: https://anagora.org/github
4/13/2022, 11:01:11 AM - flancian 🍄: for 3., that's probably the most annoying. I have had to turn down at least one contribution from someone who definitely didn't want to sign a CLA. this is the one I'm most worried about.
4/13/2022, 11:02:26 AM - flancian 🍄: about why Google gets to choose all this: a committee reviewed my proposal to keep the Agora my copyright and turned it down, essentially. so my two options were A. quit Google before starting coding and B. open source with Google copyright. you know which one I chose :)
4/13/2022, 11:03:40 AM - flancian 🍄: I think the extent to which this should limit users' freedoms is negligible, unless I'm missing something. people can still fork the Agora as they please, and IIUC (not a lawyer, please check, I mean to learn more about this) even relicense the fork?                                                                                                                                                                                      
4/13/2022, 11:04:41 AM - flancian 🍄: in the meantime I get to keep my job which pays very well, which allows me to live very well in a stable country and donate a significant fraction of my salary to humanitarian efforts and directly to people. put another way, this lets me dedicate some resources to actually building a version of Flancia.                                                                                                                                
4/13/2022, 11:06:05 AM - flancian 🍄: my calculation is that this setup is relatively optimal, in the sense that if I stopped collecting my salary for this Agora to become fully independent from Google the overall impact on others might be negative (because I couldn't donate the same fraction anymore, etc.)                                                                                                                                                                  
4/13/2022, 11:06:35 AM - flancian 🍄: but I might be missing one or many good points here -- for example, in particular, any about a scenario where there's risk of Google exerting negative influence on the Agora in a timeline in which the Agora additionally turns out to be very significant.                                                                                                                                                                                   
4/13/2022, 11:08:57 AM - flancian 🍄: but given that IIUC 1. the community could always fork the codebases and 2. the root Agora repository does not contain code, I'm not rating that risk as high.                                       
4/13/2022, 11:09:09 AM - flancian 🍄: of course also there's only low probability that the Agora turns out to be very significant :) although I do dream.                                                                                  
4/13/2022, 11:11:04 AM - flancian 🍄: wdyt?                                                                                                                                                                                                
4/13/2022, 1:09:17 PM - doubleloop: I'm also not a lawyer but I think in theory that Google, as the copyright holder, could relicense the projects to something restrictive should they choose to.  If they did, I'm not sure that we could just fork Agora and relicense.  Only the copyright holder can.                                                                                                                                                                            
4/13/2022, 1:12:35 PM - doubleloop: That said, I kind of see Agora as an exploration of patterns of collaborate knowledge management.  So while it would undoubtedly suck if Google chose to do something negative with the code, that seems like a long way off, in the meantime of which we will have pioneered a way of working that could be replicated with a new codebase with no Google association.  And no actual data in the knowledge commons is affected.  So I agree with Flancian as to this being a local optimum that enabled it to be built.                                                                                                                                                                    
4/13/2022, 1:13:33 PM - doubleloop: Probably the biggest threat seems the reputational one where plenty of people have an aversion to Google and will be put off by the connection even if minimal.
4/13/2022, 1:30:09 PM - doubleloop sent an image. (Media omitted)
4/13/2022, 1:30:10 PM - doubleloop: Seem to be seeing this semi-regularly on anagora at the mo 
4/13/2022, 3:13:08 PM - flancian 🍄: Same here! I'll try something quick now and look into it more later
4/13/2022, 3:16:03 PM - flancian 🍄: I restarted the Agora, let me know if it makes a difference? I can't reproduce anymore
4/13/2022, 3:38:27 PM - charismatic_shell 🍄: <@flancian:matrix.org "on 1: I think I'd like to explor..."> I guess, having the name Google somewhere in the code
4/13/2022, 3:38:36 PM - charismatic_shell 🍄: <@flancian:matrix.org "on 2: same for 'liberated'."> I guess, getting rid of the name from the code
4/13/2022, 3:39:08 PM - charismatic_shell 🍄: <@flancian:matrix.org "a priori I think I understand wh..."> I understand
4/13/2022, 3:42:04 PM - charismatic_shell 🍄: <@flancian:matrix.org "for 3., that's probably the most..."> I don't want to sign a CLA too, actually
4/13/2022, 3:43:47 PM - charismatic_shell 🍄: <@flancian:matrix.org "in the meantime I get to keep my..."> A worthy trade-off, yeah
4/13/2022, 4:33:38 PM - doubleloop: <@flancian:matrix.org "I restarted the Agora, let me kn..."> Seems good, thanks!
4/15/2022, 2:41:32 AM - moonlion.eth (vera) 🍄: https://anagora.org/raw/garden/vera/ivo.md is causing 500
4/15/2022, 2:41:51 AM - moonlion.eth (vera) 🍄: flancian 🍄: where is the best log file to look in to debug errors?
4/15/2022, 2:42:24 AM - moonlion.eth (vera) 🍄: I remember trying to hunt something similar down recently and couldn't find where it was erroring to
4/15/2022, 8:48:58 AM - Flancian#6471: Ahoy! agora.log in the agora server root should be a good place to start
4/15/2022, 8:49:16 AM - Flancian#6471: Better monitoring is slowly in the works :)
4/15/2022, 11:24:54 AM - moonlion.eth (vera) 🍄: <@_discord_708787219992805407:t2bot.io "Ahoy! agora.log in the agora ser..."> awesome that worked
4/15/2022, 11:31:30 AM - flancian 🍄: nice! what was it, what's the exception?
4/15/2022, 11:32:53 AM - flancian 🍄: also is there an admin interface for gitea? [[protopian]] is having issues with access to the repo and I'd like to debug, do you know how to do this moonlion.eth (vera) 🍄 ?
4/15/2022, 11:32:53 AM - An Agora: https://anagora.org/protopian
4/15/2022, 11:34:41 AM - flancian 🍄: <@doubleloop:matrix.org "I'm also not a lawyer but I thin..."> thank you for this take! this could indeed be worrying -- it was my understanding, though, they could relicense but couldn't retroactively apply the new license, meaning the community could always fork the latest state that was apache licensed. does this map to your understanding?
4/15/2022, 11:38:26 AM - flancian 🍄: <@doubleloop:matrix.org "That said, I kind of see Agora a..."> thank you! yes, I agree with this. if the Agora is valuable I think having different implementations, hopefully all capable of talking a common Agora protocol to each other, would be desirable. and the base implementation of an [[agora server]] is simple, given the file-based nature of it -- it took me one weekend to code a barebones version and get it serving, and I'm no great coder.
/15/2022, 11:38:26 AM - An Agora: https://anagora.org/agora-server
4/15/2022, 11:40:41 AM - flancian 🍄: this is why it seemed critical to me to keep the Agora root repository, which actually contains the base contract and links to all source repositories, detached from the actual server/bridge implementations.
4/15/2022, 11:41:01 AM - flancian 🍄: unsure if it will be relevant or will just remain symbolic, but it seemed like the right thing to do.
4/15/2022, 11:43:55 AM - doubleloop: <@flancian:matrix.org "thank you for this take! this co..."> Sounds plausible!  
4/15/2022, 11:44:44 AM - flancian 🍄: <@doubleloop:matrix.org "Probably the biggest threat seem..."> yes, this is also my estimate. on the other hand, two possible flip sides: 1. some people might still have a *positive* (conditional?) disposition towards Google, although granted I'm not sure how many of them will be anarchists/commoners or have compatible goals -- then again the set can't be null as I exist :)
4/15/2022, 11:45:05 AM - flancian 🍄: 2. this might actually motivate someone to start a second implementation not bound by these constraints.
4/15/2022, 11:45:38 AM - flancian 🍄: of course the question then becomes whether the second implementation would seek to remain compatible or would break away in a way that makes cooperation unlikely, etc.
4/15/2022, 11:48:03 AM - flancian 🍄: <@charismatic_shell:matrix.org "I guess, getting rid of the name..."> I get what you mean. I guess I'd ideally go further and define 'liberate' as getting rid of the notion of 'copyright' in the first place :)
4/15/2022, 11:48:18 AM - flancian 🍄: copyright just essentially feels like a bunch of bullshit to me, I hope you don't mind the terminology.
4/15/2022, 11:49:05 AM - flancian 🍄: if not intrinsically wrong (and it might be -- at least in this digital age), then pretty much completely corrupted.
4/15/2022, 11:50:08 AM - flancian 🍄: this has something to do with my primary reaction to Google's decision -- I don't care for copyright, I'm not interested in holding copyrights, so essentially they can have it.
4/15/2022, 11:50:38 AM - flancian 🍄: perhaps a naive position? unsure. hopefully not harmful.
4/15/2022, 11:55:36 AM - doubleloop: Worth noding some of this in a stoa?    I'm sure it's not the first time it has come up, probably not the last, save you from having to explain it over and over?  Happy to pop it in somewhere if useful.
4/15/2022, 11:56:46 AM - flancian 🍄: oh, that's a good idea! it's come up before but I think this is the fullest conversation on this topic yet -- before there wasn't much of a community to have a conversation with/in/as :)
4/15/2022, 11:58:09 AM - flancian 🍄: I think we can use [[copyright]]?
4/15/2022, 11:58:09 AM - An Agora: https://anagora.org/copyright
4/15/2022, 11:58:12 AM - flancian 🍄: or [[agora copyright]]
4/15/2022, 11:58:12 AM - An Agora: https://anagora.org/agora-copyright
4/15/2022, 11:58:39 AM - flancian 🍄: the copyright node looks interesting already, nice -- its related nodes
