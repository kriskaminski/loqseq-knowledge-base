---
title: properties
---

## CLJ
:Title:     Goldberg Variations
    :Composer:  J.S. Bach
    :Artist:    Glenn Gould
    :Publisher: Deutsche Grammophon
    :NDisks:    1
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
