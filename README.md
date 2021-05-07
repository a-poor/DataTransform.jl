# DataTransform.jl

_created by Austin Poor_

__Under Construction__

This library is intended to help develop a standardized data-transformation schema for tabular data.

Data transformation files are defined in JSON so they are human-readable, trackable in VC, and so they can be passed between languages. `DataTransform`'s goal is to promote reproducablity and clean transformations (rather than hack-y fixes, whenever possible).

You pass in a rectangular dataset and define a stack of transformations to apply -- `DataTransform.jl` does the rest!

## Quick Start

...


## Installation

...


## DataTransform Schema Reference

Data transform files are defined in JSON.

* Select Column
  * by Name
    * Exact Match
    * Starts With
    * Ends With
    * Contains
    * RegEx
  * by Index
  * by Data Type
* Filter Rows
  * by Value
    * Exact
    * In List
    * Range
    * RegEx (for Text)
    * Apply Function to Column
* Arange Columns
  * Sort Names
  * In Specified Orders
* Arange Rows
  * Sort by Column (or Column Combinations)
* Apply Function by Column (or Row?)
  * Mapping
  * Convert Type
  * Case Function (`if/else-if/else` or `case-when`)
  * Predefined function from `FeatureEng`
* Duplicate Column
  * (Using Column Select Operations)
* Duplicate Rows
  * (Using Row Select Operations)
* Rename Column
  * Mapping
  * RegEx
* ~~Join with Other Dataset?~~

The basic schema structure is:

```json
{
  "version": "0.1", // Schema Version Number for Compatability
  "transformations": [...] // List of Transformation Objects 
}
```

Deciding how to handle errors. Set error handling globally.

Example file: [sample-transform.json](./sample-transform.json).


## API Reference

...


## Contributing

Any contribution would be greatly appreciated! You can help by suggestint additions to the package or changes you think would help. In addition, please feel free to submit an issue or PR!

Thanks!
Austin

