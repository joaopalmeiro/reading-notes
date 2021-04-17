# Vega-Lite: A Grammar of Interactive Graphics

> **Source**: [`Vega-Lite: A Grammar of Interactive Graphics`](http://idl.cs.washington.edu/papers/vega-lite/) | Arvind Satyanarayan, Dominik Moritz, Kanit Wongsuphasawat, Jeffrey Heer | 2017

Wednesday, May 06, 2020

- _Predicate_ (_function_) == _filter criteria_.
- "(...) grammar of graphics, providing visual encoding rules and a composition algebra for layered and multi-view displays, with a novel \[high-level\] grammar of interaction."
- "Low-level grammars (...) are useful for _explanatory_ data visualization or as a basis for customized analysis tools, as their primitives offer fine-grained control."
- "(...) for _exploratory_ visualization, higher-level grammars (...) are typically preferred as they favor conciseness over expressiveness."
- "Concise specification is achieved in part through ambiguity: users may omit details such as scale transforms (...) or color palettes, which are then filled in using a rule-based system of smart defaults."
- "_view algebra_: starting with unit specifications that define a single plot, Vega-Lite expresses composite views using operators for layering, horizontal or vertical concatenation, faceting, and parameterized repetition."
  - "Disparate views can also be combined into arbitrary dashboards, all within a unified algebraic model."
- Unit specification: "_unit := (data, transforms, mark-type, encodings)_".
- Layer specification: "_layer([unit1, unit2, ...], resolve)_".
  - "To prohibit layering of composite views with incongruent internal structures, the _layer_ operator restricts its operands to be _unit_ views."
- Concatenation specification: "_hconcat([view1, view2, ...], resolve)_" or "_vconcat([view1, view2, ...], resolve)_".
- Facet specification: "_facet(channel, data, field, view, scale, axis, resolve)_".
- Repeat specification: "_repeat(channel, values, scale, axis, view, resolve)_".
- Selection: "_selection := (name, type, predicate, domain|range, event, init, transforms, resolve)_".
  - "(...) selections can be used to drive an `if-then-else` chain of logic within an encoding channel definition."
  - "(...) Vega-Lite creates a _single_ instance of the selection that is populated and shared between all repeated instances."
