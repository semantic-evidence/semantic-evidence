# Representation of assertion subjects #
Part of the SEE approach is the structured representation of assertion subjects i.e. of _what_ is asserted in each assertion.

While representation of a claim **using an assertion instance as a representational primitive is possible**, adding a **structured representation** of the claim subject **enables representing, querying and evaluating the entities forming the subject** of a claim, e.g., the actual **materials, methods, data items or other entities** about which assertions are made.

### To this end each `rdo:assertion` instance is linked to a corresponding `rdo:proposition` instance the IRI of which identifies a named RDF graph. ###

**This graph** provides a structured representation of the assertion subject using appropriately defined resources. This setup enables querying the elements forming the assertion subject.

## Example ##
In assertion A10 it is asserted by Tate and co-workers that the particular assay they performed was a γ-GHS assay. The representation of this statement as a graph identified by the IRI of the proposition instance linked to the assertion instance representing A10 enables to access the entities A10 is about: the particular assay, its asserted type, and the typing relation itself.

![http://semantic-evidence.googlecode.com/svn/wiki/images/figure-5-assertion-subjects.png](http://semantic-evidence.googlecode.com/svn/wiki/images/figure-5-assertion-subjects.png)

**Representation of assertion subjects as named graphs.** In SEE structured, queryable representations of assertion subjects are provided as named graphs. A) The structured representation of the subject of an assertion can be accessed as the RDF graph identified by the IRI of the `rdo:proposition` instance related by the _`rdo:asserts`_ property to the `rdo:assertion` instance representing the assertion. B) Structured representation of the subject of assertion A10 asserting that the particular assay performed by Tate et al. (:assay-1) was a γ-GHS assay (:gamma\_ghs\_assay). C) TriG representation of the graph shown in B.

---


## Labelling `assertion` and `proposition` instances ##

Labels of `proposition` instances are derived from the labels of the resources used in its associated graph representation and the type of axiom involved. For restrictions, subclass axioms and type declarations the corresponding keywords of the [Manchester OWL Syntax](http://www.w3.org/TR/2012/NOTE-owl2-manchester-syntax-20121211) are used.

`Proposition` instances whose graph representation is derived from formalizing a statement of the form "some A related to some B" i.e. which consists of the instantiation of a class `(A and` _`related_to`_ `some B)` are alternatively labelled as "some A _related\_to_ some B".

`Assertion` instance labels are specified on the basis of the labels of corresponding `proposition` instances (linked via _`rdo:asserts)`_ and agents (linked via _`rdo:is_assertion_made_by`_). If "P" is the proposition label and "A" is the agent label, the assertion is labelled as "! P ! A". Multiple propositions are concatenated by " AND ". Multiple agents are separated by a space symbol.

The **rationale** of this nomenclature is that it allows to **quickly understand what is asserted** and **who asserts**, maintains a **clear connection between assertion and proposition**, maintains a **connection to the formal representation of the assertion subject** and singles out assertions as being labelled with a leading exclamation mark.