# Mathew's notes on Revive conference: Gordon Brander demos Subconscious
## Context 
* see [RENDER: Tools For Thinking conference](https://myhub.ai/items/render-tools-for-thinking-conference)
* I'm using different note-taking tools to scribe  different conference sessions - this Hedgedoc was automatically created by [[flancian]]'s [[an agora]] [page for the conference](https://anagora.org/tools+for+thinking)
* The idea we have in the [[Fellowship of the Link]] is that all the notes by all the scribes are somehow interlinked in a shared second brain, hence the wikilinks in these notes
* I've been enjoying [[Gordon Brander]]'s enewsletter for a while, so I'm really looking forward to his demo. I'm way behind properly processing his content, tho - everything I LikeThinkDo tagged [[Gordon Brander]]: https://myhub.ai/@mathewlowry/?tags=gordon+brander
* I'm looking to riff off this in search of insights meaningful to me as I explore this space, write a chapter in [[Ivo Velithckov]]'s book on Personal Knowledge Graphs, and develop my ideas for [myhub.ai](myhub.ai)
## Noosphere: worldwide PKG

### What would it take to make the internet a useful thinking tool?
Sensemaking crisis during planetwide crisis.
We didnt get a global brain from the internet because "apps trap thoughts" - caused by fundamental internet architectural idea: "same origin security model": each app its own Universe.
Needed: protocol for thoughts.
### what is Noosphere: 
* Open source project, cofunded by mozilla and ipfs.
* Ambition: create low-level p2p infrastructure, like http
* decentralised over [[ifps]]
* priotises user ownership, yet multiplayer
* belongs to everyone: you can do whatever you want

### what does it do
* local first file sync
* change hilstory a la git
* cross-app transclusions & backlinks
* user-owned data backpack - take your data with you
* self-soverign social graph - you own what you put into it
* lots of copies to keep stuff safe (content addressing)

**Layering onto [[ipfs]]:**
* human friendly names for ipfs hashtags:
* versioning
* signing with UCAN-authorized key

**@sphere/path:**
* @sphere is your username, derefernces into a public key
* paths point to memos:
    * generic protocol
    * ipfs meta envelope: header + body (pointer to a ipfs file) + parent (pointer to previous version, hence version control)
    * any filetype
    * [[UCAN]] signed: cryptographic protocol
        * authorises data management
        * self-sovereign security model: you own your keys, your identity, take it with you
            * works with wallets and passkey paradigm

**Sphere servers**
* personal ipfs gateway
* bridges to web
* synch with personal devides

## Myhub and Noosphere?
Hugely interesting. Possibly too ambitious for me.
Out of the box he's including following, so content published by people you follow comes to you. But instead of the link to content published at a URL, it's the content itself which comes to you as content is "gossipped around the web".



# Group Notes
Orginaally from https://etherpad.indieweb.org/ToolsForThinking

Please note that all contributions to this pad and other IndieWebCamp documents are considered to be released under the public domain according to CC0.

------------
RENDER();Tools For Thinking
How New Technologies are Changing How We Create, Share, and Build Knowledge
Session: #ToolsForThinking 
https://betaworkss-fabulous-project.webflow.io/event/render-tools-for-thinking
[[2022-08-16]]
video: https://player.vimeo.com/video/739652984?h=ecdefd58ba

## Speakers
* Neel Baronia (Introduction)
* John Borthwick
* Jerry Michalski
* [[Daniel Doyon]] & [[Tristan Homsi]] ([[Readwise]])
* Gordon Brander

## Participants
* [[Chris Aldrich]]
* Natasha Mott
* {{capjamesg}}
* {{kevinmarks}}
* {{campegg}}

## Notes
[[Kevin Marks]] live notes: https://www.kevinmarks.com/toolsforthinking.html
- via noterlive.com
- Twitter Thread starts here: https://twitter.com/kevinmarks/status/1559567010287206400

Noted times are being changed to actual as the day progresses.


### How Do We Define Tools for Thinking and Why Do They Matter?
* 12:10 PM – 12:20 PM
> Join [[Jerry Michalski]] and [[John Borthwick]] as they talk about their interest in tools for thinking, and what excites them the most about the future of the category.

- Jerry demos [[The Brain]] he's been using since December 1997 (25 years this year)
** Hit the half million mark this year for ideas


### Inflection Points for Tools for Thinking 
* 12:23 PM – 1:04 PM
> What are the key inflection points that will supercharge Tools for Thinking in the near future? How will new technologies, user metaphors, and funding models change how people build these tools? John Borthwick will be discussing how the landscape is changing with the co-founders of [[Readwise]], [[Daniel Doyon]] & [[Tristan Homsi]].

- Readwise is a tool to help you read better and remember what you've read. 

- @deadly_onion : we then got asked to bring the notes inot other tools, so we're like the Zapier of annotation

- 12:30 AM Funding models for these tools for thought  
- User-based subscription models vs. venture capital  
- Borthwick: SaaS services tend to silo information and data


#### Q+A
* 12:30 PM – 1:03 PM
Q: Is there an inverse of [[spaced repetition]] for Readwise: Example: Could one use Anki for writing?
A: People putting their writing into their Readwise review where they improve each "highlight"/paragraph and work on it in a spaced repetition manner. After refining they then put a full essay together from their building blocks.

Q: How do you not get stuck on the system, but manage to create rather than optimizing the process?

CJA: Spaced repetition on hightlights is useful, but it's only a small part of a successful practice.

"The pattern we see is people optimizing the tool and optimizing the process (rather than writing)" — @homsiT
NM: ^^this seems apparent given how many novel notetaking apps I'm learning about right now.  I've spent 15 minutes trying to figure out where to put my thoughts instead of actually putting them somewhere.

Q: Borthwick: Rise of audio: How does one move audio into the tools for thought space?
A: Airr and Snipt both do audio to text in this space as early attempts. AI transcripts can be annoying and a little off, but speech to text is improving. Audiobooks space is a closed format that's dominated by one player (Amazon).  

Borthwick: It's silos all the way up and down.  

Q: How has Readwise changed in respect to TfT changes over the past few years?
A: Daniel: Pulled into TfT because of note taking apps. People wanted to do everything in their note taking apps. This is starting to cool down and people are taking a "portfolio" approach to their apps and functionalities.  

Consumer SaaS is hard and has a high support need. Corporate SaaS is an easier model for many reasons.  

Q: Are people reading slower because they're taking more time to ingest?  
A: Immersion reading (visual reading and audio at the same time). 
Daniel: "It's kind for like a sensory deprivation tank for reading."
Tristan: Venkatesh (Rao?) has defined "Walden-ponding" - throw away technology and reclaim your attention
Tristan: There is no spec out there that's flexible enough for web, devices, podcasts/audio. Readwise would love for that to exist.

Q: Borthwick: There's a need for portable "knowledge blobs"...
Daniel: Readwise looked at turning everything into blocks and do a block-based architecture
John Borichevsky - documents inside of Roam was tough
They developed a phase change metaphor for guiding their design. How to turn knowledge blobs into coherent texts for sharing. Blocks vs. Docs. Take solids (documents) and turn them into fluid blocks (blobs of knowledge). Using a solid/liquid/gas framing here.

Roam Research users spurred them into using Jinja formatting to allow for customization

Readwise for discord is coming in beta...

Q: Thoughts on moving Readwise into the educational sphere?
A: They've never had success in the eduction envrionment. Their users are more auto-didacts. They'd love to do more of it.


### Demo: Protocol Design for Tools for Thinking 
* 1:04 PM – 1:20 PM (5 minutes over)
> [[Gordon Brander]] will be presenting a brief demo on [[Subconscious]] and the [[Noosphere]], products he and his team are working on to allow Tools for Thinking to become interoperable and better connected.

Subconscious - Social note taking tool
The internet is already a tool for thought. It hasn't yet produced affordances for coping better. [[information overload]]
We're facing a sense-making crisis. As a planet, we need to learn to think together.

CJA: This sort of dream also failed in the renaissance in a writing (offline only) setting. What can be learned from this prior art/effort? See [[Konrad Gessner]], et al.

Brandon: Maybe we need a protocol for thought?

CJA: maybe less protocol, but some loose standards. small pieces loosely joined, more web-by

CJA: Lots of references to Xanadu today, but nothing prior to that, sadly.

[[Noosphere]]: a worldwide knowledge graph. decentralized over IPFS, prioritizes user ownership, multiplayer, versioning, signing, self-sovreign social graph

[[Fission]] has been working on a protocol for the security part for a while [[Jess Martin]] et al.
1:17 PM [[UCAN]] model
follower/following model built in
They've got a Discord channel for Subconscious and Noosphere: https://discord.com/invite/wyHPzGraBh


### Lunch and Networking 
* 1:20 PM – 2:00 PM



### The History and Future of Software as Tools for Thinking 
* 2:00 PM – 3:00 PM
> Some of the earliest examples of software explored by pioneers like Doug Engelbart, JCR Licklider, Alan Turing, and others were at their core technologies that help magnify, inspect, and spread our ideas. Jerry Michalski will be sitting down (virtually) with [[Howard Rheingold]], author of Tools for Thought, to explore the history and future of "mind-amplifying technology".

[[peeragogy]] - neologism created by Howard Rheingold
- definition tk

- Alan Kay "Microelectronics and the personal Computer" article
- 1982/83 Person of the year: the personal computer
- Man from the Future (book) about John von Neumann
- James Fathomon (sp?) psychologist on thinking project
- tools for making tools 

Jerry Michalski: One of this favorite affordances of The Brain is its ability to juxtapose ideas, something he wouldn't get out of a more database-like tool.

Rheingold did use 3x5" index cards for outlining and arranging ideas physically with respect to each other.

Arthur Brock - expressive capacity (see: Jerry's Brain)
Early versions of AutoCad didn't have certain functionalities they did later, so architects and designers couldn't build or create certain sorts of structures. 

Bob Taylor - video on early internet (see Jerry's brain for link)

Stack exchange version for the tools for thought community? Where is this? (HR)
HLAMT part

The more responsibility you give to learners the more engaged they are. [[co-learning]]

5 literacies of social media article by Howard Rheingold (see Jerry's Brain)

Teaching people how to detect [[bullshit]] is a [[wicked problems|wicked problem]]
It's up to the reader to determine [[authority]]. It's a problem that exists as a part of literacy.

CJA: Even major platforms like television and radio now don't serve as automatic authority the way they did two or more decades ago.  The cheaper a medium is to operate in the more one must invest in determining authority and sifting out untruths.

How to create trusted social networks of information?

Mike Caulfield: SIFT acronym for information literacy: https://hapgood.us/2019/06/19/sift-the-four-moves/
    * Stop
    * Investigate the source
    * Find better coverage
    * Trace claims, quotes, and media back to the original context


[[The Well]] as an early bonfire for social knowledge on the internet. https://www.well.com/

(2:39 PM) Deliberative polling

#### Q+A
2:35 PM – 3:00 PM

Q: Why would strangers give knowledge away to others (for free)? (broadly unanswered)
- psychology, social capital, etc. 
CJA: How does this dovetail with respect for unsolicited information? (mansplaining, for example) How can we encourage one while discouraging the other.

Jerry reminiscence: Blair Newman's posts on The Well were deleted a week before he commited suicide. The community rebuilt his data after.

Q: Chip Kennedy: Is there a place for authority figures in the space without going back to "gate-keeping".
A: Authority figure is a loaded term. 

Q: our brains operate on emotion as well as reason - how do we use emotion in these second brains?
A: @hrheingold: understanding some of our emotional biases is very important - the book The Media Equation is worth reading - they did psychological tests, but swapped in a computer or a cartoon instaed of a human, and people treat them as humans
also referred to emotion as a "weakness"

Q: Spaciality and tactility with respect to analog note taking
A: [[Hiroshi Ishi]] - computational capabilities into physical objects (MIT MediaLab), https://www.media.mit.edu/people/ishii/overview/  
HR recommends [[The Extended Mind]] by [[Annie Murphy Paul]]   
(CJA) - I highly recommend this book too! Notes: https://hypothes.is/users/chrisaldrich?q=urn%3Ax-pdf%3A37343666363464373933303538336161623732646237386463616662643365313266653032623035373331303031636338326237316361396637343432643431  
Physical/emotional awareness can help us make better decisions - more experimentation needed in this area
Those with better awareness of their pulse have been shown to make better snap financial trading decisions.

Q: Has a computer interaction ever caused you to experience something like a psychedelic experience?
A: No, but recalled a time when students were taking psychedelics and chatting online...

[[Mind Amplifier]] by Howard Rheingold  
http://rheingold.com/texts/Mind_Amplifier.pdf  

### Tools for Thinking Product Demos 
* 3:00 PM – 4:00 PM
> We’ll hear from builders and thinkers deep in the space and get to take a look at what they’re working on. We’ll be checking out Plexus, Re:Collect, Jerry’s Brain, Subconscious and more. 


#### Plexus
3:00 - 3:14 pm
Davey Morse, founder of [[Plexus]], went to Williams College
Created note taking tool for himself
[@davey_morse](https://twitter.com/davey_morse)

* Friend had health issues with mono-like symptons
** (this sounds like Tiago Forte's story about using note taking to self-diagnose)

https://render.plexus.earth/p/render
@davey_morse: if you type a thought inot the box, it will give you the thought that matches it most closely

https://williamsrecord.com/168916/features/students-create-alternative-note-taking-app/


#### Re:Collect
3:14 - 3:26 PM 
AliceAlbrecht, Founder + CEO, re:collect
academic, in cognitive neuroscience, machine learning
@AliceAlbrecht
AI powered creative assistant
Being able to access your ideas when you need them. 
Breadcrumbs for our future selves. How to find your old material
scrap heaps (though she didn't use the specific word)
no explicit tagging or organizing
past self / future self problems
anxiety relating to your ideas (storing, finding) 
web app and web extension
card-based infinite canvas

#### Jerry’s Brain
3:27 - 3:37
[[Jerry Michalski]], Founder [[Open Global Mind]]
@jerrymichalski
idea sex

#### Subconscious
3:38 - 12:48 PM 
LinusLee, Independent Researcher, @thesephist
Sentence gradients

We can represent colors in numbers and then operate on them in a way we can't yet operate on words or sentences.

@linuslee
: you can't operate on words like you can work on numbers, you need to rewrite rather than quantify

@linuslee: just as we can manipulate colours by converting them to RGB values, what fi we can convert word meanings to a space that we can manipulate?

Demo. 
Looks a bit like Robin Sloan's AI Writing experiments https://www.robinsloan.com/notes/writing-with-the-machine/

@linuslee: we want to encapsulate ideas and be able to do algebra on ideas
^^ this sounds a lot like Leibnitz's idea for Universal Languages back in the day

#### Readwise
3:49 - 3:59 PM 
Superhuman email client
Twitter threads have emerged as a new form of blogging.
Attempting to create a reading app for power users
Readwise allows one to highlight images, something not currently available in other tools
Part way into their build of the product they realized they were building a web  browser


### Leveraging AI and ML in Building New Tools for Thinking
* 4:17 PM – 4:50PM 
> Alice Albrecht and Linus Lee will be sitting down with Chris Pedregal to discuss their work in leveraging AI and Machine Learning for creating new kinds of tools for thinking.

#### Q+A 
4:50 PM – 5:03 PM

### Idea Dimensionality and Representing Semantic Meaning
* 5:04 PM – 5:30 PM
> How do ideas - and the human brains that make and hold them - interact?  Get prepared for meta! Esther Dyson and Jerry Michalski, will discuss the idea of how people work together to shape, compare, intertwine and ultimately produce multi-faceted ideas and multi-dimensional idea spaces.  As David Waltz (Thinking Machines) once said, “Words are not in themselves carriers of meaning, but merely pointers to shared understanding.” Watch and lob questions as the two of them try to build and share the idea of how better ideas can be developed through collaboration.

#### Q+A
* 5:30 PM – 5:50 PM

Jerry is a fan of https://en.wikipedia.org/wiki/Hans_Monderman


### Closing and Happy Hour 
5:45 PM – 7:00 PM


## See Also
* [[commonplace books]]
* [[digital gardens]]
* [[zettelkasten]]
* [[tools for thought]]


----





