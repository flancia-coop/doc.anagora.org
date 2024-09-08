See also:

- [[[metasj flancian](http://anagora.org/go/metasj-flancian)]]
- [[[social knowledge graphs discussion](http://anagora.org/node/social-knowledge-graph-discussion)]]

By: [[[samuel klein](http://anagora.org/node/samuel-klein)]], [[[dan whaley](http://anagora.org/node/dan-whaley)]], [[[flancian](http://anagora.org/node/flancian)]], your\_name\_here

## Project description

**Wikilinks everywhere: a web extension/library/bookmarklet that eagerly or lazily resolves [[**[**wikilinks**](http://anagora.org/node/wikilinks)**]] in any web property within a user-chosen context, e.g. an Agora or other distributed knowledge graph.**

While using the web, users often need to interact with or refer to their **personal knowledge databases (PKB)**. This means taking notes (about web content or otherwise), and then **referring** and **linking** to them (as they can be resolved in their PKB). This process is needlessly cumbersome; users often _know_ precisely which PKB entries they would like to refer to, and can remember their titles, but have no interactive, real time way to **insert** or **resolve** these links. Currently they need to go through a multi-step process to fetch them (open database; search for them; select them; get a canonical URL if available; copy/paste it and any relevant information), or they&#39;ll flag the term and remember to revisit it later. Instead, a user could type [[_wikilink_]], with wikilink standing for the title of the note in question, and depend on a **web extension** to resolve the note reference to canonical URL either eagerly (at the time of writing) or lazily (at read-time).

## Use cases

- As a writer, I know that a KB entry exists, but don't have immediate access to it. So, when I am typing I&#39;ll create a stub pointer to a KB entity by typing "[[entity]]". At some point later, those links will be resolved by an asynchronous process.
- As a writer, I want immediate access to my KB graph, or other public graphs I&#39;m connected to, wherever I am so that as I&#39;m taking notes around the web I can add wikilinks in real time through the wikilink convention &quot;[[entity]]&quot;. Real-time KB linking should work w/ type-ahead so that as I&#39;m typing, suggestions of entities that satisfy the characters I&#39;ve typed (from whichever KB) are presented instantaneously, and I can click to confirm.
- Unresolved [[wikilinks]] as produced by users through the above use case could be resolved _socially_; that is, the resolution need not be scoped necessarily to a particular personal knowledge graph, but rather to a set of them. This opens up a second use case: that in which a _reader_ of an unresolved [[wiklink]] created by a third party can choose to resolve the wikilink in a user-specified content; by default, their own knowledge base or user chosen set of knowledge bases (Agora).
  - Note that, if the above use cases prove popular/valuable, unresolved [[wikilinks]] may proliferate within certain social circles and drive adoption of the system.

## Applications

- Ex: resolving wikilinks on hypothes.is notes. [default InstantLinks]
- Ex: resolving wikilinks in Twitter, Facebook, Google Docs/Etherpad -- anywhere there is user generated content that happens to make use of them.
- Make this work with [[w:Wikis]], [[d:Wikidata]], [[f:Files]], and {{t:Templates}}
  - Then make subst: work [like \_flattening\_ for go-links]
- Make a default resolution pathway for each source, &amp;
 a default meta-resolution $path (where to look for the pathway config)
  - $path can include localfile, agora:config, metawiki:config, ul:r ...
- could say: whenever you force flattening of a link [in agora] you could explicitly note this as an addition

## Resolution flow

- The extension should maintain a list of &#39;wikilink providers&#39;, that is, sites that are known to offer wikilink resolution as a service.
- The user can configure resolution priority for providers.
- The extension may default to resolving wikilinks to the top priority provider in every case, although it may also choose to do background presence checks to link wikilinks at the top priority provider that already hosts a valid node in the wikilink in question.

[[foo]] -\&gt; $base\_url/foo

## Plan

- Define an interface to resolve wikilinks in an Agora/DKG
  - Could be [[[agora protocol](http://anagora.org/go/agora-protocol)]] or a simpler subset.
  - Default: /resolve/\&lt;node\&gt; returns:
    - Json with node information, including canonical URL (to point the wikilink to) and perhaps optimally full node information (like number of subnodes, content) to inline as the client sees fit.
  - Alternative: /api/v0/node/\&lt;node\&gt;
- Implement interface as per the above
  - Estimate: ~2h
- Write a browser extension that resolves wikilinks in a given Agora using the above
  - MVP: fetches the list of [[wikilinks]] in the current page and builds links to those resolved in a default Agora.
    - Usability improvement: actually live-links them by modifying the DOM
  - Next action: find a good &quot;hello world&quot; extension to base this on? Perhaps ideally written in typescript
    - See perhaps [[[browser extensions](http://anagora.org/node/browser-extension)]] for breadcrumbs (check)
    - https://github.com/MarkaPola/Linkificator[https://github.com/MarkaPola/Linkificator](https://github.com/MarkaPola/Linkificator) could be a reasonable base, license is MPL.
    - [https://github.com/eight04/linkify-plus-plus](https://github.com/eight04/linkify-plus-plus) is BSD
    - These two may give ideas for live suggestions while writing: [Type Autosuggest](https://addons.mozilla.org/en-US/firefox/addon/type-autosuggest/) and [TextFast](https://addons.mozilla.org/en-US/firefox/addon/textfast/).

## Side projects

- Chat
  - Zulip streams could map to Agora nodes
  - Related because it&#39;s another type of wikilink integration adapted to a particular website
  - Make use of the magic-hat node-resolution that&#39;s trustworthy.
- Twitter
  - See anagora.org/node/agora-twitter-integration