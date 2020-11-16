---
title: properties
---

## CLJ
:Composer:  J.S. Bach
:Artist:    Glenn Gould
:Publisher: Deutsche Grammophon
:NDisks:    1
##
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
