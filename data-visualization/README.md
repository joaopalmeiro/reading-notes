# Data Visualization

## Table of Contents

- [Papers](#papers).

## Papers

The (bullet point) text enclosed in double quotation marks refers to quotes from the author(s) of the respective paper.

---

[`Truncating the Y-Axis: Threat or Menace?`](https://arxiv.org/abs/1907.02035) | Michael Correll, Enrico Bertini, Steven Franconeri | 2020 (v2) | [Repo](https://github.com/mcorrell/truncation)

Sunday, April 12, 2020

**Quotes, notes, and takeaways**:

- "Y-axis truncation breaks the visual conventions of bar charts, as the relative ratio of heights between two bars is no longer proportional to their difference in value (a bar that is twice as high may not represent a value that is twice as large)."
- "By contrast, when trends, rather than individual values, are important components of the intended messages, there are some cases where _not_ truncating the y-axis is perceived as deceptive."
- "designers must take into account the range and magnitude of effect sizes they wish to communicate at a per-data and per-task level."
- "The results of our first experiment show no robust difference in the impact of truncation on bar charts and line charts: truncation results in largely **qualitatively** assessed effect sizes in both types of graphs."
- "The second experiment indicates that even designs \[broken axis bar chart and gradient bar chart\] that explicitly call attention to axis breaks do not have a noticeable impact on reducing the subjectively assessed trend."
- "Surprisingly, \[the\] accurate estimation of values does not seem to counteract the visual magnification of difference."
- "Our experimental results suggest that truncating the y-axis has a consistent and significant impact on the perceived importance of effect sizes."
- "This bias is not merely a misreading of values, but seems to be connected to the visual magnification of differences."
- "Moreover, we cannot _rely_ on visual indicators of broken or truncated axes to counteract the exaggeration caused by y-axis truncation. Subjective judgments about effect size appear to be _visual_ rather than _mathematical_ or _statistical_ judgments."
- "We reject the unequivocal dichotomy of "honest" and "dishonest" charts (...)."
- Crowdsourced study via [Prolific](https://www.prolific.co/).
- The authors did not consider interactive charts, only static ones.
- The study was conducted in a "relatively context-free manner" (it was not focused on a specific domain, for example).

---

[`Belief at first sight: Data visualization and the rationalization of seeing`](https://benjamins.com/catalog/idj.25.1.04kos) | Doris Kosminsky, Jagoda Walny, Jo Vermeulen, Søren Knudsen, Wesley Willett, Sheelagh Carpendale | 2019

Sunday, April 26, 2020

**Quotes, notes, and takeaways**:

- "(...) Mercator projection causes northern countries to appear larger than they truly are."
- The authors "(...) argue that the implicit association with objectivity creates a risk that visualizations can be perceived uncritically and with a limited understanding of the influences that shaped their message, especially at first sight."
  - "(...) belief at first sight — the uncritical perception of visualizations as a sufficient representation of reality."
- Data Visualization as a mode of representation (Nelson Goodman's Theory of Symbols).
- In 2008, a streamgraph "(...) was a new and relatively unknown data representation. Ten years later, this format is included in automatic visualization generation tools such as [Rawgraphs](https://rawgraphs.io/) (...)."
- "In this way, this conventionally agreed-upon form of representing the visible world \[perspective\] comes to be understood as representing the world "as it is". However, scholars have argued over whether these drawing rules indeed portray perspective as the one "natural" or "correct" mode of representation of a scene, or if they instead reflect a convention for exhibiting three-dimensional scenes."
  - "It is now well known that the static eye assumption is an impossibility (...) Thus how can perspective truly portray reality when it is based on an impossibility?"
- "This leads to the idea of a camera as a mechanical or autonomous image production device that excludes human bias. If the reproduction of what is in front of the camera is automatic, then it is assumed to be objective."
  - "The film's bias in favor of Caucasian skin \["whiteness" bias\] was largely accepted by the public at the time, obscured by the dominant concept that science, the basis for film production, was based on reasoned decisions without racial or cultural considerations (...)."
- "A key feature of data visualization is that it involves two distinct and separable representational stages. First, a set of data represents some aspects of the world. Second, a data visualization represents the data set and thus becomes a representation of the world."
- "A long-running stream of data visualization research investigates the connection between visualizations and the human perceptual system (...) with the purpose of increasing the interpretability of the underlying data."
  - "Tufte's (...) data-ink ratio (...) has been debated as studies have shown that extraneous elements can improve the memorability of visualizations (...)."
  - "By viewing perspective and photography as modes of representation parallel to visualization, we see that the historical context in which each came to be associated with objectivity and rationalism continues in data visualization. It becomes clear that the data visualization community's discussions of representational accuracy are rooted in discussions of "correct" representations that have endured across many centuries and representational modes."
- "(...) most visualizations represent data that is already an imperfect or incomplete representation of the world."
  - Data provenance/lineage is an important concept for transparency.
- "Placing perspective, early photography, and data visualization along a historical continuum, we can see a **tendency to systematize and automate methods of producing representations**, from using rules, to machines, to algorithms."
- "What we see is intertwined with our individual and cultural experiences, which are influenced by the history of how visual media have been perceived — as a way to portray an objective reality."
  - "(...) from a cultural point of view, belief at first sight can also happen when a society in general views a medium as fundamentally objective without further critique."
- "Understanding visualization is a shared responsibility between those who create, acquire, or select data (data providers), those who create representations of data (visualization creators) and those who read or use the visualization (analysts and viewers)."
- Three points to keep in mind:
  - **Deeper visualization literacy**: "Studying and teaching the trajectories and critiques of analogous modes of representation can help creators and audiences alike gain awareness of and contextualize the changes happening in data visualization. Visualization creators can deepen their own visualization literacy by studying and considering data visualization as a part of the historical representation process".
  - **Awareness of black boxes**: "(...) many aspects of visualization can be hidden in "black boxes", from data collection and processing steps, to representation algorithms, to the reasoning behind design choices. Black boxes can be found where there is the greatest risk that viewers' understanding of the relationship between a visualization and the world will break down."
  - **Develop critical reflexivity in visualization**.
- Punch line: "(...) visualization is not about aspiring to show the most objective, neutral, and unbiased view, but rather about being aware of the context in which the data was collected, represented, framed and viewed, and the possible biases that may have influenced their portrayal."
- Similar to a position paper.
- History and Philosophy of Science (and more, like Nelson Goodman's Theory of Symbols) as a _vehicle_ for thinking about Data Visualization.
- Easy to read, _bite by bite_, until we reach the points we should take with us.
- The authors share a kind of summary of the transition of perspective and photography as representations of the world "as it is" to _just_ modes of representation.
- In a nutshell, the authors show us part of the path of perspective and photography as proxies to reflect on the supposed objectivity of Data Visualization.

---

[`Vega-Lite: A Grammar of Interactive Graphics`](http://idl.cs.washington.edu/papers/vega-lite/) | Arvind Satyanarayan, Dominik Moritz, Kanit Wongsuphasawat, Jeffrey Heer | 2017

Wednesday, May 06, 2020

**Quotes, notes, and takeaways**:

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

---

[`Width-Scale Bar Charts for Data with Large Value Range`](https://diglib.eg.org/handle/10.2312/evs20201056) | Markus Höhn, Marcel Wunderlich, Kathrin Ballweg, Tatiana von Landesberger | 2020

Tuesday, May 26, 2020

**Quotes, notes, and takeaways**:

- "(...) width-scale bar chart \[(WSB)\] that uses width, height and color to cover a large value \[or bar height\] range within one linear scale."
- "This design is inspired by the scientific notation of numbers. (...) split each value _v_ into two parts to gain a tuple of mantissa _m_ and exponent _e_ so that _v_ = _m_ × 10<sup>_e_</sup>."
- "The mantissa is linearly mapped to the height. The exponent is mapped to both the width of the bar and the color to facilitate readability. (...) all values can be displayed with _one_ scale from 0 to 10."
- "(...) orange-yellow palette as it takes advantage of the fact that the human visual system has maximum sensitivity to luminance changes for the orange-yellow hue. (...) suitable for color blind people."
- Alternatives:
  - _Linear_ and _Logarithmic_ bar charts.
  - "_Scale-stack bar charts_ use several scales to representthe values - one scale for every distinct exponent _e_. Within each scale the mantissa _m_ is represented linearly."
  - "_Order of magnitude markers_ use different elements to visualize the mantissa _m_ and the exponent _e_. The mantissa is displayed as a thin colored bar with height of _m_ in front of a thicker gray bar represent the exponent _e_. Both elements are displayed using a linear scale from 0 to 10."
- "Because the study was online, we are not able to control the display size, the brightness and contrast but we recommended a 13” or larger computer screen to take part in the study."
- "(...) we measure error (inaccuracy) and response times."
  - _Log-Error_: _e_<sub>_log_</sub> = log(_response value_ / _encoded value_).
  - "This _Log-Error_ is used to evaluate task _Value_ and task _Ratio_. For task _Sort_ and task _Trend_ we use a binary error with _true_ and _false_ value resulting in an accuracy \[(_e_ = 1 - _accuracy_)\] for these tasks".
- "WSB design improves the accuracy and time of value reading tasks. It has no significant difference to the best performing designs for ratio and sorting/extrema tasks and shows average performance for trend analysis \[the best is the linear design\]."
- [Altair demo](https://nbviewer.jupyter.org/github/joaopalmeiro/datavis-python-playground/blob/7aca5548f0aa72bf82f38e12eade2118aab4c38d/altair-width-scale-bar-chart/width-scale-bar-chart-hohn-et-al.ipynb).

---

[`Visualization in Notebook-Style Interfaces`](https://diglib.eg.org/handle/10.2312/visgap20201104) | Johanna Schmidt, Thomas Ortner | 2020

Thursday, June 11, 2020

**Quotes, notes, and takeaways**:

- _Profile_ as a term for "(...) verifying the quality of the data and understanding its structure (...)".
- "(...) data science in many cases converged to stitching together several different tools in every workflow stage to achieve the intended final data analysis goal."
- Jupyter Notebook is an example of a literate/narrative programming tool.
- The authors "(...) argue for a stronger focus on notebook-style visualization techniques in visualization research which seamlessly integrate into existing literate programming environments."
  - I think a recent example would be Facebook's [HiPlot](https://facebookresearch.github.io/hiplot/), which was also adapted to work on notebooks.
- A tool like [Visplore](http://www.visplore.com/) or a dashboard has a wider layout (vertical alignment), while a tool like Jupyter Notebook has a longer layout (horizontal alignment).
- "In an iterative workflow and when trying out alternatives, notebooks better preserve the story of the previous steps (_provenance_), which can even easily be shared with others (_collaboration_)."
- "The narrative style of notebooks naturally creates a log of the complete workflow (...)".
- "The cell structure and narrative approach of notebooks allows for keeping track of the analysis steps in the workflow, something that is lost in the linked-view environment of standalone tools."
- [litvis](https://github.com/gicentre/litvis) (Markdown + Vega + Elm).
- "Placing **Visualizations** in the **Data Workflow**": "(...) we should work on standardized data interfaces for visualization for both input and output data. Input data is defined as the data used for the visualization. Output data is defined as data created by interacting with the visualization (e.g., selections, filtering)."
  - The main idea of this point, as far as I realized, is to integrate visualizations as an auxiliary tool during the data preparation stage, and not just as a tool to use after this stage, for example.
