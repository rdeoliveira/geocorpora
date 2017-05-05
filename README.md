## Overview
This website contains 2 corpora of geographic referring expressions such as _the south-east coast of Aberdeenshire_:

* A **text-only** corpus: Semantically annotated expressions of various languages, domains and audiences.
* A **data-and-text** corpus: Semantically annotated expressions of the meteorological domain, aligned with the the GIS data representations of what the expressions refer to.

## Text only corpus
Data: [[xlsx]](https://github.com/rdeoliveira/metdata/raw/7173b85b4c1c59eb3c63e67554d3454e595bf97d/text-only.xlsx).

This data set is an Excel spreadsheet. It contains 671 referring expressions such as:
```
all North Negro tributaries
```
Each row contains one corpus instance (one expression) and the following annotation tags:

* **Domain**: The domain or topic of the document from which the expression originated. It can be _river_, _route_ or _weather_.
* **Audience**: The target audience of the document from which the expression originated. It can be _canoeing_, _driving_, _fishing_ or _general_.
* **Language**: The lanaauge of the document from which the expression originated. It can be _English_, _Portuguese_ or _Spanish_.
* **Country**: The country where the document was published. It can be _Brazil_, _Canada_, _Canada & USA_, _Colombia_, _UK_ or _USA_.
* **Frames of Reference**: The many semantic concepts that the expression utilizes. For example, if _north_ is in the expression, the frame of reference _Direction (DIR)_ is annotated for this expression. The full names of the frame abbreviations are given in the _legend_ tab.
* **Frame count**: The number of different semantic frames used in the expression.

The sheet also contains a _stats_ tab, showing basic statistics of frame of reference use within the corpus.

This data set is mentioned in:

- Rodrigo de Oliveira, Somayajulu Sripada and Ehud Reiter (2015). _Designing an Algorithm for Generating Named Spatial References_. ENLG 2015, 127. [[pdf]](http://anthology.aclweb.org/W/W15/W15-47.pdf#page=139)

## Data-and-text corpus
Data: [[zip] (coming soon!)]().
