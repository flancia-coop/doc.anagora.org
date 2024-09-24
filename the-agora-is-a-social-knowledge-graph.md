H2 {The Agora is a Social Knowledge Graph}
[[Flancian]]

In this chapter we describe and analyze a device we call an **Agora**, being a **distributed knowledge graph** provisioned and maintained by a community, ideally as a [commons](https://anagora.org/commons). This Agora can also be said to be a **social knowledge graph** as the information it contains is produced in a social context and is contributed with a social intent.

The Agora stands out from other projects in the knowledge space in a few ways: whereas a **personal knowledge graph** usually contains resources authored or collected by a single person, and a **wiki** usually contains resources produced by a group, an Agora contains and integrates both personal and group resources and interlinks them liberally. Whereas links in a personal knowledge graph or wiki usually have a single target, **Agora links fan out by default** and can be thought of as mapping to sets of resources. Finally, whereas knowledge graphs are usually maintained using a single tool in a particular format and hosted in a centralized platform, **the reference Agora tries to remain tool, format and platform agnostic**, trying to build first on the most general conventions common to tools and platforms in the knowledge space for maximal inclusivity and diversity.

Being a graph, an Agora can be defined as a set of vertices or **nodes** `N` (entities) and **edges** `E` (known links between entities, optionally annotated). An Agora node contains the set of all known resources about or otherwise relevant to the entity described by the node title or any provided metadata. Each such resource is called a **subnode**.

Note that because links can be arbitrarily annotated (i.e. #tagged or qualified by other nearby links) and have multiplicity, the Agora is in fact a **hypergraph**.

On a system level, the free and open source reference Agora provides a minimum viable implementation of the [underlay](https://anagora.org/underlay), **interlay**, **overlay** components of a distributed knowledge graph.

Individual Agora instances are expected to **federate** and organize into a greater **Agora network**.

--

In this chapter we might also describe said reference Agora further and go into how we are using it to iterate on the system design and run experiments.

Some hypotheses that we are exploring follow:

- A knowledge commons can provide utility to participating communities efficiently, as the cost of systemic integrations within a pro-social **hub design** such as that of the reference Agora can scale with `O(N)` instead of the `O(N^2)` provided by a naive full mesh (N being the number of integrations, e.g. tools or platforms connected).
- Going from a set of voice-preserving individual contributions to a shared group resource might be an efficient way to foster **opportunistic collaboration** at scale.
- **Social** loose linking and opportunistic heterarchical categorization might complement traditional taxonomic approaches better than the same tried at the individual level by virtue of network effects. This might enable convergence on meaning and other emergent behaviour.