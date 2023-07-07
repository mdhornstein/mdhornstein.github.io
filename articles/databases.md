--- 
layout: default_math
--- 

We discuss databases and related concepts.  

A table in SQL can be seen as a relation, where each row of the table is a tuple.  

A set of attributes $$(A_1, A_2, \ldots, A_m) $$ functionally determines another set of attributes $$(B_1, B_2, \ldots, B_n)$$ if 

* The concept of "functionally determines" is somehow the opposite of "conditinoal independence".  There is an axiomatization of conditinoal independence given in Lauritzen. Is there an analogous way to give an axiomatic definition of functionally determines. There are some key properties that hold. (todo: provide a list of those key properties and a reference.


* Interesting question: Does the functional dependence symbol $$\rightarrow$$ work the same way as "implies" (the material conditional)?  It seems like it satisfies the same properties.  

* Also a conneection to logic and worlds



* What is the overall conceptual structure here?  There is a formal system that describes some mathematical entity. The formal system consists of an alphabet, well-formed strings (which can be specified by a grammar), and rules of inference (i.e. typographical rules that tell you how to derive strings from other strings). This formal system models our intuitive notion of logic and logical inference.

* In group theory, we define group axioms, and we discover that many specific examples of mathematical objects satisfy the group axioms, so anything we prove about groups holds for all of these mathematical objects.  Likewise, we can axiomatize logic (with e.g. first-order propositional logic). Is there an analogous phenomenon, where there are many specific examples of mathematical objects that all satisfy the axioms of first-order logic?  It seems like one candidate example is the functinoal dependency, which (I think) satisfies the same properties as the material conditional.

* Maybe that's why I had this intuition about the connection to first-order logic.

* Maybe the material conditional and functional dependencies are examples that can motivate an axiomatic definition based on those three properties.  Then that axiomatic definition can stand in opposition to the axioms for conditional independence.  (reflexivity, augmentation, transitivity). Why do we need augmentation?  
