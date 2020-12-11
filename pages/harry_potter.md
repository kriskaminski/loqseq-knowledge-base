---
title: Harry Potter
---

## [[Ron Wesley]]
## [[Hermiona Granger]]
##
#+BEGIN_QUERY
{:title "All pages have a *programming* property"
 :query [:find ?name
         :in $ ?property
         :where
         [?t :property/name ?property]
         [?p :page/properties ?t]
         [?p :page/name ?name]]
 :inputs ["book"]
 :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "/page/" page)} (clojure.string/capitalize page)])])}
#+END_QUERY
##
