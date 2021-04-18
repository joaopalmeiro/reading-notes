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
    - "The binomial logistic regression shows that for synthetic and real data PAE is significantly associated with what charts participants select as most or least complex."
    - "For synthetic data, we find that underlying base function is significantly associated with what charts participants select as most or least complex."
    - "(...) small differences in PAE are easier to spot in charts with lower PAE than with higher PAE."
  - "Varying chart PAE affects participants' ability to perform the visual task of identifying changes in a line chart."
    - "Masking [(pause time)] is used to interrupt the perceptual processing so that user responses are due to cognitive, rather than low-level perceptual pattern matching."
    - "(...) initial chart's PAE, magnitude and sign of (...) [PAE difference], and chart type have an effect on participant's accuracy in identifying the initial chart in the gallery."
    - "(...) the sign of (...) [PAE difference] affects task accuracy. (...) participants are more accurate when the change is positive than negative. (...) As the magnitude of the PAE difference increases, the accuracy for both signs increase, however the bias also persists."
    - "(...) clear trend towards 50% accuracy (random guess) as the difference in PAE between the two charts decreases, irrespective of other conditions."
    - "(...) as the initial PAE increases (the chart is more complex), so too does the necessary change in PAE in order to accurately differentiate the charts."
    - "(...) given two charts, participants have a systematic bias towards choosing the chart with lower PAE. We do not have an explanation of why this might be, but hypothesize that it might be because the lower PAE charts appear closer to the 'shape envelope' of the initial chart, especially when viewed at a glance."
  - "Varying chart PAE affects participants' ability to perform the visual task of identifying the base function of a chart."
    - "(...) users were able to correctly identify the underlying shape of a chart with close to 100% accuracy when the PAE (x-axis) of the chart, with the added noise, is low."
    - "(...) user accuracy drops to ~70% for a PAE of 0.8, and to ~50% for a PAE of 1.2. Further, we find that answer certainty consistently decreases as the PAE increases."
  - "Reducing the amount of time participants are given to study line charts, and the PAE of a line chart 'at a glance' affects comparison accuracy on charts."
    - "Glance time (...) was significantly correlated with accuracy (...)."
- "(...) PAE could inform aspect ratio selection methods to select a ratio that takes visual complexity into account."
