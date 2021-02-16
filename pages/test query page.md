---
title: Test Query Page
---

## {{query 
#+BEGIN_QUERY
      {:title "📅 NEXT"
    :query [:find (pull ?h [*])
            :in $ ?start ?next
            :where
            [?h :block/marker ?marker]
            [?h :block/ref-pages ?p]
            [?p :page/journal? true]
            [?p :page/journal-day ?d]
            [(> ?d ?start)]
            [(< ?d ?next)]
            [(contains? #{"NOW" "LATER" "DOING" "TODO"} ?marker)]]
    :inputs [:today :10d-after]
    :collapsed? false}
#+END_QUERY



}}
