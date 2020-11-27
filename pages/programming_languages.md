---
title: Programming languages
---

##
#+BEGIN_QUERY
{:title "All pages have a *programming language* tag"
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
