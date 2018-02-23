## Data Grid Libraries
#### A Comparison of Leading Tools and Utilities

---

### What do we know?

* FOS needs a _scalable_ data grid solution that provides _rich functionality_, _usability_, and _adaptability_

---

### What do we not know?

* Does NT have mandates and restrictions over open source libraries?

* How should we weigh short-term benefits against long-term costs?

* Is NT willing to pay (potentially) for commercial licensing?

---

### Objective

* Present research on the available tooling we have found 

* Provide a high-level cost-benefit analysis of those tools

* Begin a discussion around potential and/or known risks

---

### Comparison 

| Library           | Time | Customize | Risk   | Perf    | Cost  |
| ----------------- | ---- | --------- | ------ | ------- | ----- |
| react-virtualized |  8   |  8        | 3      |  8      | Free  |
| ag-grid           |  5   |  4        | 9      |  4      | $$$$  |
| react-datasheet   |  6   |  7        | 5      |  6      | Free  |
| native canvas     | 10   | 10        | ?      | 10      | Free  |

---

### [react-virtualized](https://bvaughn.github.io/react-virtualized/#/components/List)

Pros: 
* Best performance short of the canvas approach. 
* Most flexible solution. 
* Usable with other tools.

Cons: 
* Everything built from scratch or integrated with another library.
* Some learning curve.

+++

In an internal call with another ACN FED, he _strongly_ recommended react-virtualized. 

He ran into substantial issues after starting with 'simpler' solutions and later uncovering new unsupported requirements. The end result was maintaining 4 different grid solutions, each with their own feature sets and their own dependencies. 

If they had started with react-virtualized, the total effort required would be much lower.

--- 

### [ag-grid](https://www.ag-grid.com/)

Pros:
* Has a huge list of supported features, including nearly every feature we need
* Has a two month [free trial](https://www.ag-grid.com/start-trial.php)
* Enterprise version is still open source (only for reference)

+++

Cons:

* Probably very expensive if we need an [OEM license](https://www.ag-grid.com/license-pricing)
* Might have some limitations with 'tweaking' it.
* Locks us in to a very specific tool
* Licensing limited to the agreed upon use case. Potential legal issues.

---

### [react-datasheet](https://nadbm.github.io/react-datasheet/)

Pros:
* Selecting included
* Excel like keyboard shortcuts included
* "easy" to get started 

Cons:
* No sorting, grouping, filtering out of the box

---

### Native Canvas

Pros:
* No limitations
* This is what Google Sheets uses

Cons:
* Incredibly expensive to develop
* Every single thing will need to be built _completely_ from scratch.
* Large amount of "reinventing the wheel"

---

### Recommendation

*react-virtualized*

blah blah reasons