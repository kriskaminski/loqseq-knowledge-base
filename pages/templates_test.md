---
title: templates test
---

## Day
:PROPERTIES:
:template: day
:END:
### tasks
### Day
## Terry
:PROPERTIES:
:author: Pratchett
:book: all
:END:
## Tiffany
:PROPERTIES:
:author: Pratchett
:END:
##
#+BEGIN_QUERY
{:title [:h2 "Programming languages list"]
 :query [:find (pull ?b [*])
         :where
         [?b :block/properties ?p]
         [(get ?p "author") ?t]
         [(= "Pratchett" ?t)]]
 }
#+END_QUERY
