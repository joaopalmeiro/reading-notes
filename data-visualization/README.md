<!-- markdownlint-disable-file MD033 -->

# Data Visualization

## Table of Contents

- [Blog Posts](#blog-posts)
  - [`Introducing visx from Airbnb`](#bp1)
  - [`Announcing the W&B Machine Learning Visualization IDE`](#bp2)
  - [`The Stellar Chart: An Elegant Alternative to Radar Charts`](#bp3)
- [Papers](#papers)
  - [`Truncating the Y-Axis: Threat or Menace?`](#p1)
  - [`Belief at first sight: Data visualization and the rationalization of seeing`](#p2)
  - [`Vega-Lite: A Grammar of Interactive Graphics`](#p3)
  - [`Width-Scale Bar Charts for Data with Large Value Range`](#p4)
  - [`Visualization in Notebook-Style Interfaces`](#p5)
  - [`Augmenting Code with In Situ Visualizations to Aid Program Understanding`](#p6)
  - [`B2: Bridging Code and Interactive Visualization in Computational Notebooks`](#p7)
  - [`VaBank: Visual Analytics for Banking Transactions`](#p8)
  - [`ViCE: Visual Counterfactual Explanations for Machine Learning Models`](#p9)
  - [`TeleGam: Combining Visualization and Verbalization for Interpretable Machine Learning`](#p10)
  - [`DALEX: Explainers for Complex Predictive Models in R` (short version)](#p11)
  - [`InstanceFlow: Visualizing the Evolution of Classifier Confusion on the Instance Level`](#p12)
  - [`At a Glance: Pixel Approximate Entropy as a Measure of Line Chart Complexity`](#p13)
- [Talks](#talks)
  - [`The Python Data Visualization Landscape in 2020`](#t1)

## Blog Posts

The (bullet point) text enclosed in double quotation marks refers to quotes from the author(s) of the respective blog post.

---

### BP1

[`Introducing visx from Airbnb`](https://medium.com/airbnb-engineering/introducing-visx-from-airbnb-fd6155ac4658) | Chris Williams, Harrison Shoff | 2020 | [Repo](https://github.com/airbnb/visx)

Wednesday, September 23, 2020

**Quotes, notes, and takeaways**:

- visx is a "(...) collection of expressive, low-level visualization primitives for React."
- visx is formerly known as vx.
- It was rewritten in TypeScript.
- D3 + React = visx.
  - In the end, it's "(...) just React."
- _Selling points_:
  - "Keep bundle sizes down."
    - "visx is split into (...) [more than 30] packages."
  - "Un-opinionated on purpose."
    - visx can be integrated with the various options available for state management, animation, CSS-in-JS, among others.
  - "Not a charting library."
    - It is an interesting option to build a charting library through its primitives.
- Target group: Front-end developers.
- Requirements:
  - "Learnable."
    - "Ideally, engineers should be able to learn a visualization library as quickly as other frontend packages."
  - "Expressive."
    - "(...) it needs to support both simple charts (...) and highly custom visualizations for internal data products."
  - "Performant."
    - In terms of the bundle size mainly.
- Why not just use D3?
  - "(...) D3 and React both want to own DOM manipulation, we've found that it's best to only use D3 for the math and React for the DOM because two mental models for updating the DOM opens the door for bugs to sneak in."
- "(...) existing React visualization libraries are often _high-level abstractions and optimized for ease of use_ (...) _at the expense of expressivity_. None offer the expressivity of D3 primitives and many don't allow for the optimization we want in production because computation, animations, state management, styles, and rendering are all encapsulated."
- visx leverages D3 in some packages "(...) for math and layout calculations, and functionally mirror the underlying D3 package with a declarative React API (...)."
- The authors will soon add screenshot/visual regression testing with [Happo](https://happo.io/).

---

### BP2

[`Announcing the W&B Machine Learning Visualization IDE`](https://wandb.ai/wandb/posts/reports/Announcing-the-W-B-Machine-Learning-Visualization-IDE--VmlldzoyNjk3Nzg?s=15) | Shawn Lewis, Carey Phelps, Stacey Svetlichnaya, John Qian, Kyle Goyette, Tom Holmes | 2020

Tuesday, October 13, 2020

**Quotes, notes, and takeaways**:

- An Visualization Development Environment (VDE) powered by Vega and Vega-Lite. It "(...) lets you define Vega specs and save them for reuse, all in the context of your actual data."
- Targeted to "(...) model understanding".
- Interesting chart for backpropagation through time.
- 6 ready-to-use charts:
  - Line chart.
  - Scatterplot.
  - Bar chart.
  - Histogram.
  - ROC curve.
  - PR curve.
- "The visualizations created with this tool are _decoupled from the underlying data they display_."

---

### BP3

[`The Stellar Chart: An Elegant Alternative to Radar Charts`](https://medium.com/nightingale/the-stellar-chart-an-elegant-alternative-to-radar-charts-ae6a6931a28e) | Alexandre Morin-Chassé | 2020

Friday, January 8, 2021

**Quotes, notes, and takeaways**:

- Stellar chart, an alternative to the radar chart.
- "Data visualization's primary objective is to present statistical information in a more accessible fashion than classic number listings (i.e. tables)."
- On a radar chart, "(...) the only piece of information that is fully data-driven is the distance between each angle and the center of the radar. (...) the rest results from complex interactions between the underlying data and a subjective, editorial decision: the ordering of categories around the circle."
- "In short, radar charts contradict one of the most basic data visualization rules: don't connect categories with lines."
- An alternative name for the radial bar/column chart could be _asterisk chart_.

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

[`B2: Bridging Code and Interactive Visualization in Computational Notebooks`](http://vis.mit.edu/pubs/b2) | Yifan Wu, Joseph M. Hellerstein, Arvind Satyanarayan | 2020 | [Repo](https://github.com/ucbrise/b2), [Study Repo](https://github.com/yifanwu/midas-exp-pub)

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
  - It does not support pandas, at least for now (more information in [this issue](https://github.com/yifanwu/b2/issues/10)).
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
    - Intensional predicate: it "(...) specifies a set of data points based on logical conditions that must be satisfied (...)."
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
- In my opinion, B2 is a tool that contributes/may contribute to help to leverage the benefits of visualizing data (in a smoother way). In practice, it is sometimes easier and faster to manipulate a data frame, draw some conclusions, and proceed with the analysis — instead of creating and using a chart. This approximation of charts to data manipulation seems, at least at first glance, to invite the user to plot data, which may enhance the benefits of visualizing data coupled with the possibility of acting immediately based on what we see and select.
- [Presentation and demo](https://github.com/joaopalmeiro/b2-presentation).

---

### P8

[`VaBank: Visual Analytics for Banking Transactions`](https://conferences.computer.org/iv/pdfs/IV2020-5aDDWiHiJcr3O59ex2Ftp6/913400a336/913400a336.pdf) | Catarina Maçãs, Evgheni Polisciuc, Penousal Machado | 2020 | [Video](https://vimeo.com/444222426)

Thursday, September 17, 2020

**Quotes, notes, and takeaways**:

- Target group: fraud analysts.
- Main analysis goals/tasks identified by fraud analysts:
  - "(...) understand the temporal evolution of a set of transactions — usually grouped by an attribute, such as client ID (...)" or "(...) the comprehension of the transactions history;"
  - "(...) search for patterns and common characteristics among transactions (...)" or "the detection of the most common types of transactions [as it helps to distinguish between typical and atypical behaviors]."
- Requirements:
  - "Search by field."
  - "Distinguish amount values [(money)]."
  - "Distinguish transactions."
  - "Search common fields."
  - "Detect typical transactions. Detect the most common types of transactions can aid the analyst in the perception of unusual transactions, possibly related to fraud."
- Visualizing the output of a self-organizing map (SOM) is a way of providing "(...) a visual summary of the data topology (...)".
  - SOM: it "(...) is a method [(neural network)] for dimensionality reduction that preserves topological and metric relationships of the input data."
  - The authors use an algorithm that works with mixed data (numerical and categorical features) — Frequency neuron Mixed Self-Organizing Map (FMSOM).
  - To visualize a SOM, neurons are typically projected on a 2D grid ("(...) hexagonal grids can also be used").
  - "The most common projection is the Unified Distance Matrix (U-matrix), in which neurons are placed in a grid and the Euclidean distances between neighbouring neurons are represented through a grey scale colour palette."
  - Dissimilarity metrics (between neurons):
    - "(...) Euclidean distance for continuous values (...)."
    - "(...) measure based on probabilities for categorical features."
    - Two types ("the [final] dissimilarity [measures] (...) [are] defined as the sum of the numerical and categorical parts (...)"):
      - "(...) one for the training of the SOM [, that is, between neurons and input feature vectors] (...)": "The numerical part is calculated using Euclidean distance on normalised values. For the categorical dissimilarity measure the sum of the partial dissimilarities is calculated, i.e., the dissimilarity is measured as the probability of the reference vector not containing the category in the input vector."
      - "(...) another for the visualization [, that is, between neurons].": "For the numerical part the traditional Euclidean distance is applied `$D_n(W_i, W_j) = \sqrt{\sum_{z=1}^n (W_{iz} - W_{jz})^2}$`. For the categorical features the dissimilarity measure was defined as the Euclidean distance between the probabilities for each of the categories present in the reference vector `$D_k(W_i, W_j) = \sqrt{\sum_{z=n}^k \sum_{m=1}^r (W_{iz}\[a^m\] - W_{jz}\[a^m\])}$`."
      - Note: `$n$` is the number of continuous features, `$k$` is the number of categorical features, and `$r$` is the number of categories of the `$k_{th}$` feature.
  - Python package for SOMs: [MiniSom](https://github.com/JustGlowing/minisom).
- The proposed tool is divided into three views:
  - The _Transaction History_ view:
    - It contains (also) a matrix that divides "(...) the space in different ranges of amounts on the y-axis and temporal values on the x-axis. (...) histograms are drawn to show the total number of transactions per column and row, respectively."
    - "The transactions [(glyphs)] are then distributed by the cells of the matrix, according to their date and amount."
    - "If more than one transaction with the same characteristics (...) occur within the same cell, they are aggregated and its glyph grows in size. The placement within each cell is made through a [circle packing](https://en.wikipedia.org/wiki/Circle_packing) algorithm which starts by placing the biggest glyph in the middle of the cell and the others around it."
    - "The user can hover each glyph and see more details [(a.k.a. tooltip)] (...). If the user clicks on a glyph, these details are fixed in the canvas [(matrix)]. Then, the user can click on an attribute to highlight all transactions that share that attribute."
    - Timeline:
      - "In the bottom, we placed an interactive timeline, so the user can select and visualise different periods of time in the data (...)."
      - The time periods, that is, the time bars are defined with a hierarchical temporal aggregation algorithm. This algorithm adapts the granularity of the timeline and adjusts the size of the time bars for fixed-size timelines based on the available space and the minimum width of the bar size.
      - "The timeline is divided vertically in two parts. In the upper part, we represent the number of transactions with bars [(they also have tooltips)]. Each bar is drawn as follows: (i) its height represents the total number of transactions; (ii) the main colour of the bar is defined by a gradient between blue and orange — the more blue, the higher the number of online transactions, the more orange, the higher the number of business transactions. (...) To give more details, we represent the quantity of each transaction type with a bar placed vertically in the main bar, according to the percentage of occurrence, and coloured, according to the transaction type."
      - The strategy above looks like an adaptation of the idea of a stacked bar chart.
      - "In the bottom part of the timeline, we place a rectangle with a predefined height if one or more fraudulent transactions occur. This rectangle is coloured according to the percentage of fraudulent transactions in that specific period of time. The higher the number of fraudulent transactions, the brighter and more red the bar will be (...) If no fraud occurs, no bar is drawn."
  - The _Transactions Topology_ view:
    - Goal: "(...) represent the distribution of different types of transactions present in the data and extrapolate at a higher level the characteristics of the dataset."
    - This view has a _typical_ SOM visualization.
  - The _Transactions Relations_ view:
    - Goal: "(...) express the relations among clustered data and emphasise the most typical transaction (...)."
    - "(...) neurons and transactions are represented as nodes and are positioned within the canvas according to their dissimilarity measure: the similar two neurons are, the closer they will get."
    - However, "(...) nodes have distinct representations. The neurons are represented with the glyphs (...). For the groups of transactions we use a circular graph that represents the number of transactions by month of occurrence."
    - "We use a line to connect the nodes. These lines are coloured: (i) in red, if they connect a node representing a group of transactions and their BMU neuron; (ii) in light grey, if they connect a group of transactions and other neurons which are also similar to them, but are not their BMU; and (iii) in blue, if they connect two similar neurons."
    - "(...) only nodes which dissimilarity is below a predefined threshold have forces of attraction, creating visual clusters defined by the SOM topology."
    - "(...) gravitational force, attracting all nodes to the centre of the canvas. The higher the number of connections between nodes, the higher this gravitational force. With this, clusters more representative of the dataset will be in the centre of the canvas, and the ones representing atypical transactions in the periphery."
    - "To avoid clutter, only neurons selected as a best matching unit (BMU) in the training process of the SOM are represented (...)."
  - Note: The last two views are SOM-based projections — a matrix/grid and a force-directed graph, respectively.
- Glyphs composed of three levels of visual detail/impact are used to distinguish transactions (in the three views). Page 4 has a great figure illustrating the glyph elements.
  - First level (three characteristics):
    - "First, the analysts aim to distinguish online from business transactions. Then, it is necessary to analyse the transaction amount and whether it was considered as fraud or not."
    - Color is used to highlight the characteristics of the first visual level:
      - "(...)" different hues to the types of transaction: orange for business; blue for online."
      - "(...) saturation to represent the amount, the brighter the colour, the higher the amount."
      - "As small differences in saturation would be imperceptible, we defined three levels of saturation [(based on a threshold compared to the average amount)] to represent: low, medium, and high amounts."
    - Shapes are also used "(...) to emphasise the distinction between transaction types — a circle for online transactions, and a rectangle for business."
    - "To represent fraud, we place a red line above the main shape."
  - Second level (two characteristics):
    - "(...) inbound and outbound transactions; and new and old beneficiaries."
    - "The transactions’ shape are complemented with a set of symbols that represent the types of operation. They are divided according to the directionality of the transaction, outbound or inbound."
    - "As the new beneficiary characteristic is a binary value, we represent transactions for new beneficiaries by dividing the stroke of the main shape in two."
  - Third level (two characteristics):
    - "(...) the time characterisation of each transaction and the interface with which the transaction was made (...)."
    - "(...) we represent the year, month, and day of the week of the transaction. Each time variable is represented by a circle with different radius centred in the main shape [respectively] (...)."
    - The circles/strokes are divided into wedges. "All wedges are coloured in light grey, except the wedge that marks the transaction date, coloured in black."
    - "The day of the week has a thicker wedge, as the analysts referred to it as the most important time variable."
    - The "(...) elapsed time between the current transaction and the previous and following transactions (...)" is also represented through three levels of time distance (based on a threshold compared to the average).
    - "(...) the interface of the transaction is represented by filling the elapsed time's shape with the interface colour (...)."
- Evaluation:
  - The authors used four metrics for each task group: difficulty, certainty, accuracy, and duration.
  - "The [fraud] analysts also had some difficulty in interpreting the glyphs, which made their certainty to be slightly lower than the other groups."

---

### P9

[`ViCE: Visual Counterfactual Explanations for Machine Learning Models`](https://arxiv.org/abs/2003.02428) | Oscar Gomez, Steffen Holter, Jun Yuan, Enrico Bertini | 2020 | [Repo](https://github.com/5teffen/ViCE)

Friday, October 2, 2020

**Quotes, notes, and takeaways**:

- ViCE is an "(...) explainable machine learning visual analytics tool (...)."
- ViCE's main goal is "(...) to support understanding of individual predictions through counterfactual explanations and to provide an intuitive visual representation for them."
- ViCE is a model-agnostic, counterfactual-based tool for binary classification.
- The evaluation is carried out through a case study.
- Target group: _Client-facing_ people (not model developers, although ViCE can also be used by them).
- "(...) visualization has been increasingly used to support the understanding, debugging, verification, and refinement of machine learning models."
- "(...) [Manifold](https://github.com/uber/manifold) (...) enables the comparison of data distribution at different levels of granularity (...)."
- Requirements:
  - "Data distribution"
  - "Relevant features"
  - "Possible changes"
  - "Actionable changes — Is it possible to change only a subset of actionable features to change the model's prediction?"
- Counterfactual algorithm:
  - ViCE uses an adapted counterfactual algorithm designed for tabular continuous data (it does not handle categorical features).
  - "(...) the entire dataset is discretized by fitting a Gaussian on each of the features and splitting the values into _n_ bins such that the middle _n - 2_ capture four standard deviations from the mean, and the extreme bins capture data points beyond this."
  - It "(...) greedily moves feature values across the bins until the predicted class is changed, or until the pre-defined constraints (no more than _w_ features are changed in a single explanation and no feature value is moved across more than _l_ bins) are reached."
  - For this work, the authors chose _n_ = 10, _w_ = 5, and _l_ = 5.
  - These constraints can help to find changes that "(...) are at the same time interpretable (minimal set of features) and feasible (minimal amount of change) (...)."
- UI:
  - Percentage bar:
    - It "(...) is used to indicate the exact prediction made by the model (...)."
    - "(...) any model prediction value greater than 50% is classified as _positive_ (...)."
    - It would be useful to be able to adjust the classification threshold.
    - A diverging color scheme is used, in which the _negative_ part is associated with red/brown and the _positive_ part with green. The color scheme looks like an adaptation of the [BrBG](http://colorspace.r-forge.r-project.org/articles/hcl_palettes.html)/[brownbluegreen](https://vega.github.io/vega/docs/schemes/#brownbluegreen) color scheme.
  - Confusion category:
    - "The correctness of the prediction is also presented (...)."
    - The confusion category is represented by a colored rounded square according to the predicted label. A striped pattern is added in the background if the prediction is incorrect according to the ground truth.
  - Features:
    - "Each attribute column is also supplemented with a [frequency] density distribution visualisation. Based on the opacity of the purple background, the frequency of occurrence at that position can be analysed."
    - "By default, the tool displays the density distribution based on all the data points, however, the user has the option to map the densities based on points with _positive_ or _negative_ target values [(ground truth)] (...)."
    - "(...) changing between the general, positive, and negative density frequency distribution views gives an indication of the monotonicity of the features."
    - The specific value of a given instance, for a given feature, is marked with a number and a horizontal tick.
    - ViCE can display a maximum of 30 features at the same time.
  - Counterfactual explanations:
    - "Arrow shaped polygons are used to exhibit a single increment in the bins (...)."
    - "The current value and the suggested new level are both shown numerically for clearer reading and detail."
    - "The color of these symbols is based on the binary decision made by the model."
  - Locking:
    - "(...) a locking function is available to remove certain attributes from consideration [(like age, for example)] (...)."
  - Sorting:
    - "Toggling the sort button orders the features based on their standardized values. In this way users can quickly identify singular feature values that are considerably above or below the average for a feature."
- "In most cases, the counterfactuals are elicited in examples with prediction percentages nearer to the cutoff threshold of 50%. This is due to the fact that samples [(instances)] in which the model predicts a very high or low percentage usually cannot be flipped by implementing a few changes (...)."
- Tech stack:
  - Flask (and Python).
  - D3 (and JavaScript).

---

### P10

[`TeleGam: Combining Visualization and Verbalization for Interpretable Machine Learning`](https://fredhohman.com/papers/telegam) | Fred Hohman, Arjun Srinivasan, Steven Drucker | 2019 | [Repo](https://github.com/poloclub/telegam)

Sunday, October 11, 2020

**Quotes, notes, and takeaways**:

- TeleGam is a model-specific tool (interface) for ML Interpretability (_post hoc_) that combines (interactive) Data Visualization and (automatically generated) text.
- "(...) systems combining both visual and natural language explanations for ML models remain largely underexplored."
- TeleGam is designed for generalized additive models (GAMs) and tabular data.
  - "A GAM provides both local instance explanations similar to linear regression, but also global feature explanations which other models lack."
  - In this way, TeleGam supports global and local paradigms.
  - "GAMs are a generalization of linear models; GAMs replace linear model's slope coefficients with smooth, shape functions. In both models, the relationship between the target variable and the features is still additive (...)."
- TeleGam works for (multi-class) classification and regression problems (in terms of the model's output, it uses the value predicted by the model).
- TeleGam is a follow-up work for [Gamut](https://fredhohman.com/papers/gamut).
- The evaluation consists of a (hypothetical) case study.
- Use the Greek letter tau (`τ`) for user-defined threshold parameters (lowercase).
- Target group: Data scientists.
- "(...) textual descriptions, or verbalizations, can be a simple, yet effective way to communicate or summarize key aspects about a model, such as the overall trend in a model's predictions or comparisons between pairs of data instances."
- Verbalizations (a.k.a. explanations) are generated from textual templates and threshold-based heuristics (adjustable by the user).
- Explanation: "(...) collection of features from an interpretable domain that relate a data instance to a model's outcome."
- "(...) often at the core of explainable ML, sits an inherent trade-off between the completeness and simplicity of an explanation [(its resolution, basically)]."
- In my perspective, the authors do not take visualization as an answer _per se_ for the creation of effective and efficient interfaces, highlighting the (possibly) necessary visualization literacy and the ease of using text for certain cases:
  - "(...) depending on the complexity of the model (e.g., number of features), interpreting these visualizations [for Model Evaluation] can be difficult and may require additional expertise."
  - "(...) explanatory visualizations can also require high **graphicacy** (...) from the people that create and use them for model iteration and decision making."
  - "While visualizations are powerful tools to help people better understand ML models, they may not be sufficient, and depending on a user's background, they can also be challenging to interpret."
  - "Text is useful for providing short, approximate explanations that provide most of the necessary information to understand a prediction without the **cognitive burden of digesting a visualization**."
  - "Natural language explanations could **complement** explanatory visualizations by helping people identify or verify inferences derived from a chart, identify prediction contributions they might have missed, or emphasize differences between predictions for multiple instances."
- TeleGam "(...) support(s) both global and local paradigms, as well as offer(s) an interactive affordance [(a three-level slider)] that allows users to dynamically update the resolution of a verbalization [(all of them, to be more precise)] to tailor the level of detail desired in explanation."
- To complement the point above, the interface has a slider that the user can adjust to obtain less or more detail of the available verbalizations.
- ModelTracker and Squares are tools that leverage "(...) **unit visualizations** for interactive model debugging and performance analysis (...)."
- Verbalizations and (feature and instance-level) charts are interactively linked (details-on-demand).
- TeleGam adopts an "(...) _overview and detail strategy_ (...) for generating explanations where visualizations are used to give an overview while the verbalizations highlight specific features or trends."
- Requirements:
  - "Local instance explanations."
  - "Instance explanation comparisons."
  - "Feature importance."
  - "Counterfactuals."
- Interface:
  - **Configuration area** to select the dataset, the resolution for the verbalizations, and whether the waterfall charts should be ordered by magnitude (absolute value) or not.
  - "The **Global Model View** displays model feature-level verbalizations of GAM shape function charts that describe a feature's overall impact on model predictions."
    - In other words, "(...) the system automatically displays textual statements summarizing the major feature trends (...)."
    - "TeleGam highlights four groups of feature-level verbalizations based on the overall geometry of the shape function line charts — namely, features that have positively linear, negatively linear, non-linear, or flat geometry."
    - "To identify these groups, we used an agglomerative hierarchical clustering approach: (...) we represent the shape function line charts (...) as time series and cluster them based on their overall geometry."
    - "[Hovering] (...) over sentences displays a tooltip (...) showing the GAM shape function line charts [(in Vega-Lite)] that present an overview of the feature values (on the x-axis) and model predictions (on the y-axis) corresponding to the features listed in the sentence."
    - "These visualizations also enable a user to ask counterfactuals (...)."
  - "The **Local Instance View** displays two [(or just one)] data instance's [(selectable from a dropdown menu)] waterfall charts [(in D3)] (...) that shows the cumulative sum of the contribution each feature has on the final prediction."
    - "Alongside are instance-level verbalizations [(and a summary highlighting the differences between the predictions and the possible features that may cause this difference, if applicable)] that, when (...) [hovered], highlight (in orange) the corresponding marks [(bars and feature names)] of the visualization that the verbalization refers to."
    - **Instance Feature Summary**:
      - "To generate this verbalization, we first compute the ratio of each (...) [feature's GAM prediction contribution] with respect to the (...) [final instance] prediction. If the ratio is greater than a predefined threshold [(0.15 or 15% in this work)] (...), then that feature is included in the verbalization."
    - **Instance Comparison Summary**:
      - "(...) we first normalize both the total predictions and the individual feature contributions for all instances to [0−1] so the comparison can be made in context of the entire dataset."
      - "Then, we check for the differences between the considered pair of normalized predictions and compare them to [two] preset thresholds [(0.25 and 0.75 in this work, respectively)] (...) to generate the verbalization [(the predictions will be similar, different, or moderately varying/similar)]."
      - "For the second half of the verbalization, a feature is considered accountable for the difference between the final predictions of two instances if for any feature (...) [the absolute difference in their normalized contributions is greater than a threshold (0.25 in this work)]."
    - The expected and predicted values are also shown for each selected instance.
    - Waterfall chart: "(...) the features are listed on the x-axis and the contribution to the prediction from each feature are represented by the height of the bars. The color of the bar indicates whether the contribution is positive (light gray) or negative (dark gray)."
    - "To enable visual comparison, TeleGam ensures the scale of the y-axis as well as the ordering of the features on the x-axis in both waterfall charts are normalized and consistent."
  - Two **accordion tabs to configure the thresholds** that parameterize the verbalizations.
- A possible idea inspired by this paper is the use of logging capabilities in computational notebooks, for example, to share possible explanations, but also to share important notes about certain aspects of the charts (different scales on the vertical axes in two charts side by side, for example), something that can be turned on and off.
- TeleGam uses the `crosshair` cursor (`cursor` CSS property) when the mouse pointer is over a verbalization (more info [here](https://developer.mozilla.org/en-US/docs/Web/CSS/cursor)). Personally, I think other valid options would be `context-menu`, `help`, `alias`, and `zoom-in`.

---

### P11

[`DALEX: Explainers for Complex Predictive Models in R` (short version)](https://jmlr.org/papers/v19/18-416.html) | Przemysław Biecek | 2018 | [Repo](https://github.com/ModelOriented/DALEX)

Saturday, October 17, 2020

**Quotes, notes, and takeaways**:

- DALEX:
  - R package.
  - Model-agnostic.
  - Single model or multiple models.

---

### P12

[`InstanceFlow: Visualizing the Evolution of Classifier Confusion on the Instance Level`](https://arxiv.org/abs/2007.11353) | Michael Pühringer, Andreas Hinterreiter, Marc Streit | 2020 | [Repo](https://github.com/puehringer/InstanceFlow)

Sunday, December 13, 2020

**Quotes, notes, and takeaways**:

- InstanceFlow is "(...) a novel dual-view visualization tool that allows users to analyze the learning behavior of classifiers over time on the instance-level \[(and class-level)\]."
- Characteristics:
  - Post-hoc model evaluation.
  - Training phase.
  - Temporal (epoch-based) performance analysis.
  - Deep Learning tool.
  - Model-agnostic tool.
  - Single model.
  - FE: React.
  - Input: JSON-based results file.
- Target group: data scientists (_model developers and builders_).
- InstanceFlow consists of two main linked components (both support different levels of granularity):
  - _Flow View_/Sankey diagram:
    - To visualize "(...) the flow of instances throughout epochs, with on-demand detailed \[(squared or rectangular)\] glyphs and traces for individual instances."
    - "In its basic form, (...) visualizes 'class changers' in a Sankey diagram. _Distribution \[Stacked\] Bar Charts_ emphasize the fraction of correctly versus incorrectly classified instances. At the finest granularity, _Instance Glyphs_ encode each individual sample, with _Instance Traces_ connecting the instances to reveal their classification history (...)."
    - X-axis: epoch.
    - Y-axis: predicted classes.
    - "The user selects classes of interest, and each class is assigned to a vertical region in the Sankey diagram. All non-selected classes are aggregated as 'Other' and also assigned to a dedicated vertical region."
    - The epochs can be selected using a slider range.
    - Tooltip when hovering.
    - "Clicking on a section of the Sankey diagram selects those instances."
    - Instance Glyphs:
      - "The color of the Instance Glyphs denotes the actual class of the instances (...)."
      - "The shape \[(as well as the sub-bars of the Distribution Bar Charts)\] indicates if the instance predictions are temporally stable, coming from a different class, leaving for a different class, or coming from and leaving for different classes."
      - Double encoding: "The horizontal positions encode the same information, with glyphs for incoming instances placed at the left, outgoing ones at the right, and stable ones at the center."
      - Double encoding: "To visually rank the instances by their 'importance', the opacity and vertical position of each glyph encode one of the calculated numerical difficulty measures (...)."
  - _Tabular View_:
    - "By default, only instances with at least one incorrect classification are shown (...)."
    - "One column shows the class predictions over time as a colored heatmap (...) using a categorical color scheme to encode the sequence of predicted classes."
    - "An additional column shows a histogram of correct, incorrect, and other predictions (...) "incorrect" refers to predictions of wrong classes from among the selected subset of classes, while 'other' refers to wrong predictions of non-selected classes."
    - "The encodings \[(chart types)\] in both of these columns can be switched between time-dependent heatmaps and summarizing histograms."
- User tasks: - Instance-focused tasks: - "Find _difficult_ \[(to classify)\] instances" - "Trace an instance's _classification history_" - "Analyze if an instance visits _many_ or _few_ classes" - "Find instances _oscillating_ between classes" - Epoch-focused tasks: - "Assess _class distributions_ for a given epoch" - "Find momentarily _wrong_ and/or _correct_ instances" - "Find instances _staying_ in their class or _moving_ between
  classes at a given epoch"
- "(...) a temporal drill-down to the instance level can help model developers to distinguish stable (mis)classification patterns from stochastic effects caused by the partially random training mechanism."
- InstanceFlow is inspired by Squares (although in Squares only the final predictions of the model can be analyzed).
- Instance-based temporal difficulty measures/metrics:
  - "Let $m$ be the total number of instances, $n$ the number of classes, and $k$ the number of selected epochs. Let $C(i)$ be the actual class of instance $i$ and $P(i, j)$ the prediction for instance $i$ in epoch $j$."
  - Misclassification score $S$ ("(...) fraction of epochs in which (...) \[an instance\] was assigned to the wrong class (...)"): $S(i) = (1/k) \sum_{j=1}^{k} [P(i, j) \neq C(i)]$ (similar to Hamming loss). "A misclassification score of 0 means the model predicted the correct class in every epoch, whereas a score of 1 means that the model never predicted the correct class."
  - Variability $V$ ("(...) ratio of how many classes were predicted for an instance across all epochs (...)"): $V(i) = (1/n) |\{P(i, j)\}_{j \in \{1, ..., k\}}|$. "A variability of $1/n$ means that the model predicted the same class in every epoch, whereas a variability of 1 means that the model predicted every possible class at least once."
  - Frequency $F$ ("(...) ratio of epoch transitions for which the model's prediction jumps between classes (...)"): $F(i) = 1/(k-1) \sum_{j=1}^{k-1} [P(i, j) \neq P(i, j+1)]$. "A frequency of 0 means that an instance always stayed in the same class, whereas a frequency of 1 means that the prediction changed after every epoch."
- The evaluation part corresponds to a usage scenario/case study.
- The sort glyph/icon for the columns in the Tabular View consists of a number for the priority, a downwards arrow, and a variable icon according to the type of variable (numeric, categorical, or string-based categorical) for the order. These glyphs, as well as the Tabular View itself, are based on the [LineUp.js](https://github.com/lineupjs/lineupjs) library (as well as [Font Awesome](https://fontawesome.com/)'s _sort_alpha\_\*_, _sort_amount\_\*_, and _sort_numeric\_\*_ icons). Some of them have the following approximate appearance:
  - $1.\downarrow_{1}^{9}$
  - $2.\downarrow_{9}^{1}$
  - $1.\downarrow_{A}^{Z}$
  - $2.\downarrow_{Z}^{A}$

---

### P13

[`At a Glance: Pixel Approximate Entropy as a Measure of Line Chart Complexity`](https://arxiv.org/abs/1811.03180) | Gabriel Ryan, Abigail Mosca, Remco Chang, Eugene Wu | 2018 | [Repo](https://github.com/cudbg/pae)

Saturday, February 27, 2021

**Quotes, notes, and takeaways**:

- Metric for (1D) line chart (visual) complexity: Pixel Approximate Entropy (PAE).
- To use this metric, first scale "(...) the dataset by mapping its values into the visual domain as positional variables, so that the x and y data values are in terms of pixels."
- The default values for the parameters are $m = 2$ (window size) and $r = 20$ (distance threshold). The authors "(...) selected these values by synthetically generating a training set of line charts with varying amounts of generated noise and found values that maximized the average PAE-to-noise level correlation across the training set."
- Characteristics:
  - "Correlated with perceived complexity".
  - "Correlated with noise-levels".
  - "Predictive of perceptual accuracy".
  - "Simple".
  - "Widely Applicable".
- "(...) visualization of larger, more complicated data, the first impression of a visualization centers on its overall shape and trend."
- "The result of the study confirms that users perceive visualizations with higher (lower) approximate entropy as more (less) complex."
- At a glance perception:
  - "Greene and Oliva found that in rapid scene categorization, people interpret a scene based on global, ecological properties that describe its spatial and functional aspects rather than by breaking it into objects (...)."
  - "(...) Biederman et al. found that a person's ability to detect an object in a scene is dependent on specific relations between the object and scene as opposed to specific characteristics of the object itself (...)."
- "(...) the classic measure of entropy is computed over an unordered set of values, and does not work for ordered visualizations."
- "Approximate entropy quantifies [(using a sliding window approach)] the unpredictability of changes in a series of points. Intuitively, a series of points with more repeated patterns is easier to predict."
- "(...) approximate entropy is estimated using a fixed $N$. (...) This is a natural fit for visualizations, where we can set $N$ to the width of the chart in pixels."
- "(...) altering the scale of a chart effects its entropy measure. Increasing the relative height of the chart will increase the entropy, while increasing the width will decrease entropy."
- "In practice PAE can be interpreted as the amount of space on the chart that is taken up by _unpredictable_ data."
- Hypotheses:
  - "There is a statistically significant correlation between PAE and the amount of noise added to the chart."
    - Yes.
  - "PAE is an effective measure of perceived complexity, such that there is a statistically significant correlation between participants' perception of complexity and the line chart's PAE."
  - "Varying chart PAE affects participants' ability to perform the visual task of identifying changes in a line chart."
  - "Varying chart PAE affects participants' ability to perform the visual task of identifying the base function of a chart."
  - "Reducing the amount of time participants are given to study line charts, and the PAE of a line chart 'at a glance' affects comparison accuracy on charts."

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
