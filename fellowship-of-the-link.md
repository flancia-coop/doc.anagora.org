# Fellowship of the Link

- a [[meeting]].
    - [[weekly]]
    - #go https://meet.jit.si/fellowship-of-the-link
    - Wednesdays at [[6PM UTC]].
    
## Agenda

Can be recurring or with a marked date.

- Attending: [[x]]
- Start recording, we're currently using Jitsi and that works best with a [[Chromium]] based browser.
- #pull [[fotl threads]]

## 2022-11-02
- Attending: [[peter kaminski]] [[chris aldrich]] [[aram zucker-scharff]] [[jerry michalski]] [[flancian]]
- [[peter kaminski]] [[airtable]]
    - #push [[thinking tools map]]
        - working on [[project plan]] prior to bringing it to the [[fellowship of the link]]
        - https://dainty-sable-264aa3.netlify.app/project/measuring_thinking_tools.html
    - [[chris aldrich]] [[openness]] axis seems too dense
    - [[calendar]]

## 2022-10-26
- Attending: [[peter kaminski]] [[chris aldrich]] [[flancian]] [[bentley davis]] [[maparent]] [[samuel klein]]
- Second call on [[Wednesday]].
- Recording in Jitsi only works in Chromium.
    - No firefox, no safari for now.
    - Worth filing a bug.
- Last time recap
    - Integration of tools for thought
    - Hyperknowledge and Agora
    - Debate tools and quality of discourse as they relate to the political scene
