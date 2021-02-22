---
title: Test Query Page
---

##
#+BEGIN_QUERY
{:title "All tasks"
 :query [:find (pull ?b [*])
         :where
         [?b :block/marker ?m]
         [(not= ?m "nil")]]}
#+END_QUERY
## {{query [[recipes]]}}
## {{query ((between -7d +7d) )}}
