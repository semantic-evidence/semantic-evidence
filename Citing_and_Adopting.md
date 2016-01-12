# SEE design pattern: Representing the acceptance of other agents' findings #

For example, an agent, CB, could upon evaluation of the claims made by Tate et al. conclude for _himself_ that GS was indeed isolated from rat liver.

This is represented as an `rdo:assertion` instance in its own right (A30, labelled '! some GS-enzyme isolated from some rat liver ! CB') - see figures below. It is linked to the corresponding proposition via _`rdo:asserts`_ and the assertions made by Tate et al. via _`is_directly_inferred_from`_.

In SEE there are two semantically different patterns to make this connection. In pattern 1 assertion A30 is linked to assertion A2 (Figure A). In pattern 2 (Figure B) A30 is linked to a new composite assertion that involves two more curator assertions (A31, A32) and A4 as a representation of terminological domain knowledge. A31 and A32 are linked by _`rdo:is_directly_inferred_from`_ to composite assertions reflecting factual descriptions of data and procedures given in Tate 1972.

**There is a subtle, yet important difference in meaning between these two representations:**

In **pattern 1**, exemplified in figure A, CB's conclusion is based on Tate et al.'s assertion on the same subject, i.e., it is based on the author statement itself and does not necessarily imply an affirmation of how Tate et al. reached their conclusion.

In **pattern 2**, exemplified in figure B, the CB's inference is based on factual descriptions in Tate 1972, i.e., it affirms the conclusions of Tate et al. as own conclusions on the basis of the reported experimental results.

![http://semantic-evidence.googlecode.com/svn/wiki/images/figure-7-acceptance-author-statement.png](http://semantic-evidence.googlecode.com/svn/wiki/images/figure-7-acceptance-author-statement.png)

**Figure A: Representation of acceptance: inference from author statement.** The pattern to represent inference from author statement is illustrated here by linking curator assertion A30 (shown in bold) to assertion A2 of the Tate et al. argumentation signifying inference of A30 on the basis of an author statement of Tate et al. on the same subject.

---


![http://semantic-evidence.googlecode.com/svn/wiki/images/figure-8-acceptance-by-evaluation.png](http://semantic-evidence.googlecode.com/svn/wiki/images/figure-8-acceptance-by-evaluation.png)

**Figure B: Representation of acceptance: inference from evaluating experimental evidence.** The pattern to represent inference from evaluation of the reported experimental evidence, in contrast to inference based on author statement (Figure A), is illustrated here by linking curator assertion A30 to a new composite assertion involving curator assertions A31 and A32. These are, in turn, linked to the composite assertions A9-A12 and A15-A20, respectively. These composite assertions reflect data and procedures reported in Tate 1972. Taken together this graph therefore represents a curator conclusion (A30) based on the affirmative outcome (A31, A32) of the evaluation of the data and procedures reported in Tate 1972. Note that A2, the principal conclusion of Tate et al. is unrelated to the new composite assertion. Curator assertions and their links to the Tate et al. argumentation are shown in bold.

---



## Representation of citations ##

Claims made in scientific reports which reiterate previous findings are represented using the same design pattern: as assertions on the same subject made by the respective agents.

The reiterating claim is represented as an `rdo:assertion` instance which is linked to the source assertions by _`rdo:is_directly_inferred_from`_ and linked to the same `rdo:proposition` instance as the source assertions by _`rdo:asserts`_. Each assertion can be linked to its corresponding agents and reports.

![http://semantic-evidence.googlecode.com/svn/wiki/images/figure-3-reiterating-assertion.png](http://semantic-evidence.googlecode.com/svn/wiki/images/figure-3-reiterating-assertion.png)

The fact that Meisters assertion (A1) reiterates what Tate & co-workers have asserted on the isolation of GS from rat liver (A2), is represented by a relation of the former to the latter via _`rdo:is_directly_inferred_from`_ and by sharing the same proposition instance via _`rdo:asserts`_. Each assertion is linked to its corresponding agents and reports.

---
