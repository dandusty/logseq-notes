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
## {{query (between [[Dec 5th, 2020]] [[Dec 7th, 2020]] )}}
##
#+BEGIN_QUERY
{:title [:h2 "Books List"]
 :query [:find (pull ?b [*])
         :where
         [?b :block/properties ?p]
         [(get ?p "type") ?t]
         [(= "Book" ?t)]]
 :view (fn [result]
         (when (seq result)
           (let [blocks (flatten result)]
             [:div.table-wrapper
              [:table.table-auto
               [:thead
                [:tr
                 [:th {:width "20%"} “Title"]
                 [:th {:width "20%"} "Author"]
                 [:th {:width "60%"} "Pages"]]]
               [:tbody
                (for [{:block/keys [title properties]} blocks]
                  [:tr
                   [:td (second (:url (second (first title))))]
                   [:td (get properties "creator")]
                   [:td (get properties "description")]])]]])))
 }
#+END_QUERY
## {{query (page-property type book )}}
