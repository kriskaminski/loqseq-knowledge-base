---
title: Programming languages
---

##
#+BEGIN_QUERY
{:title "All pages have a programming language tag"
 :query [:find ?name
         :in $ ?tag
         :where
         [?t :tag/name ?tag]
         [?p :page/tags ?t]
         [?p :page/name ?name]]
 :inputs ["programming-language"]
 :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "/page/" page)} (clojure.string/capitalize page)])])}
#+END_QUERY
##
#+BEGIN_QUERY
{:title "All page tags"
:query [:find ?tag-name
        :where
        [?tag :tag/name ?tag-name]]
:view (fn [tags]
        [:div#query-all-page-tags
         (for [tag (flatten tags)]
           [:a.tag.mr-1 {:href (str "/page/" tag)}
            (str "#" tag)])])}
#+END_QUERY
##
#+BEGIN_QUERY
{:title "Block tag list"]
 :query [:find (pull ?b [*])
         :where
         [?b :block/tags ?t]]}
#+END_QUERY
##
#+BEGIN_QUERY
{:title "DEVOPS"
 :query [:find (pull ?b [*])
         :where
         [?b :block/tags ?tag]]}
#+END_QUERY
## doker #devops
## kubernetes #devops
##
##
#+BEGIN_QUERY
{:title "All page tags"
:query [:find ?tag-name
        :where
        [?tag :tag/name ?tag-name]]
}
#+END_QUERY
