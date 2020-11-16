---
title: templates test
---

## Day
:PROPERTIES:
:template: day
:END:
### tasks
### Day
### ttt
:PROPERTIES:
:props: working 
:END:
###
## Terry
:PROPERTIES:
:author: Pratchett
:book: all
:END:
## Tiffany
:PROPERTIES:
:author: Pratchett
:book: Kapelusz pełen nieba
:END:
##
#+BEGIN_QUERY
{:title "Programming languages list"
 :query [:find (pull ?b [*])
         :where
         [?b :block/properties ?p]
         [(get ?p "author") ?t]
         [(= "Pratchett" ?t)]]
 }
#+END_QUERY
