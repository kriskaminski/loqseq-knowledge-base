---
title: properties
---

## Clojure
## CLJ
##
#+BEGIN_QUERY
{:title [:h2 "myprop list"]
 :query [:find (pull ?b [*])
         :where
         [?b :block/properties ?p]
         [(get ?p "type") ?t]
         [(= "myprop" ?t)]]
 }
#+END_QUERY