- Check ins
    - [[maparent]]
        - Discussed a lot of common issues in [[free jerry's brain]] meeting on Monday.
        - In there we spoke about [[hyperknowledge]] and [[next actions]] as well.
        - Among other things, made a plea for [[concept glue]] between systems.
            - Deep links, deep addressability aspects seem key.
            - Making cross linking easy.
        - Bentley brought up: we could achieve a better understanding by trying some use cases and seeing which kind of maps do we want to build off real data.
            - [[flancian]] we had a pending AI from a previous meeting that 
        - [[frame views]] URLs for concepts and for frames centered around that thing
            - [[flancian]] sounds similar to [[nodes]]
            - [[chris aldrich]] lots of note taking tools are text based, and backing databases are non public / don't have URLs
                - #map deep linking and addressability is indeed about having a URL for each block even in those scenarios
                - [[web annotations]] use ranges, we could have the same for markdown
                - "xpath for markdown"
                    - +1
                    - web annotation targets for markdown
                - [[flancian]] what about wikilinks as anchors within notes?
                    - #map semantic ambiguity
                        - #flancian Not sure
                    - #map doesn't work in the general case as it's only controlled by the writer
                        - #flancian: fair
                        - #maparent look at at-json
                - 'this thing in this document at this time' -- [[memento protocol]] for example
                    - "memento protocol over massive wiki"
                    - could map to a git commit in the case of git backed repositories
                    - [[chris aldrich]] could be resolved via internet archive for the web in the general case when that is available
                    - [[maparent]] Actually used by web archive. See http://timetravel.mementoweb.org/about/
                - [[meta]] how do we track of 'interesting threads' like that above?
                    - [[peter kaminski]] what about a shared page?
                    - -> AI: create a document/repository location and designate it as first version of this :)
    - [[Peter Kaminski]]
            - [[Thinking Tools Map Project]] update
                - [[mathew lowry]] did a fair amount of work
                - some of our project work got out of sync but it's being merged
                - realization: we had not set up a way to do collaboration beforehand, both platform and convention level
                - -> [[massive wiki channel]] in [[ogm mattermost]]
                    - <https://chat.collectivesensecommons.org/agora/channels/massive-wiki>
                    - <https://chat.collectivesensecommons.org/agora/pl/nshenqwxxj8mbq1rptiddut96r>
                - collaborating over chat is relatively hard, threading is only basic
                - [[github issues]] and branches
                    - maybe a document workflow with comments would be lighterweight?
                    - Note: issues in git (vs github) with [GitBug](https://github.com/MichaelMure/git-bug)
            - Looked again at Markdown parsers (particularly those that can create ASTs, because that's a sign of development organization and quality)
                - [remark](https://unifiedjs.com/explore/project/remarkjs/remark/) + [micromark](https://github.com/micromark/micromark) (JavaScript)
                - [mistletoe](https://github.com/miyuchina/mistletoe) (Python)
                    - [[flancian]] the Agora (Python) currently uses [[marko]], but mistletoe looks superior at first glance
                    - [[markdoc]] is an extended [[markdown]] syntax created/used by [[stripe]]
            - [[schema]]
                - [[people]] [[tools]] [[techniques]]
                - #map [[goals]] maybe as a separate category, or [[intent]]
                - maybe also [[audience]]
                - -> AI: add to threaded document.
            - Wishing there were typed links in Markdown
                - [[flancian]] in the Agora, links are typed/annotated by the preceding one (or tag)
                - @scalingsynthesis uses prefixes: https://anagora.org/@scalingsynthesis
                - [[chris aldrich]] [[microformats]] could be part of a link
                - #map [[yaml]] blocks could go anywhere?
                    - [[supertag]] syntax is growing on him
                    - see Gyuri's work on Trailmarks
        - [[sj]] - I think a good 80% solution for reconciling different types into a single namespace is to support [[TOPIC (qualifier)]], have it rendered while reading as just TOPIC, and have the link to [[TOPIC (qualifier)]] redirect to any of: "TOPIC", TOPIC (qualifier)", "TOPIC#qualifier" etc. which authority file can be updated by any editor of the markdown network (and may change as people take time to fill out nodes for increasingly specific variations on the topic).  
            - very similar to what i came to
    - [[flancian]] have been meaning to collect a list of repositories which we would like integrate into a shared construct (agora wink wink) -- do you have any?
        - [[peter kaminski]] massive wiki is agnostic w.r.t. versioning and sharing models (or tries to be)
            - for git, [[massive wiki]] can have submodules
            - [[massive wiki builder]] will build
        - do you have note repositories of your own, personal or otherwise?
            - [[peter kaminski]] have one but not currently shareable :)
            - AI: suggest we keep discussing this in future instances
                - [[sister sites]], sister pages
                - twin pages
                - interwiki
                - web rings :)
                - wiki [[collaboration primitives]]
                - Instant wikilinks / cascading wikisheets: implicit interwiki resolution (a la https://www.mediawiki.org/wiki/InstantCommons) :: make the local .cws legible so you can see the order in which your current interface looks for matching nodes in choosing the default interwiki 
                    - try variation that chooses cascade order based on length/quality of target node
                    - try interface variation that shows top N options in asymmetric list/pie
                - [[fedwiki]] is brilliant but the feeling of the room is that we don't fully understand it
                    - is there people building any kind of business providing fedwiki widely/easily?
                    - https://byname.wiki.conversence.com
                - sj: update vocab to distinguish meki from wiki 
      - #map [[coauthor]] https://coauthor.conversence.com
    - Q: [[sj]] how to capture third-party cross-wiki page-name-maps?   e.g. say we read together a dozen sources, which are not generally world editable, and are building (in a shared space) interwiki links + merge requests across the set of pages in those sources.
        - [[maparent]] this is what I meant by "glue" earlier, it's a core [[HyperKnowledge]] goal
- AIs
    - AI: start a [[tracking document]] for tracking pending interesting threads
        - done -> [[fotl threads]]
    - AI: Then let's do a pass collecting all useful links we already have in this node and in [[fotl]] and move them to [[fotl threads]].
    - AI: Let's move communications over chat for the above projects to the [[fellowship of the link]] channel by default, or share links there to other sources of truth.
    - AI: let's discuss wiki [[collaboration primitives]] and the potential of integrating independent note taking repositories/wikis a la massive wiki / agora
    - AI: add schema section to [[fotl threads]]
    - AI: upload recording to some well known location :)
        - [[bentley]] suggest putting the raw file in drive first

## 2022-10-19
- Attending: [[Jerry Michalski]], [[Flancian]], [[Chris Aldich]] [[Mark-Antoine Parent]] [[Peter Kaminski]] [[Jack Park]]
- First call on [[Wednesday]].
- (joined late.)
- [[Supermind]]
- [[Storyspace]] https://en.wikipedia.org/wiki/Storyspace
- [[Tinderbox]]
    - [[Mark Bernstein]] http://www.eastgate.com/garden/Enter.html
- [[Classification axis]] for [[tools for thought]]
    - [[Peter Kaminski]] -> [[massive wiki]] for this: https://dainty-sable-264aa3.netlify.app/project/project_plan
    - [[Mathew Lowry]] is working on the particular dimensions
    - [[Marc-Antoine Parent]]'s doc with dimensions: https://docs.google.com/document/d/1AY6y-uHUQE82zfLgwZLk29VPTaI1P5AMo6HT8zz1WDU/edit
    - Previous [[radar chart]]: https://docs.google.com/spreadsheets/d/1hY2V5NoSS713R2wzcjBE2q5KZIlfMOPFtL9g6Gaop_o/edit#gid=0
- [[Peter Kaminski]] on a tool called [Scrintal](https://www.scrintal.com/)
- [[Jack Park]] [[LiteNet]] https://docs.google.com/document/d/1m56SHPGgeFfB_3ToO9-VB9Yu266wtS5-9xlwaFeJ68k/edit
- [[Marc-Antoine Parent]]
    - [[Fermat]]
    - [[Tools for thought rocks]] https://lu.ma/tftrocks-oct22
- [[flancian]]
    - what could we do with what we already know, even with an incomplete map?
    - [[marc antoine]] [[hyperknowledge maps]] https://hyperknowledge.org/HyperKnowledge.mp4
        - we want:
            - [[deep hyperlinks]]
            - deep [[anchoring]] (new, a la [[web annotations]])
            - many to many relationships between anchors and entities
        - [[flancian]] we probably want this second level map for projects that are trying to work on interlinking 
        - preconditions:
            - backlinks
            - supple many:many relationships between anchor text and meaning
        - [[agora]]
            - [[interlinking]]
            - [[push]] [[pull]] [[go]]
        - [[maparent]] focusing on the differences:
            - [[deep backlinks]]
        - any single idea will be in millions of contexts, how to keep the graph "readable" 
        - attribution/degree of belief
            - surface surprising beliefs, beliefs that could be questioned
        - [[jerry michalski]] deck of patterns for cognitive biases
            - swipe right / swipe left? :)
        - [[jerry michalski]] real world example
            - half of the republicans running now *say* that the election was stolen
            - should this ideally disqualify them? 
            - #map ~ [[maparent]] we want to qualify belief by track record, e.g. the work of [[superforecasters]]
            - distinguish empty claims from testable claims
        - what's the minimum set of coordinated actions we could take to maximize the chances this great crowdsourcing effort happens?
            - hashtags/wikilinks as one way to coordinate -- but might not be enough?
            - [[chris aldrich]] the [[instagram problem]]
            - [[flancian]] the Agora tries to make it so that the community can cross-link oportunistically/share entities and auto link
            - [[maparent]] worried about ambiguity still regardless of whether they are autogenerated or human generated
        - [[chris aldrich]] on the recent controversy in US politics with racially charged comments by politicians
            - #map [[dao]] and [[smart contracts]] -- enforced accountability
            - #jm [[lexon]] as a human readable [[dsl]] for contracts
        - #map working on a plan and a prototype for [[hyperknowledge]]
        - [[chris aldrich]] how to push actors towards more precise speech (to counteract Trump's style of not saying anything but convincing some people he is aligned with them, even in the centre left initially)
        - two kinds of self organization:
            - self organization around a shared goal in a self-selected group
            - coordinated action in a very large scale


## 2022-10-14
- The band is back together! After a while :)
- Attending: [[jerry michlski]] [[aram zucker scharff]] [[chris aldrich]] [[flancian]] [[bentley]]
- [[jerry michalski]]
    - hope to see [[fotl]] be a guiding project for [[rel8]]
- [[check ins]] / what are we up to?
    - [[flancian]]
        - [[work]]
        - [[flancia]]
            - [[agora]]
                - [[pkg book]] -- just got back feedback 
                    - [[chris aldrich]]
                        - About the terms of the book: they're using an academic publishing model, very little benefit for the writers
                        - (Looks like the publisher is https://exapt.press)
                        - Chris is likely dropping out
                    - #jm if you were to create a version of this book that was more interesting, what would it look like?
                        - [[aram]] maybe doctorow-like?
                - [[agora]] 2nd anniversary on ~[[2022-11-15]]
    - [[chris aldrich]]
        - interested in [[cosma]]
            - (this led to a very interesting overview of promising tools)
    - [[bentley]]
        - list of [[tools for thought]]
        - [[canonical debate lab]]
            - [[debate tools]] ~ [[tools for thought]] in some perspective
    - [[jerry michalski]]
        - one week in a conference called [[unfinished]]
          - very interesting Brazilians, including [[Macul]]
          - [[keynote]] [[trust is the only way forward]]
        - [[lithuania]]
        - [[policy keys]] is trying to gamify policy discussions
            - deconstructing arguments into pros and cons
            - [[bottleneck issues]], [[hot issues]]
    - [[aram zucker scharff]]
        - mostly real life work since last time :)
        - work in the privacy space; GDPR, Virginia and California privacy regulations. Have been reading lots of documents.
        - spotted an interesting project
        - working on an archival tool for tweets, dealing with the issue that [[an increasing amount of people are deleting old tweets]], and also with styling issues
        - [[flancian]] maybe check out [[nitter]] code
        - wdyt about [[threader]] (app)?
- possible time/day of the week for the next call?
    - Wed at 10?
        - Aram: **11am** better
    - Thu?
    -> Mattermost


## 2022-09-16
- Attending: [[jerry michalski]] [[marc antoine]] [[mathew]] [[stacey druss]]
- #push [[canonical debate lab]]
  - [[maparent]] presents
  - [[argument technologies]] https://docs.google.com/spreadsheets/d/1wQShF0J3lGmIFACTvt5FLQWnKc1YdRaaCEDvRJlcUT8/edit?usp=sharing
      - map of [[tools for thinking]]
      - [[airtable]] approach, preferred structured to unstructured
      - knowledge management definition plan
      - [[jerry michalski]]
          - spider diagram
      - [[CI features and goals]] document: https://docs.google.com/document/d/1AY6y-uHUQE82zfLgwZLk29VPTaI1P5AMo6HT8zz1WDU/edit
          - seven dimensions
          - list of functional features
  - [[jerry michalski]] argumentation or debate as a view in an environment that facilitates collection, tagging and eventually policy making
      - grid making / dimensionality of the space we're exploring
      - [[flancian]] exploring a [[hypergraph]] as the target common data structure / exchange convention?
          - start with no typing, define required typing within the hypergraph (it's meta)
          - #push [[hyperknowledge]] https://hyperknowledge.org/hyperknowledge-components-1.html
  - classification / the meta problem
      - high dimensionality matrix 
      - [[mathew]] but who will want to do that kind of work? defining the dimensions, then actually filling in that sort of space
      - https://docs.google.com/spreadsheets/d/17cnrfNVwh_ETZDbfCIw-XV_t2zmwP2jJHCKUJIY0nGg/edit?usp=sharing
      - [[]]
  - [[syntax]] for modeling
      - paraphrasing each other
      - [[flancianization]]
      - [[mathew lowry]] [[change my mind]] analysis, [[change my mind reddit]]
  - #ml wdyt about [[you are not so smart]]?
      - [[marc antoine]] loved [[the enigma of reason]] #2017 
      - #jm https://bra.in/6qzdab
  - [[shared purpose]] as a prerequisite for collective meaning
      - "why do you believe this"
      - [[stacey]] flexibility: it's important to not have to attach something in precisely the right point
      - also: when you put the arguments in the map, I'm answering an abstract position (represented in the map) that is not necessarily that of a particular person (so it gets defused)
  - #jm [[fake lie detector]] in [[the wire]]
      - it might be possible to identify what someone is saying in real time
      - reduce the delay between utterance and fact check
      - live scoring would help
      - #ml [[ministry of truth]] ~ [[map]] as a risk
      - #map [[cdl]]'s plan is to organize claim information; #map wants to provide a sort of [[claim overlay]]
  - truth roots
  - adversaries, [[drake equation]]
  - #push [[canonical debate lab]]
      - [[white paper]] https://github.com/canonical-debate-lab/paper/blob/master/README.mediawiki
      - [[democracy earth foundation]]
  - [[forgiveness]]
      - [[building bridges]]
      - #jm [[reconciliation commission]] for companies, [[truth and reconciliation]] process
  - [[election fraud]] claims
      - [[stacey druss]] looked into the cases behind the claim, case by case, and found that there were cases were people were being hurt and that we could have helped
  - #jm my notes for this call: https://bra.in/3qaEeE 
      - https://sfpeace.org/
  - #map
      - [[deliberate polling]]
      - [[the enigma of reason]] -- when people talk together, we get better results
      - recursive approach, exploit alpha/delta
 
  
      
 

## 2022-08-26
## Attending: 
- [[Gene]] [[Jerry Michalski]] [[Flancian]] [[Chris Aldrich]] [[Bentley]]
- Late: [[Aram Zucker-Scharff]], [[mathew lowry]]


### Videos

### Notes
- Introductions!
- [[jerry michalski]] ~ #jm
    - on previous calls
    - on sometimes having overlap in different dimensions but not having shared clarity/understanding
    - sharing clarity vs rambling
    - happens even at the organizational level when you're trying to set up a mission statement
        - [[motherhood statements]] ~ "we believe in X", "we believe in Y" -- but we're usually looking for nuggets of novelty
    - [[numenta]]
        - would like to jump into a "digested format"
        - [[prediction framework]]
            - as [[society of mind]]
- #push [[Gene]] and [[Jerry Michalski]] go way back
    - [[system thinker]] -> [[storyteller]]
    - #go https://bra.in/8vGe9q
    - married and divorced [[the brain]] multiple times
    - uses [[napkin]]
    - [[richard maxis]] ~ [[richard macksey]], former Johns Hopkins University professor with a large personal library
    - #push [[richard macksey]]
        - [[library background]]
        - https://app.thebrain.com/brains/3d80058c-14d8-5361-0b61-a061f89baf87/thoughts/34f84a89-4bc2-46f5-ac9b-b3ba8e8bff11/notes
        - https://www.youtube.com/watch?v=4rvXUHI331k
        - [[umberto eco]] https://www.youtube.com/watch?v=Czc_KjWji8E
        - [[library tours]]
- Spider chart example
    - reusable ethical services might be a competitive advantage of tools in the [[commons]]
    - commercial tools seem to have an advantage in the current market -- they get the backing of the market "leads" (VC, etc.) which lets them out-compete freer options
        - uber is not a [[fair marketplace]], yet it outcompeted more ethical alternatives
        - on the [[hypocrisy]] of "fake markets" -- platforms that behave like markets but are controlled by a single entity
            - #push [[fake markets]]
                - https://bra.in/8vBe4W
    - [[chris aldrich]] ~ #ca if we did [[spider graphs]], how do you select axis to focus on?
        - how do we present this information in a way that prioritizes the ethical aspect, and perhaps helps tool developers prioritize lacking dimensions?
        - #jm selecting dimensions in different contexts
        - #jm finding which tools are missing, which tools are complementary
            - "which tools play well with each other"
        - #ca another thing which is important to people in this space: even though [[obsidian]] is not open source, people find it easy to develop against it and it's got open source extensions
            - so it seems unlikely they will turn into a new Twitter
            - but even in that case it seems you could move to other players which are more open
    - [[bentley]] implemented [[filtering]] in [[spider graphs]] (demo)
    - #jm what is [[indieweb]]'s perspective on convincing people to build openly?
        - #ca #push [[indieweb]] they have built a structure on a two prong idea:
            - you own your own domain name
                - [[flancian]] ~ #f what about weakening this into "you own some URL space"
                - #ca it's possible, but at the end of the day you want to own what a URL resolves to
                - the ecosystem is developing in the direction of letting you redirect between domains
            - you have control over your data
            - #jm what about separating data from apps, e.g. storing on github?
                - as in, you map any new tool to the same existent dataset
                - #ca you can point tools in [[indieweb]] to repositories of data
                - #ca #push [[micropub]] is a spec; a "data plug board" that allows people to easily write apps that publish events to different consumers
                    - #go https://www.w3.org/TR/micropub/
                    - a post goes first to your website
                    - then the website has the know how on how to publish to feeds
                    - [[bookmark service]] is the [[hello world]] here
                - [[medium]] could rewrite its backend to support [[micropub]] and it would let you cross post to many other sites
                - #f how does this interact with [[activitypub]]?
                    - #ca it fits in this model but it's a steeper learning curve
                    - in most of the AP space, if you don't interop with [[mastodon]], you don't exist
                    - lots of tools target [[mastodon]] as it supports some core things well
                - [[aram zucker]]
                    - guide to [[activitypub]]: https://tinysubversions.com/notes/reading-activitypub/
                - #push [[fotl agenda]] 
                    - the field of [[x clone]] in the [[fediverse]]
                    - no single AP client that supports all features
                    - [[lemmy]] as an interesting example of new platform built on [[activitypub]]
                    - [[goodreads]] functionality
                        - #ca https://indieweb.org/personal_library#Silo_Examples
    - back to meta level here?
        - on mapping of the fediverse, of tools?
        - or [[spider charts]]
            - #f [[go/t4t radar]] points to the chart (- and + also work for spaces)
                - which categories do we want here?
                - linking articles to support scores/opinions
                - #f [[assertion feeds]]
                - #jm spreadsheet is easily embeddable to begin with
                - #ml publishing markdown/resources to repositories and sharing that
            - #f [[gardens]] and [[feeds]]? :)
            - #ml can we add domains/repositories to what is searching?
                - #f yes
            - [[aram zucker-scharff]] ~ [[az]]
            - #jm [[noosphere]]
            - #ca most of the big commercial offerings allow people to store data on [[dropbox]] or [[google drive]]
                - [[agora]] could enable people to move from [[dropbox]] to [[git]] based workflows
                - micropub spec ostensibly could be used for moving from platform [[x]] to platform [[y]]
    - [[solid]] and [[solid like]]
        - [[mathew lowry]] ~ #ml
        - [[mysilio]] https://github.com/mysilio-co
    - [[jerry michalski]] will host a [[podcast]]
        - default topics:
            - [[startups]] to motivate a [[bootcamp]]
            - [[chris aldrich]]
            - who else should we invite?
                - [[anne laure]]
                - [[maggie appleton]]
                    - [[anthropology]] [[history]] background
                - [[andy matuschak]]
                - [[cory doctorow]]
                - #list https://twitter.com/i/lists/1437865198346379264/members
            - [[commons]]
                - [[knowledge commons]]
                - #ml [[global commons]] usually means [[global english commons]], although that can be generalized with AI
                - "[[The Eighth Coalition]]" http://en.wikipedia.org/wiki/Hundred_Days
    - #ca [[lukasa]] as materialized [[method of loci]]
        - [[pacific navigators]]
        - [[steam ships]] as bad for lifeboats because people lost knowledge on the working of [[currents]]
        - [[Lifeboat]]: A History of Courage, Cravenness, and Survival at Sea (2003) 
        - For more on pacific islanders' migration: [[Life on the Rim]] (as in Pacific rim) 
    - #meta #ml let's set up a [[doodle]]?
    - ([[flancian]] dropped here.)
- (A copy of the default Agenda goes below)
- [[names]] for the project that has already started :)
    - [[flancian]] my proposal is, well, you know what I call it :)
        - would love to discuss [[agora protocol]] with you
            - is the heart of the [[Agora]]
            - it is what you and me define it to be :)
            - feedback welcome :)
