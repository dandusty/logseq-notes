---
title: Logseq Query Ideas
---

## All scheduled
#+BEGIN_EXAMPLE
#+BEGIN_QUERY
{:title "All scheduled" :query [:find (pull ?b [*]) :where [?b :block/scheduled]]}
#+END_QUERY
#+END_EXAMPLE 



All deadlines
#+BEGIN_EXAMPLE
#+BEGIN_QUERY
{:title "All deadlines" :query [:find (pull ?b [*]) :where [?b :block/deadline]]}
#+END_QUERY
#+END_EXAMPLE 


All scheduled OR deadlines

#+BEGIN_EXAMPLE
#+BEGIN_QUERY
{:title "All scheduled OR deadlines" :query [:find (pull ?b [*])  :where (or [?b :block/scheduled] [?b :block/deadline])]}
#+END_QUERY
#+END_EXAMPLE 


All scheduled AND deadlines (block must have both attributes)
#+BEGIN_EXAMPLE
#+BEGIN_QUERY
{:title "All scheduled AND deadlines" :query [:find (pull ?b [*])  :where [?b :block/scheduled] [?b :block/deadline]]}
#+END_QUERY
#+END_EXAMPLE
