# SEE design pattern: Representing consecutive layers of attribution #

Consecutive layers of attribution occur **whenever a third party makes assertions on what another agent has asserted**.

For example, when a curator evaluates a scientific article and reports on the author's assertions (without necessarily affirming them).

In SEE consecutive layers of attribution are represented as **assertions the subject of which is about other assertions**. This design pattern allows for representing **arbitrary many consecutive layers of attribution**.

![http://semantic-evidence.googlecode.com/svn/wiki/images/figure-6-attribution.png](http://semantic-evidence.googlecode.com/svn/wiki/images/figure-6-attribution.png)

**Representation of consecutive layers of attribution.** CB's assertion that 'Tate and co-workers assert that assay-1 was a gamma-GHS assay in their 1972 report' is represented as an `rdo:assertion` instance linked to a `rdo:proposition` instance whose named graph representation relates the `rdo:assertion` instance A10 to the Tate 1972 report via the _`rdo:is_assertion_made_in`_ property.

---
