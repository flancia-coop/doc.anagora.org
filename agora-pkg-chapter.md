## Introduction

- In this chapter we describe an **Agora**, a **social knowledge graph** provisioned and maintained by a community as a [commons](https://anagora.org/commons).
- The Agora differs from other projects in the knowledge space in a few ways: 
    - Whereas a **personal knowledge graph** usually contains resources authored or collected by a single person, and a **wiki** usually contains resources produced by a group, an Agora contains and integrates both personal and group resources and aims to interlink them liberally by default. 
    - Whereas links in a personal knowledge graph or wiki usually have a single target, **Agora links fan out by default** and can be thought of as mapping to collections. 
    - Finally, **the reference Agora tries to remain tool, format and platform agnostic**, the guiding principle being to build first on general conventions common to many tools and platforms in the knowledge space with the aim of achieving greater inclusivity and diversity.
- This chapter describes a set of [[protocols]], [[contracts]] and [[goals]] that can be said to define an Agora. It also covers a reference implementation of such a construct as free software, and potential applications of a network built around such a platform in the [[knowledge]] and [[social]] domains.
- We also cover details of a free and open source reference Agora which provides a minimum viable implementation of the [underlay](https://anagora.org/underlay), **interlay**, **overlay** components of a **distributed knowledge graph**.
    - This reference system is based on off-the-shelf components like Markdown and git. 
    - Individual Agora instances are expected to **federate** and organize into a greater **Agora network**. 
    - We describe how this network can integrate with the wider internet ecosystem and how it could be used to run experiments on distributed thought.

## Graph definition 
- Being built around a knowledge graph, an Agora can be defined as a set of vertices or **nodes** `N` (each mapping to an entity in a knowledge base) and **edges** `E` (each mapping to a relationship between entities, optionally annotated). 
    - An Agora [[node]] contains the set of all known resources *about* (or *related* to) the entity described by the node id, defaulting to its name as an arbitrary length unicode string. 
        - (But potentially overrided or extended with provided metadata and annotations.)
        - In this paper each such resource attached to node `N` is called a **subnode** `N_s`. 
    - Note that because links can be arbitrarily annotated (as they can be considered named according to . nearby #tags and [[wikilinks]]), the Agora graph can be seen to be a **hypergraph** [^hypegraph].

[^hypergraph]: And thus may be sufficient to efficiently encode any data structure as per Wolfram et al.

## Data format
- Layer 0: [[plain text]].
    - Plain text is ubiquituous.
    - It is not only a common standard for all tools in the knowledge space, which simplifies interoperability; it is a common standard for thought as shown by thousands of years of preserved culture.
    - It can trivially encode outlines.
        - It can be made to encode trees, like in this example.
    - It generalizes to binary data.
        - It can be made to encode arbitrary data via application of uuencode or other encoding conventions.
- Layer 1: [[markup]] and conventions for cross-referencing and linking.
    - Markdown, org mode, HTML or other rich markups building on top of plain text belong to this layer.
    - [[wikilinks]] and #hashtags seem like sensible cross-format extensions for semantic linking.
    - More generally, this is an [[inline metadata]] layer. The above are just relatively unobstrusive generally available implicit standards that inline well.
- Layer 3: JSON, EDN, RDF, protobufs.
    - In general, data exchange formats.
    
## Data model
- Users can contribute individual resources to an Agora.
    - To do so, as of the time of writing, they can:
        - Submit a URL plus a set of relevant nodes the resource should be attached to.
        - Interact with an Agora system account (i.e. bot) in supported platforms like social media while indicating relevant nodes using a Layer 1 convention.
- Users can contribute repositories to an Agora.
    - To do so, they publish their resources to a repository they control and then they let an Agora know of their intention to integrate, a desired username and their agreement with an AGora

## Protocol


## Federation

## Applications

### Collaboration

### Counter anti disintermediation

### Adversarial interoperability

## Thanks

To [[Flancia Collective]], [[Agora Discuss]] and [[Fellowship of the Link]] for the discussion and inspiration.

To my friends (included those in the groups above) for the support.