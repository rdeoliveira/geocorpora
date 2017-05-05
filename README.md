## Overview
This website contains 2 corpora of geographic referring expressions such as _the south-east coast of Aberdeenshire_:

* A **text-only** corpus [[xlsx]](https://github.com/rdeoliveira/metdata/raw/7173b85b4c1c59eb3c63e67554d3454e595bf97d/text-only.xlsx): Semantically annotated expressions of various languages, domains and audiences.
* A **data-and-text** corpus [[zip]](https://github.com/rdeoliveira/geocorpora/raw/master/data-and-text.zip): Semantically annotated expressions of the meteorological domain, aligned with the the GIS data representations of what the expressions refer to.

## Text only corpus
This data set is an Excel spreadsheet. It contains 671 referring expressions such as:
```
all North Negro tributaries
```
Each row contains one corpus instance (one expression) and the following annotation tags:
* **Domain**: The domain or topic of the document from which the expression originated. It can be _river_, _route_ or _weather_.
* **Audience**: The target audience of the document from which the expression originated. It can be _canoeing_, _driving_, _fishing_ or _general_.
* **Language**: The language of the document from which the expression originated. It can be _English_, _Portuguese_ or _Spanish_.
* **Country**: The country where the document was published. It can be _Brazil_, _Canada_, _Canada & USA_, _Colombia_, _UK_ or _USA_.
* **Frames of Reference**: The many semantic concepts that the expression utilizes. For example, if _north_ is in the expression, the frame of reference _Direction (DIR)_ is annotated for this expression. The full names of the frame abbreviations are given in the _legend_ tab.
* **Frame count**: The number of different semantic frames used in the expression.

The sheet also contains a _stats_ tab, showing basic statistics of frame of reference use within the corpus.

Read this article for a contextualised explanation of the data:
- Rodrigo de Oliveira, Somayajulu Sripada and Ehud Reiter (2015). _Designing an Algorithm for Generating Named Spatial References_. ENLG 2015, 127. [[pdf]](http://anthology.aclweb.org/W/W15/W15-47.pdf#page=139)

## Data-and-text corpus
This data set contains several files:
* GeoJSON: Each file represents a binary weather forecast scenario -- places are either dry or experiencing precipitation -- and it contains 1 or more geographic expressions. Each expression is semantically annotated with frames of reference and align to specific regions of the represented geography (the central region of Scotland).
* PDF: Essentially the same data as above, but for human reading.

You can view the GeoJSON files in any [LeafLet](http://leafletjs.com) based web map such as http://geojson.io/. Simply paste the contents of a file onto the designated area and the data should be plotted automatically.

The GeoJSON files use the standard GeoJSON format (as described [here](http://geojson.org/geojson-spec.html)) and have the following structure:
```
features
  feature
    geometry
      coordinates
    properties
      marker-symbol
      expression
      marker-color
      labels
full-text
```
Where:
- A _feature_ is a subregion of the region.
- Each feature has a _geometry_, which is essentially an array of lon-lat (not lat-lon!) coordinates.
- Each feature that represents a subregion for which an expression exists in the text has: 
  - A specific number (_marker-symbol_).
  - A specific colour (_marker-color_).
  - An expression in English (_expression_).
  - A set of semantic tags (_labels_).
- _full-text_ is the original text where the expression originates from.

_features_ always contains an array of coordinates representing the subregion that is not referred to in the text: _distractors_.
  
You can view the GeoJSON files in any [LeafLet](http://leafletjs.com) based web map such as http://geojson.io/. Simply paste the contents of a file onto the designated area and the data should be plotted automatically.

Read this article for a contextualised explanation of the data:
- Rodrigo de Oliveira, Somayajulu Sripada and Ehud Reiter (2016). _Absolute and Relative Properties in Geographic Referring Expressions_. The 9th International Natural Language Generation conference. 2016. [[pdf]](http://www.aclweb.org/anthology/W/W16/W16-66.pdf#page=272)
