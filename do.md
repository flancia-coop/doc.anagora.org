I think I'm going to start using the stoa in [[do]] to keep my top level todo list -- or at least my [[inbox]]. Unfortunately [[do]] the node is overloaded, and this is very convenient as I can just edit it in any browser :) Feel free to do the same if it helps! (I'll likely soon add one doc per user in the Agora.)

# [[flancian]]
- write [[building bridges]]
  - I think about this a lot but for some reason I never get to work on it
  - related to [[knowledge commons]] and [[protopoi]]
      - the [[commons]] aspect is probably top priority
- code [[agora bridge]]
  - [x] [[agora bot replies to wikilinks from followers]]
  - [x] [[agora bot links wikilinked posts from followers]]
  - [ ] [[agora bot]] links from [[matrix]]
  - [ ] [[agora bot stores messages for users]]
      - we are for now blocking on giving each user an independent (git) repository that stores their messages instead of using a centralized approach.
- code [[auto pull]]
  - perhaps base it on inline transclusion like wikipedia/url pulls
  - this is partially implemented now, finally
- code [[auto push]]
  - [[foo]]
      - foo gets this line auto pushed because it's a wikilinked parent of a block (as defined by indentation or user set syntax)
      - this is still not done surprisingly! I'm not sure it's actually blocking on getting a proper [[agora protocol]] [[ast]]; we could extend the current [[lxml]]-based hack.
- #pull [[todo]], [[now]], [[later]], [[plan]]
- see also: [[did]], [[done]] :)