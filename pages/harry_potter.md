---
title: Harry Potter
---

## [[Ron Wesley]]
## [[Hermiona Granger]]
##
#+BEGIN_QUERY
{:title "wszystkie książki"
 :query [:find ?name
         :where
         [?t :tag/name ?tag]
         [?p :page/properties ?a]
         [?p :page/name ?name]]
 :inputs ["book"]
 :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "/page/" page)} (clojure.string/capitalize page)])])}
#+END_QUERY
