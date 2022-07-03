## Introduction

- In this chapter we describe an **Agora**, a **social knowledge graph** provisioned and maintained by a community as a [commons](https://anagora.org/commons).
- The Agora differs from other projects in the knowledge space in a few ways: 
    - Whereas a **personal knowledge graph** usually contains resources authored or collected by a single person, and a **wiki** usually contains resources produced by a group, an Agora contains and integrates both personal and group resources and aims to interlink them liberally by default. 
    - Whereas links in a personal knowledge graph or wiki usually have a single target, **Agora links fan out by default** and can be thought of as mapping to collections. 
    - Finally, **the reference Agora tries to remain tool, format and platform agnostic**, the guiding principle being to build first on general conventions common to many tools and platforms in the knowledge space with the aim of achieving greater inclusivity and diversity.
- This chapter describes a set of [[protocols]], [[contracts]] and [[goals]] that can be said to define an Agora. It also covers a reference implementation of such a construct as free software, and potential applications of a network built around such a platform in the [[knowledge]] and [[social]] domains.
- We also cover details of a free and open source reference Agora which provides a minimum viable implementation of the [underlay](https://anagora.org/underlay), **interlay**, **overlay** components of a **distributed knowledge graph**.
    - This reference system on off-the-shelf components. Individual Agora instances are expected to **federate** and organize into a greater **Agora network**. We describe how this network can integrate with the wider internet ecosystem and how it could be used to run experiments on distributed thought.

## Graph definition 
- Being built around a knowledge graph, an Agora can be defined as a set of vertices or **nodes** `N` (each mapping to an entity in a knowledge base) and **edges** `E` (each mapping to a relationship between entities, optionally annotated). 
    - An Agora [[node]] contains the set of all known resources *about* (or *related* to) the entity described by the node id, defaulting to its name as an arbitrary length unicode string. 
        - (But potentially overrided or extended with provided metadata and annotations.)
        - In this paper each such resource attached to node `N` is called a **subnode** `N_s`. 
    - Note that because links can be arbitrarily annotated (as they can be considered named according to . nearby #tags and [[wikilinks]]), the Agora graph can be seen to be a **hypergraph** and thus is believed to be generally sufficient to efficiently encode any data structure.

## Data format
- Plain text as layer 0.
    - Plain text is ubiquituous.
    - It is not only a common standard for all tools in the knowledge space, which simplifies interoperability; it is a common standard for thought as shown by thousands of years of preserved culture.
    - It can trivially encode outlines.
        - It can be made to encode trees, like in this example.
    - It generalizes to binary data.
        - It can be made to encode arbitrary data via application of uuencode or other encoding conventions.
- Markup formats and conventions for referencing and linking as layer 1.
    - Markdown, org mode, HTML or other rich markups building on top of plain text belong to this layer.
    - [[wikilinks]] and #hashtags seem like sensible cross-format extensions for semantic linking.
    - More generally, a [[metadata]] layer. The above are just relatively unobstrusive generally available implicit standards that inline well.
- JSON, EDN, RDF, protobufs as layer 3.
    - In general, data exchange formats.
    
## Repository definition
- A data is 

## Protocol


## Federation

## Applications

### Collaboration

### Counter anti disintermediation

### Adversarial interoperability

## Thanks

To [[Flancia Collective]], [[Agora Discuss]] and [[Fellowship of the Link]] for the discussion and inspiration.

To my friends (included those in the groups above) for the support.