- where are you [[feeds]] and [[gardens]]?
    - [[flancian]] note my daily feed shows up as part of https://anagora.org/journals which is an aggregation of daily posts by all users, 
    - if you tell me about your feeds and gardens I could add them (like everything Agora related, everything is optional always and offered as a token of friendship!)
- [[commonplace books]]
- [[mathew lowry]] let's create some distributed map of thinking tools: https://chat.collectivesensecommons.org/agora/pl/78gprua18frkpc6shrxabricqo
![](https://doc.anagora.org/uploads/upload_888c6fbb5753be41ddb48290c35d505d.png)
    - #jm https://bra.in/5qeDMg
    - #jm [[spider charts]]
        - looks like a [[polar chart]]
        - what are the axes? visualization, openness, artificial intelligence, etc.
            ML: also the different notetaking techniques
            CJA: What are the building blocks and affordances they provide so one can have a progressively improved/complex experience
    - ![](https://doc.anagora.org/uploads/upload_4735686c23bc31c6dcf2b9e44eeeed00.png)
    - https://docs.google.com/spreadsheets/d/1hY2V5NoSS713R2wzcjBE2q5KZIlfMOPFtL9g6Gaop_o/edit#gid=0
- solving for [[sustainability]] / [[viability]] of a healthy knowledge ecosystem
    - funding, donations between readers and writers
    - nested conversations, how to solve for:
        - [[communities]]
        - [[startups]] / companies
            - [[jerry michalski]] camp
- People we should invite here?



## 2022-08-19

### Attending
[[Flancian]]
[[Chris Aldrich]]
[[Jerry Michalski]]
[[Mathew Lowry]] 
[[Dan Whaley]]

### Video

### Agenda 
- [[2022-08-19]]: recap of Render Conference for Tools for Thinking https://www.betaworks.com/event/render-tools-for-thinking
    - done!

### Notes
- [[jerry michalski]]
    - [[render]] ~ [[tools for thinking]]
- [[flancian]]
    - great introduction
    - great conversation with [[howard rheingold]]
    - amazing announcement by [[gordon brander]]: [[noosphere]]
        - it is [[an agora]], done very well!
- [[jerry michalski]] welcomes [[dan whaley]]!
  - [[dan whaley]]
      - Fridays are much better meeting wise!
      - very busy but 
      - [[14 million dollars]] investment from [[ithaka]] and [[jstor]] https://web.hypothes.is/blog/say-hello-to-anno/
  - how does this interact with the global [[knowledge commons]]?
      - [[annotations]] -> the knowledge is in the annotation you take
      - but the annotation is layered on preexisting on knowledge
      - it's about protocols and things but also about seeding [[communities]]
  - [[hypothesis]] cares about the user having access to the underlying knowledge
      - regardless of whether it's because it's free or they happen to have (exclusive?) access
      - this knowledge could be resolved in a federated network
          - clients using open protocols like [[web annotations]] can participate in this network
      - [[flancian]] how does this relate to [[markets]]?
          - and the fairness of said markets.
          - IMHO [[commons]] should [[embed]] markets
          - [[dan whaley]] the knowledge is what's "out there" right now, we try to pass no judgment and support the existing models
              - most universities have access to [[json]], but most others don't
              - the [[nyt]] is not free
                  - > paywalls
              - some content might always be gated
              - the world may be moving towards [[free access]] but that will happen on its own terms?
              - [[hypothesis]] thinks there's a sustainable path for them; charging for institutional usage maybe but making the conversation available to everybody
                  - not doing ads
                      - -> [[reality distortion matrix]]
                      - silos trying to [[monetize attention]]
                  - constructive ways of funding
                  - open [[saas]]
       - [[mathew lowry]] have you watched [[render]] / [[tools for thinking]]
           - [[dan whaley]] not yet!
           - [[mathew lowry]] interesting ai potential exploration
           - what are your thoughts on integrating AI with hypothesis?
               - "here is what your friends think about X in the web" vs "here is what an AI thinks about X in the web"
               - [[dan whaley]]
                   - AI is super interesting as created by humans for humans
                   - a force for good to help us navigate the world more powerfully
                   - but of course there are negative use cases, so we need to set the right incentives
               - [[flancian]]
                   - may not there be a difference in the long term? :)
               - in terms of influencing AI
                   - (... saw something in chat :))
               - mathew: valuable content layered on top of layered content.
                   - -> sentiment analysis and meta sentiment analysis
                   - people benefiting from the AI they train instead of the current status quo
               - [[dan whaley]] very privileged to have access to this data, and to steer a new paradigm
                   - find revenues that can sustain this while being pro social is critical
                   - only will explore what will be beneficial
               - [[jerry michalski]]
                   - [[douglas tomkins]] (sp?) and [[x]] from [[patagonia]]
                   - building land tracts and are trying to turn it into a trust
                       - (!)
                   - is there one ambitious funding project that could be explored for maximum benefit here?
                   - could we fund the [[idea commons]] on some large, ambitious scale?
                       - [[flancian]] using the commons, regulating markets, to disrupt the market for public good
                   - [[dan whaley]] what is the change we want to make?
                       - you could imagine all kinds of things
                           - one idea: how could you incentivize people to make annotations professionally?
                           - meaning high quality "trailblazers"
                           - proposed legislation
                           - pre annotating bills!
                           - what would it take to be able to fund this
                       - concept of [[reddit gold]]
                           - chip in to providing high quality contributions?
                       - fixing the [[newspaper subcription model]]
                           - you put 10 bucks in, it goes to the authors of the things you read
                           - [[jerry michalski]] reinventing [[xanadu]] in a way
                       - [[jerry michalski]]
                           - the large pot of money (a risk in itself, but) can be distributed
                           - [[dan whaley]] it's a flow
                           - like mycellian nutrients
                           - [[flancian]] meta on the metaphor
                           - [[chris aldrich]] [[redwood trees]] network roots to be able to stand up taller
                               - for most trees, they tend to be mirror images
                               - not so redwoods
                       - [[data trust]]
                         - [[chris aldrich]] how to get good quality data in general  
                             - [[twitter]] is already a great repository of annotations in a sense, but you have to sift through a lot more stuff to go to the gems
                             - [[jerry michalski]] [[nugget ratio]] is very high if you curate your follows
                             - [[flancian]] -> the [[social network]] is what encodes the most information
                                 - the importance of [[open ranking]], [[open filtering]], [[open algorithms]] -> [[open ais]]
                             - [[jerry michalski]] why are [[tools for conversation]] not [[tools for thinking]]?
                                 - the lack of good permalinks in interesting answers in random forums
                                     - walled gardens
                                 - one of the nice things about hypothes.is is that it's got a great signal to noise ratio and you can easily link to full contexts
                             - [[indieweb]] is important here
                             - [[mathew lowry]] [[myhub]] is part of [[indieweb]]
                                 - on the following relationship
                                 - as leading to flows -> (of attention, of funding)
                             - [[flancian]] hypothes.is integrations with [[feeds]]? it already provides feeds, how important they seem to you
                                 - [[dan whaley]] we provide feeds but are not currently looking at providing more
                                 - focusing on providing arbitrary annotation for arbitrary web resources
                             - [[chris aldrich]] how do you also not aggregate streams only, but how do you turn those feeds into something feedin a [[garden]]
                                 - [[how to feed the garden]]
                                 - [[robin sloan]] (...) (sp?)
                                 - [[mike oldfield]] [[technopastoral]]
                                 - #push [[technopastoral]]
                                     - https://myhub.ai/items/the-garden-and-the-stream-a-technopastoral-hapgood
                                     - https://hapgood.us/2015/10/17/the-garden-and-the-stream-a-technopastoral/
                             - how do you pick out "tweets" and curate them into something?
                                 - [[flancian]] -> you start by linking them more
                                     - [[wikilinks]]`
                                 - [[jerry michalski]]
                                     - balance the [[stocks]] and [[flows]]
                                 - [[mathew]]
                                     - https://medium.com/the-mission/why-you-need-a-personal-content-strategy-ff05c84fccfd
                                     - [[gardens, not graves]]
                                 - http://www.wsj.com/articles/the-future-of-the-internet-is-flow-1443796858
                                 - [[jerry michalski]] the issue with preventing remixes and other limitations on creativity
                                     - -> [[everything is a remix]]
                                 - [[dan whaley]] whole advertising industry is based and capitalizes on [[flow]]
                                     - no ads on [[stocks]]
                                     - fresh content mesmerizes us
                                     - the fascination of time
                                         -> [[flancian]] claiming posts/items from a feed and storing them filed, with a human readable permalink, anchors them; brings them out of the [[flow]], makes them [[evergreen]]
                                 - [[mathew lowry]] exploring this in the [[pkg chapter]]: how to build a [[pipeline]]
                                     - [[flancian]] #do tell [[st]]
                                     - transformation is something people could want to pay; new formats for resources
                                     - "follow the flow into new stock"
                                         -> [[flancian]] the advantage of the hub aspect of an integrated system, efficiency
                             - [[dan whaley]] delighted to have been able to meet! hope to be able to continue to participate.
                                 - Congratulations!!!
                             - [[mathew lowry]] annotating on annotations, transforming 
                             - [[jerry michalski]] writing linked content, sharing using emergent conventions
                                 - a path to help and prototype together
                                 - [[networked scribing]]
                                 - we're in the early days of cinema, we're still looking for the [[dolly]]
                                 - the web is stuck on web 1 metaphors
                                 - corporations hve been trying to centralize and define the asthetics and the ethics of the system
                                 - [[chris aldrich]] song lines from indiginal (sp?) cultures
                                     - they inform who we are today, but we mostly ignore this
                                     - a space in this new space to bring us closer to the spoken word and new ways of communicating
                                     - the web becoming more visual / photo centric anyway
                                     - what about the music, the dance, the art
                                         -> [[flancian]] [[bolo bolo]]
                                 - [[dan whaley]] agree with this
                                     - [[i annotate]] talk on the future of note taking
                                     - [[ward cunningham]] was there
                                     - folks from [[logseq]] were there
                                 - [[dan whaley]] developed [[docdrop]] to annotate youtube videos
                                 - [[dan whaley]] https://www.youtube.com/watch?v=GThr77PbJ4w ->  https://docdrop.org/video/GThr77PbJ4w/
                                     - [[flancian]] [[agora]] the right spirit, not the right software yet :)
                                     - [[ward cunningham]] [[fedwiki]] 
                                     - [[roam]] et al is very proprietary
                                         - the opportunity is fully distributed, they don't seem to get it
                                         - [[mathew]] reminds me of the twitter missed opportunity 10 years ago
                                     - [[obsidian]] could be nudged in the right direction
- "we're trying to start a project"
    - what if we already started it? see agenda for next time :)
    - [[jerry michalski]] ~ #jm
        - registered [[the big fungus]]
    - [[flancian]] you know what I'm going to propose :)
    - [[chris aldrich]] [[commonplace books]]
        - #jm were they only personal or also social objects?
        - people would keep their own commonplace book and go in the will to someone else
        - [[the book nobody read]] about [[copernicus]] and [[revolutions]]
            - [[flancian]] -> [[david deutsch]]
            - [[student notes]] passing through the ages
            - [[marginalia]]
            - [[torah]] annotations
        - [[scrapbook]] flipped in meaning
            - [[commonplace books]]
    - [[jerry michalski]]
        - [[spider charts]]
        - [[chris aldrich]] data visualization/rendering services
            - [[flancian]] in a federated network
        - [[mathew lowry]] identifying complementary tools

### Agenda
- Tools for Thinking Recap https://www.betaworks.com/event/render-tools-for-thinking
    - https://etherpad.indieweb.org/ToolsForThinking
    - Jess Martin's notes: https://jessmart.in/articles/render-recap
- [[flancian]]
    - where are you [[feeds]]?
    - mine is in https://anagora.org/journals which is an aggregation of daily posts by all users, if you tell me about your feeds I could add them there (like everything Agora related, everything is optional always and offered as a token of friendship!)
    - [[agora protocol]] -> moved to next week
        - is the heart of the [[Agora]]
        - it is what you and me define it to be :)
        - I have bootstrapped it to be markdown plus wikilinks, wikilinks being descriptions of entities in a free knowledge graph as common [[language]]
        - feedback welcome :)





## 2022-08-11

### Attending
[[Jerry Michalski]] [[Mathew Lowry]] [[Chris Aldrich]] [[Aram Zucker-Scharff]]

### Video
today's FoTL call is up, Unlisted: 
https://youtu.be/fBOfMKtBpss and 
https://youtu.be/i0Tty7TIaWI 

### Notes
Jerry's brain for this session: https://bra.in/6p63ZP

- [[betaworks]] conference: https://www.betaworks.com/event/render-tools-for-thinking
- [[Mathew Lowry]]
    - WordPress plugin to syndicate news orgs from multiple sites of different languages 
    - Would be useful to give publishers more to cite and a better understanding  
    - A type of shared memory 
    - Hard to get journalists to adopt the tool
    - A bunch of different organizations sharing the tools for mutral benifit. 
    - From Mattermost - https://chat.collectivesensecommons.org/agora/pl/gbonf7z177yquffqz59mu8uino :
        - The basic idea was to create CMS plug-ins for newsrooms which would allow journalists in different participating newsrooms to access each other's content, both published and otherwise (ie, drafts, notes, etc.), via their CMS. The  participating newsrooms essentially become a sort of decentralised press agency. This is particularly interesting in Europe, where every newsroom cannot have a journalist in every country. Hence the system would incorporate machine translation, autocategorisation and autosummary. Obviously, every time newsroom A used newsroom B's content - ie A translated and republished B's article into their own language for their own audience - newsroom B would earn credit. And every time B used A's, they would spend that credit.
        - This is a very specific use case, with a business model, for decentralised sharing. And the social benefit is real, because it would set up a decentralised alternative to the big press agencies and allow stories which they will never pick up to travel across borders and find new audiences. 
        - ![](https://doc.anagora.org/uploads/upload_93d18a7e1ef02e22c9e6482dd39300c8.jpg)
        - ![](https://doc.anagora.org/uploads/upload_f52edad0579e3a487bf2d8b201765b49.jpg)
- [[Aram Zucker-Scharff]]
    - https://restofworld.org/ 
    - Old version of [[Zemanta]]
        - A blog post "enhanced" by Zemanta https://hacktext.com/2011/02/what-is-a-text-and-how-do-i-hack-it-521/ 
        - https://static.packt-cdn.com/products/9781849511407/graphics/1407_02_15.jpg 
        - Eventually purchased by Outbrain and killed
    - https://www.distributedmedialab.com/publishers 
- Potential space for this [[WordCamp for Publishers]] https://twitter.com/wcpublishers/
    - Great event, highly recommend! - Aram
- There's the https://knightlab.northwestern.edu/projects/ that is really great. 
- Chris
    - The NYT has a digital archive team of about 3
    - Photos are not fully backed up there
    - 2 decades of working on the problem and not everything is backed up. 
- Mathew
    - The European Commission relies on the Internet Archive for websites they no longer wish to maintain. 
- Jerry
    - YouTube has its own storage problems stuff is not well archived. It is remarkable that they even capture what they can. 
    - The future digital anthropoligsts what will they find?
- Aram
    - Archiving should be something anyone can do and have on their own site 
    - Just like [POSSE](https://indieweb.org/POSSE) there should also be link once and archive yourself 
    - These systems should be able to talk to each other and share and replicate their resources
- Jerry
    - How does this survive though? My hard drives don't survive me 
- Chris
    - We have this problem with music - we saw how a lot of that music got lost.
    - Tip of the iceburg - so much history is lost 
    - music notation didn't exist in printed forms until about 11th century
- Jerry
    - In Small Things Forgotten 
    - Gravestones are very useful for history. Also potery. 
    - Tiny differences in gravestones over time are fashion trends that are time indicators. 
- Aram
    - I think in terms of preservation we can look at Activity Pub. When you federate with another server it pulls and replicates and distrubutes stuff. It would be great if we could get that done with archives. 
    - Open sourcing is good as well
- Mathew 
    - If you link to something you automatically make a backup is a good idea
    - What does this have to do with content sharing? 
        - https://en.wikipedia.org/wiki/Content-addressable_storage
        - http://open-content.net/caw
        - One peice of content can be shared out replicated and shares an address across many locations.
- Smallest Federated Wiki 
- IPFS but pinning is an issue. 
- Collective intellegence - what that means for spread and maintenance 
- Songlines Are the Original Blockchain - https://bra.in/5jQYgm
- Jerry
    - A lot of ways of remembering were intentionally destroyed by colonization 
    - [[Songlines]] are an example of that
    - but it turns out that these ways of handling it are important.
    - Local populations carefully crafting things and being overwritten by colonization. 
- The Biggest Estate on Earth: How the Aborigines Made Australia (2011) 
- Chris
    - [[David Christian]] on [[collective intelligence]]: The beginning of collective knowledge and intellegence as the marker for the beginning of human history. 
-  Jerry
    - Christian talked about how there are not hooks in the work to be able to pull his data out of his finished thesis. 
    - Humans are really good at killing themselves off and then passed down the ways they learned not to. 
- How practices spread and disceminate? 
- We overvalue the written world - Jerry. 
- Mathew
    - An overvalue of memorization 
    - Greeks overvalued it and that was the end point of oral learning. 
- What does a non-literary method look like here? 
- Aram:
    - [Queens Memory](https://queensmemory.org/) - Podcasts as a method of oral history 
    - Memes and emoji as inconographic languages 
- Jerry
    - There are others as well like NPR's project here that do podcasts for oral histories 
    - [[The Alphabet Versus the Goddess: The Conflict Between Word and Image]] (1998) 
- Aram
    - https://en.wikipedia.org/wiki/Linguistic_relativity
    - http://en.wikipedia.org/wiki/Sapir-Whorf_hypothesis
- Chris
    - Interesting project to 'write' coreography in a way that isn't the standard way of transmitting coreography
    - https://en.wikipedia.org/wiki/Dance_notation
    - Different ways to lay out colors an images to annotate video - how could you have a recorded record that could be used to recreate a movie from the notes. 
- Graphic facilitators 
- Mathew
    - volcano model for desktop information - starts in the center and slowly flows towards the sides until it falls off the desktop. 
- Aram
    - Reminds me of 3d desktops
        - ![](https://doc.anagora.org/uploads/upload_43742f2c6167180e0f75a72217f54e4e.png)
- Jerry
    - [[Songlines]] on the desktop 
    - Grapiphic facilitation at conferences 
    - Point back at stuff that was written on the wall from a previous day. 
    - What would The Brain look like as the file system for an operating system. 
    - synecure
- Aram
    - Archiving as a regular personal practice 
- Chris
    - References of people who value their knowledge so they protect against it being lost to history. 
        - These bound books over here with all my notes take them out of the house 
- Jerry
    - Tools for thinking - https://app.thebrain.com/brains/3d80058c-14d8-5361-0b61-a061f89baf87/thoughts/4bfe6526-9884-4b6d-9548-23659da7811e/ 
- https://scalingsynthesis.com/
- Scaling Synthesis - Multiplayer TFT https://lu.ma/9a21amd7 from 2022-08-09 video should be available shortly from [[Boris Mann]] et al.
- Should we write a database of these things or should we poll people and publish interviews? What tools do people recommend?
    - Good example: https://indieweb.org/commonplace_book 
    - Would be good to hear from people: 
        - I have this practice 
        - this  is how I use it 
        - this is what it looks like 
        - and this is how I turn it into outputs? 
    - Looking at how people use their information graphs and how they visualize information 
    - It would be really valuable to me to know if I want a good graph this is what it looks like 
    - Why isn't there more documentation of these tools and how could it lead to interoperability 
- Chris
    - Even the history of the tree space isn't as well known or broadly distributed.... 
    - Lima, Manuel. [[The Book of Trees]]: Visualizing Branches of Knowledge, 2014. 
        - https://papress.com/products/the-book-of-trees-visualizing-branches-of-knowledge 
        - Jerry: in my brain - https://app.thebrain.com/brains/3d80058c-14d8-5361-0b61-a061f89baf87/thoughts/cff5e4d0-94af-70a0-d710-d324cbdd55e6/ 
- Jerry
    - Could we have a [[pattern language]] for this? 
        - http://en.wikipedia.org/wiki/Pattern_language
    - Ex: Light from Two Walls can become a shorthand for talking about loose rules that trigger understand and contextualization. 
    - Ex: [[1 2 4 all]]
        - [Jerry write up of instrumenting](https://wiki.rel8.dev/tile_-_1-2-4-all_zoom_app)
- Mathew
    - Is there a syntax or thesouras for pattern languages
- Jerry
    - Patern Languages of Pattern Languages
        - https://www.hillside.net/plop/2022/ 
    - Chatbots maybe a solution?
        - Hey I'm intersted in Starting with Tools for Thinking
- Aram
    - Maybe just a question and answer page?
- Jerry
    - And then you could feed it into a Chat Bot
- Mathew
    - How do we help people find the right tool for them
    - How do we help people find the right pattern langugage for them. 
- Aram
    - It seem swe have to interview people first and get them to talk us through it. 
    - Do we need a questionaire? 
- Jerry
    - a smorgasbord of thinking tool users' preferences
    - There is some skill required to pull people out of their over-complexity.
- [ ] questionnaire for thinking tool users? 
    - What are you using this tool for and why? 
    - What did you wish your tool suite did? 
    - In the note taking space a lot of people don't think out the longg term value 
    - Creating one or two notes a day over a year before the big affordances become obvious 
    - what is the long term value of your tool suite and process? 
    - create a 3 minute video of your most typical use case 
        - UX Studies Practice here ?
            - Narrate yourself through the proceess and what you are thinking 
- Chris
    - Very few people get to the 3 or 4 month mark where they see pay off from notetaking.
    - Not many people are writing about it as a benefit either. 
- Mathew
    - We need to use the 5 why technique - we need to ask why a lot
    - Not everyone wants to use notes for creation, some are just collectors. 
- Chris
    - Some people have collect a lot of stuff as the only goal and then the assumption is that [[note taking magic]] happens, but that isn't really the case. 
- People find a system and then want to sell it and that can be a problem
    - [[GTD]] aka [[getting things done]] is an example here
    - [[nick milo]] and [[linking your thinking]] https://www.linkingyourthinking.com/
- [[Memory]] and [[major system]] https://en.wikipedia.org/wiki/Mnemonic_major_system as a historical example of people selling intellectual systems or frameworks. This is playing itself out again with note taking tools.
- https://boffosocko.com/2022/06/10/reframing-and-simplifying-the-idea-of-how-to-keep-a-zettelkasten/
- Critiques of Learning Styles https://bra.in/2q5oKV
- [[design from trust]] designfromtrust.com 
    - Universal Benefit
 


## 2022-08-04
### Agenda
- Shared memory / collective learning
    - [[collective knowledge]] [[shared knowledge]]
- how the agora has an advantage over platforms (Flancian)
    - [[wikilinks everywhere]] <-> [[hashtags everywhere]]
    - [[adversarial interoperability]]
    - -> AI(flancian): post about this in [[ogm]]
        - [[Jerry Michalski]] do the simplest thing that can possibly work sounds good
    - AI(flancian): let's invite [[dan whaley]] here again?
- [[meta]] how to have a more structured agenda

### Attending
[[Jerry Michalski]] [[Mathew Lowry]] [[flancian]] [[Chris Aldrich]]

### Notes
- [[Jerry Michalski]]
    - [[betaworks]] render event next week about [[tools for thought]] [[2022-08-16]]
        - [[nyc]]
        - https://render.betaworks.com/thinkcamp-a-betaworks-accelerator-program-for-tools-for-thinking-de7e18bf5682
    - how to get a [[posse]] working together
    - [[chorus of voices]]
- [[internet slowness]]
    - [[van jacobson]]
    - https://en.wikipedia.org/wiki/Van_Jacobson_TCP/IP_Header_Compression
- on [[conventions]]
    - [[lower caps]] vs [[initial caps]]
        - eventual fixup
        - eventual convergence :)
    - inclusivity aspect of it: be liberal w.r.t. what you take
    - [[Mathew Lowry]] myhub does the same, lowercase by default everywhere. Based on my (poor) experience with Roam.
    - arguments for/against
        - [[lower caps]]
        - [[initial caps]]
            - more readable
            - the cost of writing caps is helped by tools like [[obsidian]] auto completing links once you type \[\[
        - [[Chris Aldrich]] about unicode coalescing (there's a better word for this) in both directions, pros and cons
            - (...)
            - very used to writing in caps anyway
            - ex: platforms like instagram show how people "exploit" hashtags by using many similar ones to have greater reach
            - a platform could actually coalesce hashtags
                - [[triangle thinking]] ~ [[combinatorial creativity]]
- [[Jerry Michalski]] operationalizing communal note taking in preparation for [[betaworks]]
    - how do you do note taking?
        - [[Chris Aldrich]] almost on git but not currently
            - most of the public stuff starts in [[hypothes.is]]
            - notes in hypothes.is have permalinks
                - actually have two URLs:
                    - one for the page/resource you annotated followed by a trigger for hypothes.is to open and show the annotation in context
                    - one in the hypothes.is domain which refers to the actual annotation proper
                    - "[[js;dr]] problem"
                - [[Jerry Michalski]]
                    - you can share a highlight to a passage using the current #... convention
                - https://indieweb.org/media_fragment (thanks!)
                - https://www.w3.org/TR/media-frags/
                - hypothes.is reads the tags and uses it for presenting annotations/highlights
                - https://www.w3.org/annotation/
                - https://www.w3.org/TR/annotation-vocab/
                - Research on various annotation implementations created by Hypothes.is: https://docs.google.com/spreadsheets/d/1f86L7vgHUW9wSLNNSunhjmtxtg6KlCOVpHGKbqUzW-Y/edit#gid=0
- [[jerry michalski]] on 
    - #push [[how people think]]
        - https://www.collaborativefund.com/blog/think/
    - how could we bridge these numbered 1 .. 17 aspects with:
        - notes about the same in other note taking systems
        - hypothes.is annotations on those sections
    - [[mathew lowry]] which level of granularity do you use for your notes? resource/concept/etc. 
        - how to map one to the other?
        - [[jerry michalski]] call this the [[nugget problem]]
        - [[chris aldrich]] [[nugget size]] vs [[zoom levels]]
        - [[jerry michalski]] 
            - [[ted nelson]]
                - [[stretch text]] ~ [[StretchText]] (1967)
                - [[hypertext fiction]]
                - AI(flancian): tell [[armengol]] about this, he was working on something related.
            - Q: is there typing in [[thebrain]] or some other way to distinguish nuggets from e.g. full resources?
                - it could encode this but the way Jerry uses it loses this information
                - Jerry does not use some features just because they slow him down / they take a lot of time
                - [[Mark Trexler]] uses more of these features and is a [[climate change]] expert.
            - [[chris aldrich]] the labels/wikilinks that you used for these are unlikely to be the same other people use.
                - (but once these are known to all be in a particular resource...)
                - [[google search]] including fragment lookup in search results in some sites
                    - engineering focused solution
                - (on striping tracking data from URLs)
                - [[building blocks]]
                    - if it's online, there'a permalink to it somewhere; that's a starting point
                    - [[media fragments]] to dig into text, video, audio
            - [[rel8 pioneers]]
                - where to [[meet]] in this notion of [[idea sex]]?
                    - [[schelling point]]
                        - where would we go in the internet if we couldn't pass information about the place?
                - which places, which formats?
                - [[chris aldrich]] [[permalinks]] and [[wikilinks everywhere]]
                    - negotiating equivalence between wikilinks in different repositories
                    - -> [[agora]]
                    - [[peter hagen]]
                        - #push [[lindy annotations]]
                            - https://annotations.lindylearn.io/new/
                    - #push [[crowdwise]]
                        - https://chrome.google.com/webstore/detail/crowdwise/hogoebkpcnajkkjdidfhojkljppfalip
                    - personal [[agoras]]
                        - providing entity resolution, entity coalescing, annotations
                        - a context in which to resolve wikilinks to permalinks
                    - [[optimistic linking]]
                        - wishful thinking with dangling links
                    - [[mathew lowry]]
                        - fedwiki for working on convergent links/pages
                        - [[chris aldrich]] creating [[red links]] (in wiki terms), it would be nice to be able to get resolution paths whenever one is clicked (resolve this in X, Y or Z)
                        - [[jerry michalski]] the autocomplete in obsidian could be extended to resolve in expanding circles
                            - #push [[patterns]]
                                - #127 [[intimacy gradient]]
                    - [[mathew lowry]] "a tool that lets me curate my content according to my social network" would be super powerful
                    - [[chris aldrich]] [[google plus circles]]
                        - how to incentivize a company into a non profit motive, or a low profit motive, so they can be trusted
                    - [[bonfire]] https://bonfirenetworks.org/
                    - #push [[agora]]
                        - is about [[resolving]] with [[trust]]
                - [[ai]] ~ [[artificial intelligence]]
                    - communities building corpora
                    - [[mathew lowry]] and setting up a [[dao]] to steer resulting models
                    - or [[disco]]
                - [[jerry michalski]]
                    - tweets if they were connected more tightly with the internet
                        - they could embed anchor data / use a mechanism like hypothes.is 
                - [[chris aldrich]] https://twitter.com/search?q=filter%3Afollows%20-filter%3Areplies&src=typed_query&f=live
                    - AI(flancian): add it to the Agora as one of the search "providers" :)
                    - [[mellow twitter]] https://twitter.com/search?f=tweets&q=filter%3Afollows%20-filter%3Aretweets%20-filter%3Areplies%20-filter%3Alinks&src=typd
- next actions for [[betaworks]] conference
    - -> [[fotl mattermost chat]]
    - [[mathew lowry]] which visual language do you envision here?
    - [[jerry michalski]]
        - in this private language:
            - [[caret]] ~ [[>]] means incorporate into brain
            - cloud means private
        - but there's many views that make sense for different context, different people
        - the all singing, all dancing platform lets you choose your own view based on what you need and shift between them
        - how to solve this?
            - [[flancian]] assume it will work and then make it work :)
                - gather resources of many different types/mental models, all about the same entity/event/thing
                - then try to make them coalesce and translate between each other
            - [[chris aldrich]] solving the general problem is hard, start with subproblems
                - (someone who solved a related problem)
            - [[jerry michalski]] [[unix model]]
                - composability
                - separate data from (apps?)
    - [[john borthwick]]
        - [[commons culture]] / [[startup culture]]
        - [[civilizational commons]]
        - [[chris aldrich]] it would help to offer a wiki and tools for thought introduction/historical context
            - -> [[rel8 tiles]] ~ https://wiki.rel8.dev/tiles
            - (built on [[massive wiki]] which is git based) -> https://github.com/OpenGlobalMind/rel8-wiki
    - "in a breakfast of ham and eggs, the chicken is [[involved]], the pig is [[committed]]."
        - building lightweight [[bridges]] between tools.
    

## 2022-07-28

### Attending

[[Jerry Michalski]]
[[Chris Aldrich]]
[[Aram Zucker-Scharff]]
[[David Weinberger]]
[[Mathew Lowry]]

### Video
https://youtu.be/aLZ9a70lw2g


### Notes
Jerry's brainf for this meeting: https://bra.in/7j3ewE

- [[Anagora]] shared notes 
- #push [[Commonplace books]]
    - Passed down
    - Example: [[Erasmus Darwin]]'s was left to his family. [[Charles Darwin]] used it and passed it down; it's now in a library
    - Easier to do now on the web while active, harder to preserve 
        - https://indieweb.org/longevity
- [[Aram Zucker-Scharff]]
    - Context.center 
        - [Timelines at work](https://fightwithtools.dev/projects/context-timelines/) - I find timelines to be really useful on understanding and progressing things and finding pattersn and understanding causes.
    - Logging git work and developing in public to make reference easier. 
        - [[Paul Frazee]] - works on [[Beaker]] and other [[Hyper]] projects. 
            - Really cool logging of code work linked with live streaming -  https://paulfrazee.medium.com/building-in-the-open-70ac9dccf1aa 
        - fightwithtools.dev - stream of thought developer notes linked to git commits (still in progress). Trying to make my work more approachable. 
- [[Mathew Lowry]]: What about [[Spaced Repetition]]
    - [[mnemonic medium]]
    - [[Jerry Michalski]]: https://app.thebrain.com/brains/3d80058c-14d8-5361-0b61-a061f89baf87/thoughts/6900f8c3-d117-94dc-4996-39241bd989e0/ 
    - Chris Aldrich: [Piotr Woźniak](https://en.wikipedia.org/wiki/Piotr_Wo%C5%BAniak_(researcher))
    - [[mnemonic reading]]
    - [[Anki]] https://apps.ankiweb.net/ 
    - Duolingo
    - A useful version of this is active notetaking while reading articles - perhaps combined
        - Refrence to Genius and other web highlighting/note-taking layers that exist 
    - [[Soren Bjornstad]] formerly of Anki and now at Remnote has lots of work on spaced repetition https://www.sorenbjornstad.com/writing/ 
    - [[David Weinberger]] [[automated summarization]] could play a role here? 
    - [[Mathew Lowry]]: Something I want to add to MyHub
        - Imagine you are creating another piece of content in the same zone - remember you asked this question to yourself 5 months ago?
    - [[Aram Zucker-Scharff]]: Recently worked on a timeline learning tool - where you get a package of articles in a timeline and it tracks your reading of each article. I wonder if it works with the automated summization content to create learning cards?
    - [[Mathew Lowery]]: It might be interesting to see about giving people different orders of articles than just date saved, that they store so they can build narratives out of those cards. 
    - [[Aram Zucker-Scharff]]: You can pull date from metadata btw. Also: Narrative creation by ordering cards is really interesting. One example of this is Will Wright's tool for Current TV - https://hacktext.com/2011/02/crowd-sourced-television-goes-to-the-next-level-with-bar-karma-and-storymaker-477/
    - [[Jerry Michalski]]: Founder of https://redforester.com/ is working on something similar that takes elements and can organize them in different ways. I recommended animation to different forks. 
    - [[Chris Aldrich]]: Taking notes then reviewing them - asking yourself a question that forces you to produce an answer is a far better method of review that simply re-reading material. Example: [[Cornell Notes]] https://en.wikipedia.org/wiki/Cornell_Notes 
    - [[Jerry Michalski]]: Five Rs of Note Taking: 
        - Recite
        - Record
        - Reduce
        - Reflect
        - Review 
    - [[Mathew Lowery]]: Do you have a set of pre-generated questions that you can slot specific things into or is it more freeform? (To Chris)
    - [[Chris Aldrich]]: [[Cloze]] process where, when you are writing it/taking up the notes you use brackets that mean you are already writing the card. 
        - Have to make sure the questions are not too open ended. 
        - Usually one or two sentences with only a few things missing. 
        - I use it very sparingly because I have other methods I prefer to [[Spaced Repetition]]
        - Actively linking notes also helps a great deal. 
    - book: Memory Craft: Improve Your Memory with the Most Powerful Methods in History (2019) by [[Lynne Kelly]]
- [[Jerry Michalski]] AR projects seem to lack informational, helper, curational stuff. 
- Useful concept memory palaces: loci
    - https://en.wikipedia.org/wiki/Method_of_loci
- [[David Weinberger]] 
    - background in philosophy 
    - for past 30 years writing about the ways in which technology effects the ways we think about things. Focused on Machine Learning for the past 5 years. 
    - Working at Google on Ethics and AI
- [[David Weinberger]] - Writing Notes Process
    - Hobbyist programmer
    - Wrote app that lets me take notes in plain old [[ascii]] (text)
    - bibliographic info at top
        - page number, note and tag
    - took notes on a ton of info that way
    - then built an app that let me shunt it all into databases 
    - Went back to Zotero yesterday
        - Couldn't get it to work and it doesn't work the way I want it to. 
    - [yes](https:yes.com) 
- [[Aram Zucker-Scharff]] 
    - I liked [[Endnote]] when someone else was paying for it. 
    - [[Zotero]] is great, not for me really because I'm no longer an academic, but lots of great ways to plug in to it to make it for me.
    - For arguing on the web, that's what I use context.center for. 
- [[Chris Aldrich]]: 
    - Mendeley seems to be shutting down
    - Zotero is useful for annotating PDFs and now does export of notes from .pdfs as of version 6.0
- [[Jerry Michalski]] big charts and zooming in and out of them is one of the problems we need to take on. 
- [[Mathew Lowry]] 
    - [[Harvard Growth Lab]] has an amazing infographic about economics
        - https://growthlab.cid.harvard.edu/
- Reminds me of - https://github.com/Quartz/Chartbuilder
- [[Cesar Hidalgo]] - https://centerforcollectivelearning.org/
- What do we take on next? Agenda for next week:
    - How to explain the shared memory concept? 
    - A lot of different answers. 
    - Maybe understanding what the technical format is for a "memory" so it can be shared effectively. 
- Where are the YouTube listings of our calls?
    - In Jerry's brain 
    - In the Mattermost chat 

## 2022-07-21

### Attending: 

[[Jerry Michalski]]
[[Chris Aldrich]]
[[Aram Zucker-Scharff]]
[[flancian]] (who says: thank you so much for taking notes last time!!!)
[[Mathew Lowry]]

### Video
July 21, in 2 parts:
- https://youtu.be/P6Ge5-DAXF0  and 
- https://youtu.be/oaWi86wUHLE

### Notes

Jerry's Notes on this session: https://bra.in/8vm4JJ

- The book Mathew is working on: https://personalknowledgegraphs.com/#/page/Personal%20Knowledge%20Graphs
    - working with [[wireframes]]
- [[Chris Aldrich]]
    - [[punch cards]]
    - [[beatrice webb]] https://en.wikipedia.org/wiki/Beatrice_Webb
    - [[niklas luhmann]] was born the year after she published
    - [[conrad gessner]]
        - [[flancian]] likely the namesake for [[gessnerallee]], and I didn't know him!
    - [[ramon llull]] 
        - the [[catalan]]
    - [[herman hollerith]]
    - [[roland barthes]] (look into previous week's notes)
    - [[aristotle]]
        - influenced the [[great chain of being]]
    - [[sky woman]] vs [[adam and eve]]
    - [[doughnut economics]]
        - [[flancian]] [[ontoshift]] in [[free, fair and alive]]
        - [[aram zucker-scharff]] reported on economics back in the day
            - "[[economics]] is more [[sociology]] than it is [[mathematics]]"
            - [[Chris Aldrich]] there's interesting work in [[complexity economics]] that goes beyond [[clockwork models]]
                - [[santa fe institute]]
                    - [[cognitive artifacts]]
- [[Jerry Michalski]] is an [[economics undergrad]]
    - taking [[pattern languages]] and [[extending]] them and [[integrating]] them 
    - [[open source pattern language]] of [[re(generative) commons]]
    - how to share notes with each other, into myhub, agora and other platforms?
- https://anagora.org/node/ontoshift
- Formats and protocols to exchange and connect knowledge 
    - [[flancian]] thinks of Anagora as a reference implementation of [[agora protocol]], which is this protocol
    - What are the standard objects that move back and forth on this protocol? What is the shapes and how can they enable information exchange and connection? 
        - Does this connect with ActivityPub? Could we send objects and federate "brains" in this way?
    - A schema for everything(?) https://schema.org/
- [[Jerry Michalski]]
    - #push [[rel8]]
        - https://wiki.rel8.dev/rel8_pioneers
- [[Mathew Lowry]]
    - [[Chris Aldrich]] asked for examples of model [[zettelkasten]] outputs
        - hasn't gotten many :)
        - #push [[zettelkasten]]
            - [[model examples of zettelkasten output processes]] https://boffosocko.com/2022/07/12/call-for-model-examples-of-zettelkasten-output-processes/
            - conceptualization: we can all take small notes, interlink them ([[Jerry Michalski]] calls them [[nuggets]])
                - [[Jerry Michalski]] [[nuggets, narratives and points of view]] https://www.youtube.com/watch?v=EmId2x6JSQE&feature=related
            - how can I pull up 2, 3 nodes that bring up a certain number of text blocks that can then be assembled into long form text or some other format that is fit for consumption by others?
                - linear version is one output format, likely the most useful one
                - interactive experience as an alternative?
                - closest UI that exists might be [[devonthink]]
                - [[Mathew Lowry]] akin to what script writers assemble
                    - [[aram]] that is called [[murder board]] / [[scrub down]]
                    - [[Chris Aldrich]] [[anacapa]] charts / [[anacapa charts]]
   - #push [[zettelkasten]]
       - [[Jerry Michalski]] question about [[zettelkasten]]
           - why would the numbering system be useful nowadays?
               - unclear
           - is the fandom in a [[blind alley]] because of the focus on form?
           - [[Chris Aldrich]] [[zettelkasten origin myth]]
       - [[aram zucker-scharff]] confusion of technique with presentation layer
           - [[trello]] is inspired by [[getting things done]]
       - [[Chris Aldrich]] the ability to reuse what you've already written is key to every productive academic; the means of doing this is critical to productivity
           - [[luhmann]] kept changing, improving his technique
- going back to the [[flatten]] problem (going from n notes to a long form text)
    - [[flancian]] two possible approaches
        - define a [[dsl]] for flattening/assembling (transclusion helps; pull, push in the Agora goes in this direction)
        - train and use large language models with notes being part of prompts
    - [[dimensionality problem]]
        - [[planarity]] as first target when processing a high dimensional graph
        - then [[linearity]] closer to text?
    - [[Jerry Michalski]] the [[zoom problem]]: information does not make sense at all distances
        - [[the brain]] always seems to work for [[jerry]] in this sense
        - adding [[clusters]] to link existing nodes is critical for keeping it manageable
        - [[yellow]] means cluster
            - [[types]]
        - [[purple]] means opinion
            - [[enumerated wisdom]]
            - [[cialdini's six principles]]


### Action items / #TODO

- [ ] invite others
    - who?
    - if we write it down in a canonical place we can distribute this (useful, social) work
- [ ] set up cross-review?
    - [[flancian]] would be willing and glad to review other people's writing, perhaps we could do this as a group?
        - full disclosure: I'm also writing a chapter :)
        - Always glad to read and make suggestions! - [[Aram Zucker-Scharff]]
- What else might we publish? Potentially on the site
- [ ] [[let's share notes]]
    - [ ] start integrating pattern languages
        - [ ] build a [[meta pattern language]]


### Chat log
Jerry Michalski says:
https://flowimmersive.com/tricast
Fellow Jitster says: (note for later: Obs 27 has issues) 
Jerry Michalski says:
https://doc.anagora.org/fellowship-of-the-link
 
Jerry Michalski says:the book in progress: 
https://personalknowledgegraphs.com/#/page/Personal%20Knowledge%20Graphs
mathew says:Shipping containers for thoughts 
https://anagora.org/ramon-llull
Jerry Michalski says:
https://en.wikipedia.org/wiki/Conrad_Gessner
Chris Aldrich says:You want this reference Mathew: Lima, Manuel. The Book of Trees: Visualizing Branches of Knowledge, 2014. 
https://papress.com/products/the-book-of-trees-visualizing-branches-of-knowledge
mathew says:👍 
Chris Aldrich says:Some additional names for your history of knowledge list: Aristotle, Porphyry, Isidore of Seville, Lambert of Saint-Omer, R. Llull, Joachim of Fiore, F. Bacon, C. Linnaeus, R. Descartes, E. Haeckel, Thomas Harrison, Leibnitz, Beatrice Webb 
Jerry Michalski says: https://wiki.rel8.dev/rel8_pioneers


## 2022-07-14

### Attending: 

[[Jerry Michalski]]
[[Chris Aldrich]]
[[Aram Zucker-Scharff]]
[[Marshall Kirkpatrick]]
[[Timur Ismaligov]]

### Video
https://youtu.be/OlIxzH23ee0


### Notes
Jerry's Brain for this session: https://bra.in/5p7LJJ

Flancian had family conflict and couldn't attend

[[Marshall Kirkpatrick]] 
	- First attendance here, though only for a portion of the call
	- working on a climate justice news aggregator

General discussions about archives and miscellaneous topics

Jerry and Chris stayed late to talk about note taking related topics.

[Flow Immersive Tricast](https://flowimmersive.com/tricast) is the app that Jerry uses to put his face into a small highlight while he shares his screen 

### Chat log
Jerry Michalski: our real chat is over here: [https://chat.collectivesensecommons.org/agora/channels/ogm-fellowship-of-the-link](https://chat.collectivesensecommons.org/agora/channels/ogm-fellowship-of-the-link)

11:13 Aram Zucker-Scharff: Here's the link to that - [W3C group on sustainability](https://www.w3.org/community/sustainability/)

11:20 Jerry Michalski:[https://www.linkedin.com/in/ryankspangler/](https://www.linkedin.com/in/ryankspangler/) ?

11:31 Aram Zucker-Scharff:[Trophy](https://rrchnm.org/portfolio-item/tropy/)

11:53 Marshall: Gotta run! Thanks all!


## 2022-07-07
### Attending: 
[[Jerry Michalski]] [[Chris Aldrich]] [[flancian]] [[aram zucker-scharff]] [[Mathew Lowry]] [[bouncepaw]]

### Video
In 2 pieces. here's segment one https://youtu.be/41bA7oHG__c and two https://youtu.be/n1hS6sADgaw  
with my Brain notes here: https://bra.in/8px4ZK

### Notes
- Where to track a recurring agenda/our goals?
    - [[Jerry Michalski]] https://wiki.rel8.dev
    - [[Chris Aldrich]] something that has worked for indieweb is having people who join show a token of interest; e.g. try to improve something for someone
        - i.e. we can talk all day, but improvements to real systems are what we should be shooting towards
        - we could focus here on integrating systems that already exist (the ones we're building or fostering individually) as a group
    - [[flancian]] let's try to spot patterns (...)
- [[aram zucker-scharff]]
    - works for the [[The Washington Post]]
    - developed [[pressforward]], a tool for [[wordpress]]- http://pressforward.org/
    - building easy to use websites, archives -- in a way that allows them to interact with each other
        - https://context.center/
        - https://github.com/AramZS/contexter
        - https://fightwithtools.dev/projects/context-pages/
    - [Aram on the Fediverse](https://indieweb.social/@Chronotope) 
    - interested in solving [[misinformation]] and [[archival]]
    - for note taking, [[markdown]] on [[git]]
        - [[flancian]] https://anagora.org
- [[fellowship of the link]], a crowdsourced introduction :)
    - [[zettelkasten]], [[commonplace books]], [[tools for thought]], [[personal knowledge graphs]], [[interlays]]
    - [[Chris Aldrich]] lots of projects in this space are trying to sell something; but we care most about the [[commons]]
    - how do we take idea capturing and generating and link them into a healthy [[knowledge commons]]?
- [[logseq]] model as it relates to the commons
    - taking VC money seems slightly worrying as they'll want to be repayed
    - https://boffosocko.com/2022/07/05/economic-models-in-social-media-and-a-better-way-forward/
    - [[logseq]] looks close to [[obsidian]]
        - do we have enough variety of approaches?
    - paying for services is fine
- [[you need a wiki]]
- [[agenda]]
    - #push [[rel8]]
        - https://wiki.rel8.dev
        - [[Jerry Michalski]] [[rel8 pioneers]]
    - [[flancian]] let's all push our projects onto a shared space and talk by default about interlinking and integrating them?
    - [[Chris Aldrich]] let's start a list of resources and repositories? 
        - this may help to bootstrap a [[commons]]
        - [[Jerry Michalski]] [[mycelium]]
- [[Jerry Michalski]]
    - [[liberating voices pattern language]]
        - [[1 2 4 all]] ~ [[one two four all]]
- [[bouncepaw]]
    - [[mycorrhiza]]
    - [[hypha]]
- [[flancian]] let's build an [[agora]]? :)
    - this seems to be what we're trying to achieve this, regardless of the name?
- let's bring to the next meeting -- a list of:
    - [[repositories]]
    - [[tools]]
    - [[projects]]
    - (that we want to integrate/cross reference/discuss)
- [[affordances]]
    - [[wikilinks]] and [[metadata]] as key to the [[commons]]
- [[meta]] about chat
    - let's prefer the [[mattermost]] to [[jitsi chat]]
- [[Jerry Michalski]] what's the difference between [[indieweb]] vs [[fediverse]]
    - [[Chris Aldrich]] [[fediverse]] is a subset of [[indieweb]]
    - [[Chris Aldrich]] [[indieweb]] is based around the notion of having your own website and building your identity around it
    - [[Chris Aldrich]] [[fediverse]] is based around the notion of your identity being hosted in an instance like [[mastodon.social]]
 
 - Let's discuss what we wrote to [[rel8]], our lists of:
    - [[repositories]]
    - [[tools]]
    - [[projects]]
    - (that we want to integrate/cross reference/discuss)
- People who need access to the repo (github usernames):
    - flancian
    - aramzs
    - bouncepaw
    - chrisaldrich
    - mathewlowry
- Let's talk about [[search engines]]
    - https://warmedal.se/~bjorn/posts/2022-07-02-providing-meaningful-search-results-without-own-index.html 
    - [[queries as addresses]]
- Phone service vs Internet service analogy: https://boffosocko.com/2022/07/05/economic-models-in-social-media-and-a-better-way-forward/
- Let's onboard everybody to the [[fediverse]]!
    - [[mastodon]] app is actually good to bootstrap/choose an instance
- Dump your ActivityPub IDs here ;)
    - @flancian@social.coop
    - @chrisaldrich@boffosocko.com
    - @bouncepaw@lor.sh 
- What do we see as our long term goal?
    - [[flancian]] let's integrate repositories and tools and write [[science fiction]] together :) how could our tools, platforms, the internet, the world at large look like by [[2025]], [[2030]]?
    - [[Mathew Lowry]] is focusing on producing the [[pkg book]] chapter and would love to do research and writing in this space
    - [[Jerry Michalski]] would like to participate in exploration and prototyping; illustrate and broadcast interesting ideas for others to pick up; analyze what it will take to deliver this by the next decade; organize activities
    - [[Chris Aldrich]] appreciate the idea of [[shared wikis]] that can communicate back and forth with each other
        - [[flancian]] we should invite [[ward cunningham]]!
        - [[Chris Aldrich]] history of the medium
        - [[Jerry Michalski]] [[songlines: the power and promise]] 
            - [[Chris Aldrich]] [[third archive]]

## 2022-06-30
### Attending: [[Jerry Michalski]] [[Chris Aldrich]] [[diego de la hera]] [[flancian]]

### Video
https://www.youtube.com/watch?v=x8pkNRRncTc

### Notes
- [[Jerry Michalski]] 
    - #push [[rel8]] 
        - #go https://www.rel8.dev
            - (a [[google site]])
            - https://www.rel8.dev/wiki is embedded above
        - "relating ideas, documents, perspectives and people"
    - (Jerry is using [[obsidian]] plus [[obsidian sync]] for this)
    - [[short term]], [[medium term]] and [[long term]] goals for [[rel8]]
    - [[short term]]
        - define: how do we share notes?
        - import [[jerry's brain]] from [[json]] into [[obsidian]] and [[excalidraw]]
            - [[Zsolt Viczián]] (https://www.zsolt.blog/) is interested in doing this
        - what do we put on [[rel8]]?
            - a list of formats/processes that are sufficient for us to 'store our brain' comfortably?
            - [[Mathew Lowry]] user requirements exercise
        - [[flancian]] on a hub architecture for integrating brains and negotiating exchange (format conversion)
            - [[underlay]], [[interlay]], [[overlay]] as per [[metasj]]
        - [[Mathew Lowry]] decentralized or centralized?
            - decentralized is the idea (or distributed)
        - [[Mathew Lowry]] what should we be using as way of standards to create this?
        - [[Chris Aldrich]] text -> markdown -> html
            - (shared by default is convenient but can be problematic)
            - text as the basic standard
            - then add links, e.g. markdown or org mode
            - then html, microformats, json, yaml can be layered on top
            - exchanged p2p (distributed) or via hubs
        - [[Mathew Lowry]] interested on web mentions, fediverse as they exist in the data exchange ecosystem
        - [[Chris Aldrich]] how can you design a minimum building block that is interoperable with other pieces?
            - [[web mentions]] takes the older ideas of pingback/trackback, strips them down to the essentials. it's a notification system via [[post]] requests.
            - [[mastodon]] could support web mentions (there was talk about this a few years back)
            - if X writes a post about URL A by Y, Y will be pinged
            - Y receives the notification, can do some spot checks (does the call refer to a post that actually has the expected link), and then does whatever it wants with it
            - [[activitypub]] could take advantage of [[webmentions]] as a building block, but it mostly doesn't
                - [[kevin marks]] (sp?) added microformats to [[mastodon]]
       - [[flancian]] decentralized vs distributed approach, web3 and all
       - [[Jerry Michalski]] technical details vs ease of use
       - [[flancian]] two directions we could go in:
           - text as the standard makes it easy to use actually as users can write text wherever they want, a priori
           - focusing on making existing tools and ecosystems easier to use/onboard to
       - [[Chris Aldrich]]
           - high tech skills: you set up your own mastodon instance, agora, etc.
           - medium: you produce information, content but someone else pays the [[admin tax]] (you contribute to an instance)
           - (spectrum)
           - no technical expertise
           - #push [[blot im]] is very useful, imports from whenever you want
               - [[flancian]] nice, and it's open source: https://github.com/davidmerfield/blot
               - wanted to do this for the Agora so this is super helpful
       - [[Mathew Lowry]]
           - who are we building this for?
           - "instagram user" might be too wide a net?
           - disconnect from building a knowledge graph and writing for others
       - [[Jerry Michalski]]
       - #push [[nuggets, remedies and pov]]
           - [[nuggetization]] https://www.youtube.com/watch?v=EmId2x6JSQE&feature=related
       - [[public]] vs [[private]] as a default
           - [[public]] as default seems better to seemingly most of us
       - [[Chris Aldrich]] mostly these days notes start in [[hypothes.is]]
           - periodically gets feedback about how cool it is to work in public
       - [[Jerry Michalski]] [[fedwiki]]
           - [[twitter]] user 509 here (!)
       - [[diego de la hera]]
           - going back to what we have in mind and where our ideas overlap
           - not really sure what he's expecting here, but a tool that would be interesting would be like this:
               - like the agora, where you could see it from two different perspectives
                   - as a personal tool, where an individual user decides which graphs converge on the agora
                   - "mix and match" feeds and gardens, an aggregator
                   - like an [[agora view]]
               - another agora is closer to anagora.org, where you push many graphs to a place but where the owners of the repos decided that in advance
           - an extension or tool could be written so that the nodes you see could be actual URLs, and incoming/outgoing links would be those around your internet context (social graph, feeds)
           - [[Jerry Michalski]]
               - [[apple's]] [[knowledge navigator]] video back in 1986
       - [[adversarial interoperability]]
           - [[Chris Aldrich]] For the [[adversarial interoperability]] fans: https://granary.io/
           - [[Mathew Lowry]] [[mysilio]]
       - [[myhub]]
           - writing aids to get from notes to defined outputs
       - [[having a somewhere]]
           - [[knowledge contexts]] as a service
       - [[Chris Aldrich]]
           - [[writing toolkit]]
           - #push [[social reader]] tracks, breaks down and integrates feeds
               - #go https://indieweb.org/social_reader
           - https://indieweb.org/Microsub
           - [[micro.blog]] is great
           - [[refbacks]]
               - https://notes.andymatuschak.org/z2QvtE9w5zs49x7WUeG8Ut1vywHDLiG2Wkm9p pinged his site
       - [[Jerry Michalski]]
           - [[intimacy gradient]] is a pattern in [[a pattern language]]
           - [[the view master]]
               - how do we generalize and integrate the superpowers that each tool gives?
       - [[diego de la hera]]
           - would like to highlight the link aspect of how information pieces relate to each other
           - which links are mentioned in that tweet, that post?
           - about the [[great fungus]]
               - still thinking of this as an individual app customized by the user
               - [[personalized fungus]]? [[fungus view]]
- [[minimum viable formats]]
    - text
    - diagrams
- [[goals]]
    - define our [[wheres]] (from [[having a somewhere]])
        - [[the big fungus]]
        - [[agora]]
    - define minimum viable formats for storing our brains

## 2022-06-24
### Attending: [[Jerry Michalski]] [[Chris Aldrich]] [[flancian]]
### Video
https://www.youtube.com/watch?v=K9aRBtTqLjw

### Notes
- Discussion of [[go links]]
    - Demo in anagora.org :)
    - [[go/fotl/chat]] and [[go/fellowship of the link/chat]] both now work
- Time?
    - 11am Pacific on Fridays?
        - Could conflict with date nights in Europe :)
    - [[11am Pacific on Thursdays]]?
        - Let's try this!
- [[shared resources]]
    - [[Chris Aldrich]] putting up something in the site
        - add a go link :)
    - here's what we're doing, here's where we're going, here is how to join
    - let's use [[chat]] for coordinating
- what's a high leverage topic for the three of us?
    - [[Chris Aldrich]] what's pareto optimal/the 20% we could tackle first?
    - [[Jerry Michalski]] has been working on a [[shared vision]]
    - [[flancian]] [[2025]]
- [[Jerry Michalski]]
    - how to build a "webring" for meetings, documents about projects
    - [[obsidian]] with [[excalidraw]] done by a friend
        - diagrams.net is also good
    - [[open global mind]] ~ [[ogm]]
        - [[flotilla]] -> [[federation]]
        - what do you see from the top of your mast?
        - [[multi plane camera]]
        - [[map of the future]] ~ [[mosaic]]
    - [[flancian]] [[agora]] plus iframes for mvp of the above
    - [[Chris Aldrich]] standard based, using each item as a block
        - [[oembed]]?
        - tools tends to target one tool only, lots of duplication
        - [[activitypub]]
            - [[Chris Aldrich]] over designed it, over specified it, few people understand it completely
                - [[aaron parecki]]
            - [[mastodon]] as the de facto standard rather than ActivityPub itself
                - we can bridge to mastodon or pleroma, do not need to reimplement it
            - what about [[rss]]?
                - [[Jerry Michalski]] does this not break transclusion?
                - How can we prevent the unproductive RSS/Atom wars of the early blogosphere? 
        - [[Jerry Michalski]] [[least common denominator]]
            - problem or potential?
            - [[tbl]] simplified [[sgml]] and made it break gracefully
            - [[resiliency]]
        - [[cory doctorow]] on the [[tragedy of the commons]]
            - [[modus operandi]] and [[throughput]] amazing
            - [[Chris Aldrich]]: cory has a [[commonplace book]] essentially, see https://pluralistic.net/2021/01/13/two-decades/
            - [[flancian]]
                - [[adversarial interoperability]] https://www.eff.org/deeplinks/2019/10/adversarial-interoperability
                - [[catalog of missing devices]]
- from chat unprocesssed
    - Jerry Michalski dice:transclusion 
    - Chris Aldrich dice:How to create a Read Fork Write Merge Web? 

(Older notes are now in [[fotl]].)