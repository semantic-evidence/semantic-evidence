# Design principles for representation of evidence #

SEE is based on **two basic design principles** for the representation of evidence:

**DP1:** Representation of evidence amounts to representation of claims and argumentative structure.

**DP2:** Evidence relations in the sense of "A is evidence for B" obtain between the things being claimed.

## Rationale for DP1 & DP2 ##
Accounts of evidence are directed towards the **justification of scientific claims**. The SEE approach is based on the notion that scientific claims put forward possible, more or less likely scenarios and outcomes - **[states of affairs](http://plato.stanford.edu/archives/sum2012/entries/states-of-affairs/)** - as being accurate descriptions of a subject of scientific inquiry.

Something is evidence for a certain state of affairs, if and only if it gives reason to believe that this state of affairs in fact obtains. A **pairing of evidence and what it is claimed to be evidence for** therefore **corresponds to the set of premises and the conclusion of an argument** in which the truth of the premises alleges to give reason to believe the conclusion is true.

### Therefore the evidence used by authors or agents to justify a claim, possibly using further unstated background assumptions, can be mirrored by an argumentative structure having the claim as its conclusion. ###

Typically, **what is used to justify** the authors conclusions within this argumentative structure **are claims in themselves** accepted as true on the basis of observations or inferences of the same or of other investigators. SEE, therefore, models evidence relations in the sense of "A is evidence for B" specifically as relations between claims.

## Representation of claim subjects ##

**A researcher's assessment of the evidence** for a finding usually includes evaluation of which materials and methods were used, what kind of data was obtained and which properties were observed, inferred or assumed to establish the finding.

Consequently, a representation of the materials, methods, data items and other elements forming the subject of a claim should be part of a computationally accessible evidence representation.

In RDF and OWL the subject of a claim, a state of affairs, must be expressed, using appropriately defined resources, as (one or more) triples and axioms, respectively.

It follows then, in accordance with DP2 that in an RDF/OWL-based representation of evidence that includes claim subjects the **representation of evidential relationships should operate between claim subject representations**, i.e. between sets of RDF-triples and/or OWL-axioms **(DP3)**.

## Representation of claim provenance ##

**DP4:** Representation of claims and hence representation of evidence must take into account claim provenance, in particular **through which source** and **by which agents** the claims were made.

Knowing which agent made the claim is crucial for **evaluating independence and reproducibility**. Tracking the **original source** of a claim provides **a natural reference point** for all subsequent representations of the claim and its supporting background and for re-evaluation of the claim within the original context in which it was communicated.

## Minimal components for representing evidence ##

We therefore identify as minimal components for modelling evidence elements representing
  1. **scientific claims** and the **argumentative structure** used to justify them by other claims
  1. the **[subjects of the claims](Representation_of_Assertion_Subjects.md)** i.e. of that _what_ is claimed with regard to a subject of inquiry
  1. the **agents** making the claims and arguments
  1. the **sources** in which claims were originally made e.g., the original scientific articles or database records.