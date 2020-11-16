---
title: properties
---

## re
## propblock
sfda
##
#+BEGIN_QUERY
{:title [:h2 "myprop list"]
 :query [:find (pull ?b [*])
         :where
         [?b :block/properties ?p]
         [(get ?p "type") ?t]
         [(= "Composer" ?t)]]
 }
#+END_QUERY
