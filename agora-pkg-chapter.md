## Introduction
In this chapter we describe an **Agora**, a **social knowledge graph** provisioned and maintained by a community as a [commons](https://anagora.org/commons).

The Agora differs from other projects in the knowledge space in a few ways: whereas a **personal knowledge graph** usually contains resources authored or collected by a single person, and a **wiki** usually contains resources produced by a group, an Agora contains and integrates both personal and group resources and aims to interlink them liberally by default. 

Whereas links in a personal knowledge graph or wiki usually have a single target, **Agora links fan out by default** and can be thought of as mapping to collections. Finally, **the reference Agora tries to remain tool, format and platform agnostic**, the guiding principle being to build first on general conventions common to many tools and platforms in the knowledge space with the aim of achieving greater inclusivity and diversity.

Being a graph, an Agora can be defined as a set of vertices or **nodes** `N` (entities) and **edges** `E` (known links between entities, optionally annotated). An Agora node contains the set of all known resources about or otherwise relevant to the entity described by the node title or any provided metadata. Each such resource is called a **subnode**. Note that because links can be arbitrarily annotated (i.e. #tagged or qualified by other nearby links) and have multiplicity, the Agora is in fact a **hypergraph**.

This chapter describes a set of [[protocols]], [[contracts]] and [[goals]] that can be said to 
The free and open source reference Agora provides a minimum viable implementation of the [underlay](https://anagora.org/underlay), **interlay**, **overlay** components of a **distributed knowledge graph** based on off-the-shelf components. Individual Agora instances are expected to **federate** and organize into a greater **Agora network**. We describe how this network can integrate with the wider internet ecosystem and how it could be used to run experiments on distributed thought.

## Data format
- Plain text as layer 0
- [[wikilinks]] and #hashtags as layer 1.
- Markdown as layer 2.
- HTML, XML and other rich formats as layer 3.

## Protocol


## Federation

## Applications

### Collaboration

### Counter anti disintermediation

### Adversarial interoperability

## Thanks

To [[Flancia Collective]], [[Agora Discuss]] and [[Fellowship of the Link]] for the discussion and inspiration.

To my friends (included those in the groups above) for the support.