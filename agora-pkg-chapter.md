## Introduction

- In this chapter we describe an **Agora**, a **social knowledge graph** provisioned and maintained by a community as a [commons](https://anagora.org/commons).
    - An Agora is designed to be cooperative platform that integrates and complements personal knowledge graphs with minimal effort.
- The Agora differs from other projects in the knowledge space in a few ways: 
    - Whereas a **personal knowledge graph** usually contains resources authored or collected by a single person, and a **wiki** usually contains resources produced by a group, an Agora contains and integrates both personal and group resources and tries to interlink them liberally by default. 
    - Whereas links in a personal knowledge graph or wiki usually have a single target, **Agora links fan out by default** and its targets can be thought of as mapping to collections. 
    - Whereas some tools in the personal knowledge graph space are exploring collaborative editing in an idiosyncratic way, **the reference Agora tries to remain tool, format and platform agnostic**, the guiding principle being to build first on general conventions common to many tools and platforms in the knowledge space with the aim of achieving greater inclusivity and diversity.
- This chapter describes a set of [[conventions]], [[protocols]], and [[contracts]] that can be said to define an Agora. It also covers a reference implementation as free software, and potential applications of a network built around such a platform in the [[knowledge]] and [[social]] domains.
- We also cover details of a free and open source reference Agora which provides a minimum viable implementation of the [underlay](https://anagora.org/underlay), **interlay**, **overlay** components of a **distributed knowledge graph**.
    - This reference system is based on off-the-shelf components like Markdown and git. 
    - Individual Agora instances are expected to **federate** and organize into a greater **Agora network**. 
    - We describe how this network can integrate with the wider internet ecosystem and how it could be used to run experiments on distributed thought.

## Graph definition 
- Being built around a knowledge graph, an Agora can be defined as a set of vertices or **nodes** `N` (each mapping to an entity in a knowledge base) and **edges** `E` (each mapping to a relationship between entities, annotated by context). 
    - An Agora [[node]] is a collection; it contains the set of all known resources *about* (or *related* to) the entity described by the node id, defaulting to its name as an arbitrary length unicode string. 
        - (But potentially overrided or extended with provided metadata and annotations.)
        - In this paper each such resource attached to node `N` is known as a **subnode** `N_s`. 
    - Note that because links can be arbitrarily annotated (as they can be considered according to nearby #tags and [[wikilinks]]), the Agora graph can be seen to be a **hypergraph** [^hypergraph].

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
- Users can contribute individual [[resources]] to an Agora.
    - To do so, as of the time of writing, they can:
        - Submit a URL plus a set of relevant nodes the resource should be attached to.
        - Interact with an Agora system account (i.e. bot) in supported platforms like social media while indicating relevant nodes using a Layer 1 convention.
- Users can contribute [[repositories]] to an Agora.
    - To do so, they publish their resources to a repository they control and then they let an Agora know of their intention to integrate, a desired username and their agreement with an Agora's contract.

## Protocol
- See https://anagora.org/go/agora-protocol.

## Federation

The Agora should be built on a federated protocol to limit the negative impact of diasporas. Groups might temporarily diverge in their views enough to want to run separate Agoras, but different Agoras should be able to cooperate on problems and solutions for which there is enough ideological alignment, and eventually merge back.

## Applications

### Collaborative problem solving

- One of the best possible uses for such a network would be to use it to pro-socially maintain a distributed knowledge graph tailored specifically to the goal of solving problems: those of its users and society at large.
- Its users, as a cooperative group, could by default take a naive but rational approach to problem solving:
    - For each problem in the set P of all problems:
        - Describe it as thoroughly as possible.
        - Maintain a set of known or argued possible solutions, S(P).
    - For each solution in S(P):
        - Describe it as thoroughly as possible.
        - Maintain a set of resources (people, time, attention, money) needed to implement it, R(S).
    - Individual users could also declare their views on the state of the world explicitly: they define which subsets of P, S and R they agree with, in the sense that they believe they are feasible, true, interesting.
- Users that agree on their defined subsets can then efficiently collaborate on solutions as they become available by pooling of resources.
- We apply some good old recursivity and seed the Agora with the problem of how to build itself. That is, how to build a system that allows participating users and entities to collaborate optimally in the face of adversity (such as biases, irrationality and even actual ill intent)1.

### Counter anti disintermediation
- An Agora can be used to solve coordination problems like those at the heart of enabling users to leave walled gardens and other systems whose design causes anti disintermediation.

### Adversarial interoperability
- An Agora can be used to let users regain control of their data from entities which by default are not proactive enough or flexible enough when stewarding or relinquishing control of user data.

### Network flow
- We bootstrap a Universal Basic Income experiment using the Agora with a set of simple rules:
    - If you consider yourself under-privileged, you sign up to receive an income.
    - If you consider yourself over-privileged, you sign up to donate an income.
    - Incomes are recurring donations for a set number of months.
- Optional virality rule: the person receiving the income should elect to forward e.g. 10% of the sum received to someone less privileged than them.
    - The virality rule both pushes network growth and constructively exploits wealth inequality and asymmetry of information: an under-privileged person is closer in the world to a more severely under-privileged person than the initial donor, so can more efficiently allocate the resources. This also empowers under-privileged people to also make ethical decisions.

## Thanks

To [[Flancia Collective]], [[Agora Discuss]] and [[Fellowship of the Link]] for discussion and inspiration. To my friends for the support.