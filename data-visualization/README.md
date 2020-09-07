<!-- markdownlint-disable-file MD033 -->

# Data Visualization

## Table of Contents

- [Papers](#papers)
  - [`Truncating the Y-Axis: Threat or Menace?`](#p1)
  - [`Belief at first sight: Data visualization and the rationalization of seeing`](#p2)
  - [`Vega-Lite: A Grammar of Interactive Graphics`](#p3)
  - [`Width-Scale Bar Charts for Data with Large Value Range`](#p4)
  - [`Visualization in Notebook-Style Interfaces`](#p5)
  - [`Augmenting Code with In Situ Visualizations to Aid Program Understanding`](#p6)
  - [`B2: Bridging Code and Interactive Visualization in Computational Notebooks`](#p7)
- [Talks](#talks)
  - [`The Python Data Visualization Landscape in 2020`](#t1)

## Papers

The (bullet point) text enclosed in double quotation marks refers to quotes from the author(s) of the respective paper.

---

### P1

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

### P2

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

### P3

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

### P4

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

### P5

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

---

### P6

[`Augmenting Code with In Situ Visualizations to Aid Program Understanding`](http://vis.csail.mit.edu/pubs/insitu-vis-debugging) | Jane Hoffswell, Arvind Satyanarayan, Jeffrey Heer | 2018 | [Repo](https://github.com/uwdata/code-augmentation)

Friday, June 26, 2020

**Quotes, notes, and takeaways**:

- "In Situ Visualizations" as a kind of synonym for sparklines/word-scale charts (or, more specifically, "code-embedded visualizations"). In addition, these charts are interactive.
- The authors "(...) hypothesize that automatically surfacing contextually relevant information directly within a code editor can help programmers better understand runtime behavior."
- Requirements for effective in situ visualizations:
  - Comparable.
  - Salient.
  - Unobtrusive.
- The authors "(...) decompose the design space into two types of visualized data (value[, like Vega signals,] and set[, like data fields]) at two levels of detail (data and change) across two temporalities (snapshot and sequence)."
- "To represent objects in both value and set data, we perform an object simplification in which the object is represented by one of its properties [and by a different color]. We select a representative property of the object by identifying which of its properties is most commonly used within the code."
- "We found that visualizations [histograms or bar charts] with a size of about **eight pixels per bin** are easily interpretable (...) and can support interaction on the elements. Representations that push bars towards a width of **two pixels** make it harder to distinguish between bins or interact effectively."
- "We recommend the histogram as the position encoding is a more effective representation than the color encoding in the heatmap. We include the heatmap for its amenability [(adaptability)] to miniaturization (...)."
- Tick visualization vs. timeline visualization:
  - "The redundant position/color encoding [for the tick visualization/win-loss sparkline] allows the programmer to easily extract the update status at a glance while also facilitating miniaturization."
  - "The timeline visualization may be more appropriate when the variable does not have a value during states when it was not updated (e.g., the variable only exists for states when it has been newly defined)."
  - "We selected the tick visualization rather than the timeline because the tick visualization explicitly represents each state in the program runtime and may thus be more informative for novice users."
- The "Modification Indicator" works like a bar chart.
- "To reduce the obtrusiveness of the code augmentations, we designed miniaturization [underline-scale charts] for the visualizations."
- Placement:
  - "The _inline-start_ placement leverages the code indentation to place augmentations in the whitespace at the start of the line." However, "If many augmentations are on the same line, the _inline-start_ placement may increase the indentation at the start of the line."
  - "The _left-margin_ and _right-margin_ placement techniques separate the augmentations from the token by placing them in the margin of the code editor but improve comparability across augmentations."
  - "When the unobtrusiveness of the augmentations is most important, we recommend using the _expand-inline_ placement technique (...)."
  - "To better attract the programmer's attention, we recommend using the _right_ placement [(option used during the evaluation)] technique to produce a large augmentation near the source of the token."
- "The runtime state can be represented by snapshotting the [Vega] _signal_ values."
- Results:
  - "Likelihood ratio tests indicated a marginally significant effect of the visualization condition [(the one with the in situ visualizations)] on task grade (...). Participants had roughly one more "correct" (or two more "partially correct") answers in the visualization condition overall."
  - "Exploratory data analysis also indicated a strong difference in grades due to education level [(PhD vs. undergraduate students)], but with similar absolute grade improvements in the visualization condition."
  - "(...) significant effect of task order on the log time for participants to complete the task (...), with participants faster in the second task regardless of condition."
  - "(...) significant positive effect for line visualization helpfulness (...) and a marginally positive effect for histogram helpfulness (...) significant positive effect for how interpretable the value (...), indicator (...), and line (...) visualizations were, and a marginally significant positive effect for the histogram."
  - The histogram was the only one without a significant negative effect on intrusiveness.
  - "While we did see a marginally significant effect of the visualization condition on task grade, participants were generally able to answer the task questions by reviewing the code and probing the state information with the tooltip on signals and data fields."
- "(...) the in situ visualizations turned the underlying data into a physical artifact to reason over."

---

### P7

[`B2: Bridging Code and Interactive Visualization in Computational Notebooks`](http://vis.mit.edu/pubs/b2) | Yifan Wu, Joseph M. Hellerstein, Arvind Satyanarayan | 2020 | [Repo](https://github.com/ucbrise/b2)

Sunday, September 6, 2020

**Quotes, notes, and takeaways**:

- This paper is divided as follows:
  - Abstract.
  - Introduction.
  - B2 demo (_case study_ style).
  - Related work.
  - _Theoretical_ considerations.
  - System design and implementation.
  - Evaluation (first-use study with 7 participants).
  - Conclusion.
- _Computational notebook_ is a broader term for Jupyter or Observable, for example, notebooks.
- B2 is implemented as an extension for Jupyter Notebook ([nbextension](https://testnb.readthedocs.io/en/latest/examples/Notebook/Distributing%20Jupyter%20Extensions%20as%20Python%20Packages.html)).
  - The project setup is based on [ipyvega](https://github.com/vega/ipyvega).
  - It consists of two major components:
    - A Python back-end component.
    - A JavaScript front-end component.
  - Main tech stack (excluding Jupyter-related stuff):
    - Berkeley's _[datascience](https://github.com/data-8/datascience)_ Python package (for data frames).
    - Python and IPython.
    - React.
    - TypeScript.
    - Vega-Lite (it leverages Vega-Lite's _grammar of interaction_) and Vega-Embed.
    - webpack.
  - [This repo](https://github.com/jupyter-widgets/widget-cookiecutter) contains a cookiecutter template that shows what is (minimally) necessary to create a Jupyter widget.
- "Currently, although these media \[code cells and visualizations\] may be interleaved, they remain **siloed**: interactive visualizations must be manually specified as they are divorced from the analysis provenance expressed via data frames, while code cells have no access to users' interactions with visualizations (...)."
- "(...) **data queries** as a shared representation between the code and interactive visualizations."
  - "The fundamental task of data analysis involves **iterative data transformation**, and both code \[via data frame manipulations\] and interactive visualizations \[via interactive selections\] can capture this task as a _data query_."
- The charts are displayed on a dashboard located to the right of the notebook. The dashboard panel facilitates (interactive) multi-view displays (regardless of the source cell).
- "When an interaction occurs, B2 reifies \[materializes/persists\] it as a data query and generates a history log in a new code cell."
  - Interactive selections are represented by their underlying predicate definitions.
  - This log is reusable when (un)commenting/copying and pasting entries _manually_.
  - All entries except the most recent one are folded (hidden) in the cell, and to reuse them, it is necessary to first unfold them (toggle hide/show). Entries continue to be added to the same cell until the user switches to the notebook panel.
  - The user "(...) can toggle the hiding of all generated cells with the `Toggle` \[button\]."
  - "(...) the interaction history that B2 produces is expressed as a series of human-understandable API calls \[a principle of literate programming\], rather than low-level event logs."
  - "(...) to preserve the linear flow of literate computing, B2 records these interaction histories in new code cells placed **directly after the most recently executed cell**."
- Cells marked as _reactive_ (via the `%%reactive` magic command) are automatically recomputed when new interactions occur. This feature is particularly interesting to allow charts created with other libraries, for example, to also be integrated into the workflow (there is an example with [Folium](https://python-visualization.github.io/folium/)).
- "(...) computational notebooks remain useful far beyond the initial act of authoring: e.g., for auditing, reproducing, or sharing data insights."
- "As there may be several cells between successive visualizations, it is unlikely to have more than one visualization visible on screen; thus, interaction techniques become confined to operating over a single visualization at a time (...)."
- The main persona for B2 seems to be the _analyst_.
- The related work section is divided into two blocks regarding integrating code and interaction:
  - Interactions **parameterizing** code ([ipywidgets](https://github.com/jupyter-widgets/ipywidgets), for example).
  - Interactions **generating** code.
- "B2 synthesizes appropriate visualizations by tracing the data lineage expressed in code (...)."
- Important question that B2 tries to answer:
  - How to combine "(...) the highly iterative nature and two-dimensional layout of interactive visualizations with the persistence and linear layout of computational notebooks (...)"?
- B2 vs. [mage](https://dig.cmu.edu/publications/2020-mage.html):
  - "B2 targets integrating code with interactive visualizations specifically, whereas %mage looks to graphical interfaces more broadly."
  - "(...) %mage uses string templates and pattern matching to translate interactions to code (...). In contrast, B2 records interaction histories as _predicates_, a representation that is tailored to interactive visualization but is also more robust to bidirectional changes."
- The authors identify three gaps:
  - Semantic gap: this gap "(...) prevents each side \[code cells and visualizations\] from understanding the work that is happening in the other;"
  - Temporal gap: this gap "(...) allows **only** code to persist, and **only** interactions on visualizations to be transient;"
  - Layout gap: this gap occurs "(...) between the notebook's linear structure and rich coordinated multi-view visualizations."
- **Semantic gap**:
  - "(...) visualizations do not understand the work expressed in code: specifically it is blind to the lineage of transformations and derivations on a data frame. (...) an analyst must manually construct appropriate interactive visualizations from scratch even if the code that specifies the data frame **captures semantics that can automate visualization design**." Two examples:
    - "(...) when data results from a _group_ operator, it is typical to favor a _bar_ marks to produce a histogram."
    - "(...) visualizations of two derived data frames that share a common ancestor can often be usefully linked or cross-filtered."
  - "(...) every Vega-Lite selection includes a definition for a _predicate_ \[data query\] (...)."
    - Intensional predicate: it "(...) specifies a set of data points based on logical conditions that must be satisfied (...)"
    - Extensional predicate: it "(...) enumerates a set of selected data points."
- **Temporal gap**:
  - "(...) we need to enable users to make their exploratory iterations in visualization **persist** when appropriate, and make their code iteration **more transient** when appropriate."
  - To address this gap, B2 provides features to capture "(...) a snapshot of visualization (...)", to materialize "(...) interactions as a history log or a (...) data frame (...)", and to create "(...) reactive cells that automatically re-execute when new interaction occurs."
- **Layout gap**:
  - Challenges:
    - "(...) a dashboard layout breaks the formerly tight coupling between a visualization and the code cell containing its specification (...)."
    - "(...) as interactions on visualizations now occur in the dashboard rather than as part of the linear notebook layout, should code cells containing interaction histories be automatically created or manually requested? (...) where should they be placed in the linear structure of the notebook (...)?"
- "B2 provides a simple Python API to generate interactive visualizations from data frame code." It adds a method, `.vis`, that "(...) does not require any parameters to work — B2 can infer the specification for a data frame visualization using established heuristics (...)." On the other hand, the "(...) `.vis` can be controlled directly via a set of optional parameters based on Vega-Lite configuration specifications (...)":
  - "The `mark` parameter chooses among bar charts, scatter plots, and line charts;"
  - "`encoding` configures which column is the x-axis, y-axis, how they should be interpreted (ordinal, quantitative, temporal), and sorted;"
  - "`selection_type` and `selection_dimensions` configure how the selection should happen and whether the selection is the x-axis, y-axis, or both."
- The user does not need "(...) to specify any interaction logic — we _infer_ that logic through the data lineage of the queries." If two data frames derive from the same data frame, "(...) infers that they should be linked (...)", for example.
- Selections (interactions) can be accessed in three different ways:
  - Predicates: `b2.current_selection` or `b2.all_selections`.
  - Data from the current selection: `df.get_filtered_data()`.
  - Code from the current selection: `df.get_code()` (or via the `Copy Code to Clipboard` button).
- The `snapshot` button allows to _save_ "(...) an SVG representation of the state of all visible visualizations in a notebook cell and the code to derive the data for the respective visualizations in comments."
- B2 is interesting for situations where we want to repeat the same analysis, including the interactive part, for another dataset with a similar schema to the initial one.
- None of the first-use study participants "(...) used B2's functionalities to navigate from the notebook to the dashboard."
- Two participants "(...) commented that the alternative approach of mapping interactions to code hadn't crossed their minds. In other words, the first approach requires that the analyst understands how B2 let them work across the two mediums, and it seems from the results that it's not always apparent."
- It would be interesting to have a _lightweight version_ of B2 in which interactions with a chart would result in a filtered data frame in the next cell.

---

## Talks

### T1

[`The Python Data Visualization Landscape in 2020`](https://ep2020.europython.eu/talks/B5Vff6U-the-python-data-visualization-landscape-in-2020/) | Bence Arató | EuroPython 2020 | [Recording](https://youtu.be/nUd1Tm5XQQI?t=13285)

Thursday, August 13, 2020

**Notes**:

- [plotnine](https://plotnine.readthedocs.io/en/stable/) (Python + Matplotlib + ggplot2).
- [HoloViews](http://holoviews.org/). It has 3 backends available: Bokeh, Matplotlib, and Plotly.
- [hvPlot](https://hvplot.holoviz.org/). It supports different data libraries, such as pandas, [Dask](https://dask.org/), [xarray](http://xarray.pydata.org/en/stable/), among others, and works like a high-level plotting API built on top of HoloViews.
- [Pandas-Bokeh](https://github.com/PatrikHlobil/Pandas-Bokeh).
- Spotify's [Chartify](https://github.com/spotify/chartify). It is built on top of Bokeh.
- [Plotly Express](https://plotly.com/python/plotly-express/). It is Plotly's high-level API.
- It is possible to combine charts from different plotting libraries with [Panel](https://panel.holoviz.org/) ([example](https://panel.holoviz.org/gallery/demos/gapminders.html)).
