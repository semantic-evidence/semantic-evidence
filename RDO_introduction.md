## Reasoning and Discourse Ontology (RDO) ##
RDO provides **a lightweight OWL-vocabulary** for representing scientific claims, their subjects (i.e. what the claims are about), the argumentative relations between claims and claim provenance.

RDO is the **backbone of the SEE approach** for representing scientific evidence.

The **current version** of RDO is available [here](http://semantic-evidence.googlecode.com/svn/trunk/ontology/rdo.owl).

The **typical scenario** that underlies the constructs defined in RDO is the following: Agents (e.g., individual scientists) make claims on particular occasions (e.g., as authors of a published scientific article) about a subject of inquiry. The subject of the claim - i.e. what is claimed - is communicated in some linguistic form, often as part of a more comprehensive report (e.g., a scientific article) authored by the agents. Claims are usually justified by other claims the subject of which has been accepted as true, usually on the basis of yet other claims.

## The RDO core model ##
RDO rests on the **distinction of a claim, its subject and the linguistic form in which this subject is communicated** and is centered around the concept of an assertion: instances of the class `rdo:assertion` (`courier` typeface denotes OWL classes, _`courier in italics`_ denotes OWL properties) represent particular claims made by particular agents on a particular occasion that a particular proposition, the subject of the claim, is true.

**Propositions**, in our model, are represented by the class `rdo:proposition` and taken to represent the semantic content of contextualized lexical entities formulated in some natural or artificial language.

The **lexical entities** by which the subject of a claim and propositions and reports in general are formulated are represented using the class `rdo:text`.

The **class `rdo:report`** represents accounts intended to accurately describe an event or situation. Thus, scientific journal articles or database records as typical sources of assertions are examples of a `rdo:report`.

**`rdo:agent`** is used to represent individual persons, corporate bodies or information processing devices as roleplayers in the creation of reports or assertions.

RDO specifies various properties to represent the relations between instances of these classes. In particular, **argumentative structure** is captured by the property _`rdo:is_inferred_from`_ which relates an instance of assertion to another if and only if the former is, directly or indirectly, inferred from the latter (and possibly other premises).

Full, formal specification of all RDO constructs is provided in the [ontology file](http://semantic-evidence.googlecode.com/svn/trunk/ontology/rdo.owl).

![http://semantic-evidence.googlecode.com/svn/wiki/images/figure-1-rdo-core-model.png](http://semantic-evidence.googlecode.com/svn/wiki/images/figure-1-rdo-core-model.png)

**Core classes and properties in RDO.** Boxes denote labelled classes, arrows denote labelled properties, direction of arrows denotes property domains and ranges. Asterisk: property has domain and range-specific sub-properties.

---


## Example for the core model ##
Here is an example of how the relations between a particular assertion and its subject and provenance are represented using RDO:

The article itself, _Meister 1985_, is classified as instance of `rdo:report` annotated with a uniform resource locator (URL) providing its digital representation.

The second paragraph of _Meister 1985_ constitutes a `rdo:report_part`. It is expressed as the English language text as which it is written and which is represented as an instance of `rdo:text`. The original text is linked to it via the data property _`rdo:has_lexical_structure`_.

Meister's claim that glutamine synthetase was isolated from rat liver contained in this paragraph is represented by an instance of `rdo:assertion` (A1) labelled as '! some GS-enzyme isolated from some rat liver ! AM' to indicate the assertion subject in a concise, human readable manner (formalization of assertion subjects is described [here](Representation_of_Assertion_Subjects.md)).

A1 is related to a corresponding instance of `rdo:proposition` identifying the subject of the claim, to an instance of `rdo:agent` representing Alton Meister, and to said report part by the properties _`rdo:asserts`_, _`rdo:is_assertion_made_by`_ and _`rdo:is_assertion_made_in`_, respectively.

![http://semantic-evidence.googlecode.com/svn/wiki/images/figure-2-assertion-with-provenance.png](http://semantic-evidence.googlecode.com/svn/wiki/images/figure-2-assertion-with-provenance.png)

**Representation of assertions with subject and provenance.** `rdo:assertion` instances are related to `rdo:proposition` instances representing the subject of the assertion by _`rdo:asserts`_, to the agents making the assertion by _`rdo:is_assertion_made_by`_ and to the reports in which they are made by _`rdo:is_assertion_made_in`_. See text for additional relations among assertions, agents, reports and textual representations. Assertion and proposition labels reflect the [graph representation of assertion subjects](Representation_of_Assertion_Subjects.md). Color code of assertion and proposition labels indicates the structured representation of assertion subjects (yellow: class, blue italics: property, red: Manchester syntax restriction keyword). Circle shows the index by which the assertion is referred to in the text.

---
