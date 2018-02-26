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
| react-data-grid   |  6   |  3        | 6      |  6      | Free  |
| native canvas     | 10   | 10        | ?      | 10      | Free  |

---

### [react-virtualized](https://bvaughn.github.io/react-virtualized/#/components/List)

Pros: 
* Best performance short of the canvas approach. 
* Most flexible solution. 
* Usable with other tools.

+++

### [react-virtualized](https://bvaughn.github.io/react-virtualized/#/components/List)

Cons: 
* Everything built from scratch or integrated with another library.
* Some learning curve.

--- 

### [ag-grid](https://www.ag-grid.com/)

Pros:
* Has a huge list of supported features, including nearly every feature we need
* Has a two month [free trial](https://www.ag-grid.com/start-trial.php)
* Enterprise version is open source (for reference)

+++

### [ag-grid](https://www.ag-grid.com/)

Cons:

* Probably very expensive if we need an [OEM license](https://www.ag-grid.com/license-pricing)
* Limitations with 'tweaking' it.
* Vendor lock-in
* Licensing limited to agreed upon use case. Potential legal issues.
* Questionable React support

---

### [react-datasheet](https://nadbm.github.io/react-datasheet/)

Pros:
* Selecting included
* Excel like keyboard shortcuts included
* Easier to get started 

+++

### [react-datasheet](https://nadbm.github.io/react-datasheet/)

Cons:
* No sorting, grouping, filtering out of the box
* Outdated version of React, which means major performance limitations

---

### [react-data-grid](http://adazzle.github.io/react-data-grid/)

Pros:
* Sorting, grouping, and filtering included
* Freezing included
* Virtualized

+++

### [react-data-grid](http://adazzle.github.io/react-data-grid/)

Cons:
* Monolithic codebase
* Larger number of dependencies
* Outdated version of React, which means major performance limitations

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
