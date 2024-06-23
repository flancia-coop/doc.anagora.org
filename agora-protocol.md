Self: [flancia.org/go/agora-protocol](http://flancia.org/go/agora-protocol)

See also: flancia.org/agora (motivation and TLDR), [flancia.org/go/agora](http://flancia.org/go/agora) (early stage implementation), [flancia.org/go/agora-roadmap](http://flancia.org/go/agora-roadmap) (roadmap)

By: [[D. W.]], [[Flancian]], your name here!

**[Meta, and a note to contributors](#_aj3q4ry5d83x) 1**

**[Background](#_3eqemxdhgf1m) 1**

[Wikilinks](#_5cbrmexi5exl) 2

[Backlinks](#_kq6hhyllsx2e) 2

[Block references](#_qzyeq2l8mef2) 2

[Multi-user experience](#_s9cref8d65dp) 2

**[Proposal](#_7og55z6k3nv0) 2**

[Concepts](#_980lm5aevkiv) 3

[Multinodes, or constructive conflict handling](#_633wbc2fqf1v) 3

[Other clients](#_gk5lbppzxvux) 3

[Data format](#_wax3irvckshk) 3

[Go links](#_41drleozcqrb) 4

[Contexts](#_x8svdb9axfmf) 4

[Open questions](#_kovtovaz35su) 4

**[Possible Applications](#_4tdtpf29ytug) 4**

## Meta, and a note to contributors

- _Agora_ is just a working code name; it is a recurrent label that one of the authors has been using as a placeholder for a set of concurrent, only occasionally convergent ideas. Please feel free to propose a different name, or indeed to ignore the name overall.
- This document will probably make use of unresolved [[wikilinks]] both for the purpose of demonstrating the concept and labelling entities. Eventually this text is expected to move into a reference Agora, and such links will resolve.
- I tried keeping Background to about one page and Proposal to about one page. Unsure if this is the right proportion/format at all. Open to any and all feedback :)

## Background

_The Agora is an annotation layer for the internet based on a loosely coupled socially maintained [[_[_distributed knowledge graph_](http://flancia.org/go/distributed-knowledge-graphs)_]] based on [[_[_wikilinks_](http://flancia.org/go/wikilinks)_]] and back references._

Some conventions may be emerging in a new batch of personal knowledge management tools
# 1
, or amenable to them; for the duration of this document, we&#39;ll refer to these tools as [_Roam-like_](http://flancia.org/mine/roam-like). These systems have caught on over more legacy apps such as Evernote, because associations can be created in a mesh or graph style between concepts and notes instead of relying on folders and more traditionally hierarchical organizational approaches.

This document seeks to explore common ground and propose a way towards a protocol for cross-tool distributed collaboration including aspects like interop, federation, etc.

### Wikilinks

The ubiquity of [[[wikilinks](https://en.wikipedia.org/wiki/Help:Link)]] is a notable innovation over the previous batch of Personal Knowledge Management tools. The [[wikilink]] convention is in wide use not only in wikis proper, but also in all Roam-likes.

At their core, they allow a user to quickly make a relative &quot;wiki-style link&quot; between a note in one place and a note or concept in another. Typically the user will employ a wiki-like convention to begin-- for instance, typing &quot;[[&quot;-- at which point an increasingly constrained set of options will be offered in real time as the user continues typing, against a set of notes or concepts that have already been created in their personal knowledge graph.

As of the time of writing, all Roam-likes support [[wikilinks]] with optimistic resolution
# 2
; following a non-existent [[wikilink]] triggers a new note creation. This **encourages link-driven writing and enables users to easily create stub pointers to entries to be filled in later.**

### Backlinks

Backlinks are core to the note taking and navigation experience in Roam-likes. They are the main innovation over most common Wiki tools previously in widespread use.

Backlinks are usually implemented as a list of incoming edges to the currently focused node.

### Block references

Block references are critical to some, but not all, of Roam-likes; notably Roam Research and Athens Research support them. Block references are an instance of block-level transclusion.

Obsidian, Foam and other players either don&#39;t support References at all or support only limited forms (e.g. Obsidian can transclude sections only). It is unclear whether this should be a core feature of a protocol aiming to federate between tools.

### Multi-user experience

At the time of writing Roam is the only tool with an established multi-user (a.k.a. &quot;multiplayer&quot;) experience being developed.

## Proposal

We propose to develop Agora, a protocol that

1. Enables interop between Roam-likes and the rest of the participating internet, in particular the [[[fediverse](http://anagora.org/node/fediverse)]] and the [[[semantic web](http://anagora.org/node/semantic-web)]].
2. Offers a common interface for tools targeting Roam-like databases as knowledge graph backends.

### Concepts

An _Agora_ hostsa collection of interlinked _gardens_
_# 3_. Each garden is an instance of a personal knowledge graph such as that produced by any Roam-like targeting a database. For the purpose of this document, assume that distinct users A, B and C all publish their digital gardens in an Agora.

### Multinodes, or constructive conflict handling

Whereas in a Garden each node id is expected to be unique, in an Agora conflicts are desired and enable _multinoding_
_# 4__._Assume users A and B have nodes in their gardens with a given id, for example _Stoa_.

Multinoding results in the following behaviour:

- When a user of the Agora (not necessarily A or B) visits a [[Stoa]], _both_ A and B&#39;s nodes will resolve, and be shown one after the other.
- When user C creates a new node in [[Stoa]], they are made aware of A and B&#39;s node (it is shown as related context).

### Other clients

One of the most common uses of tools such as Hypothesis is for users to create annotations which are then imported into a wiki-note application for other purposes.

An obvious affordance would be for folks to directly reference their or other&#39;s knowledge graphs in their own annotation bodies. Both the Hypothesis app and others in this category are often using a flavor of markdown as the editor syntax, so the applications are already conceptually similar to each other.

Annotation tools could connect to an Agora of the user&#39;s choosing so that while an annotation was being created, a direct reference to a concept node could be created inline. The editor would need to be able to query the remote knowledge graph in real time such that candidate concepts could be presented as the user types, just like in a native client. One could imagine this kind of capability becoming social, if some knowledge graphs were exposed publicly and one could query across them and choose amongst them. In this way, if the Hypothesis note were to be exported to another system— including the remote knowledge app itself— the direct reference to the graph would automatically work.

### Data format

Most Roam-likes, with the notable exception of Roam, store their data as plain Markdown files. This makes their databases amenable to being hosted in common version control systems.

With the exception of block references, Roam notes can be exported to this format in a lossless way.

The [Agora v0.5 reference implementation](http://flancia.org/go/agora) makes use of this data format and is based on git subtrees. This makes it so that each participating user can host their gardens independently, and rely on the Agora exclusively for Agora-enabled flows (such as multinoding and publishing).

### Contexts

To be written. See [[[distributed knowledge graph](http://flancia.org/go/distributed-knowledge-graph)]].

### Open questions

- Should [[wikilink]] resolution collapse or maintain plurals and other common variations? Same for go links.

## Possible Applications

### Go links

Note [[[go links](http://flancia.org/mine/go-links)]] and [[wikilinks]] have synergies. Go links can be seen as HTTP 302 as a service; they can provide both simple social bookmarking (letting users easily claim &quot;URL space&quot;) and be seen as a social knowledge graph client. Making clients resolve also resolve [[wikilinks]] to [[go links]] as published by participating domains (perhaps those in a list controlled by the user, or those of their &quot;friends&quot;) would allow users to crowdsource interesting targets.

### Wikilinks everywhere

See: [anagora.org/go/wikilinks-everywhere](http://anagora.org/go/wikilinks-everywhere).

[1](#sdfootnote1anc)Roam Research; Athens Research; Obsidian; Foam; Notion.

[2](#sdfootnote2anc) Or as Ward Cunningham said: &quot;When you reach the edge of your knowledge, create a new Wiki Page&quot; (h/t Gyuri Lajos for the quotation).

[3](#sdfootnote3anc) The term comes from _digital garden_, as exposed in [https://joelhooks.com/digital-garden](https://joelhooks.com/digital-garden).

[4](#sdfootnote4anc) Noding is borrowed from [everything2.com](http://everything2.com/), which successfully explored a similar setup.