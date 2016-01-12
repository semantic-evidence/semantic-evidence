# SEE overview #

SEE is designed for representation of the evidence that is provided to back up a scientific finding. For general background information on evidence read [this](Evidence_and_Representation_of_Evidence.md).

In SEE the evidence for a scientific claim is represented in terms of the **argumentative structure of its supporting background** by providing

(i) a formal representation of scientific claims, their provenance and the argumentative structure used to justify them by other claims

(ii) a formal [representation of the subject of a claim](Representation_of_Assertion_Subjects.md) i.e., of that _what_ is claimed with regard to a subject of inquiry and

(iii) a coherent integration of the two.

For the representation of claims, their provenance and argumentative structure SEE relies on an abstract model specified in the [Reasoning and Discourse Ontology (RDO)](RDO_introduction.md), a lightweight OWL vocabulary developed for this purpose.

Claim content e.g., _what_ is claimed regarding the properties of biological entities or the results and methods of an investigation is [represented in RDF graphs](Representation_of_Assertion_Subjects.md) by using appropriately defined semantic web resources and design patterns which as a best practice should, if possible, be re-used from existing domain ontologies.

The connection between claims as representational primitives and their content relies on [named RDF graphs](http://www.websemanticsjournal.org/index.php/ps/article/view/76) which enable pointing to collections of RDF-triples or OWL-axioms serialized as such.

[Read more](SEE_Design_Principles.md) about the underlying principles for representing evidence in SEE and how these elements were identified.

## Core design patterns ##
With SEE one can coherently represent the entire evidence trail and how it is communicated. Its design patterns enable representation of
  * [individual scientific claims along with their subject and provenance](RDO_introduction#Example_for_the_core_model.md)
  * [argumentative structures](Representing_Argumentative_Structure.md) within and across publications
  * [attribution and consecutive layers of attribution](Consecutive_Layers_Attribution.md) (e.g., citing what others have asserted)
  * the [acceptance of what others have asserted](Citing_and_Adopting.md) (e.g., a curator evaluates a scientific article and enters some of the reported findings into a database)
  * the [drawing of own conclusions](Representing_Alternative_Conclusions.md) (e.g., alternative interpretations of published data)

## Applying SEE for evaluation of scientific findings ##
SEE-based accounts can be used to evaluate the evidence which is used to justify a scientific claim w.r.t.
  * the observations and techniques used
  * the informations sources used and assumptions made
  * the sources through which the finding has been communicated
  * the agents which have made the claim

In addition, evidence-related information such as
  * all assertions which are directly or indirectly used to infer a given assertion
  * all assertions made in a given report
  * all assertions made by a given agent
  * all assertions on the same subject
  * all agents making assertions on a given subject
can easily be queried.

## Use cases ##
Representations which use SEE or its underlying model could be productive in a variety of use cases requiring careful examination or recording of evidence, e.g.,
  * providing supporting background information for biomedical knowledge bases,
  * creating digital abstracts of research publications,
  * adding a claim-level perspective on research publications which could be used by publishers, in bibliographic databases and in personal bibliography managers,
  * providing open linked data which can be integrated on an informed basis using varying, application specific evidence criteria.