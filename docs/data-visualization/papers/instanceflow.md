# InstanceFlow: Visualizing the Evolution of Classifier Confusion on the Instance Level

> **Source**: [`InstanceFlow: Visualizing the Evolution of Classifier Confusion on the Instance Level`](https://arxiv.org/abs/2007.11353) | Michael Pühringer, Andreas Hinterreiter, Marc Streit | 2020 | [Repo](https://github.com/puehringer/InstanceFlow)

Sunday, December 13, 2020

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
