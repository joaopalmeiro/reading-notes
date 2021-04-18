# At a Glance: Pixel Approximate Entropy as a Measure of Line Chart Complexity

> **Source**: [`At a Glance: Pixel Approximate Entropy as a Measure of Line Chart Complexity`](https://arxiv.org/abs/1811.03180) | Gabriel Ryan, Abigail Mosca, Remco Chang, Eugene Wu | 2018 | [Repo](https://github.com/cudbg/pae)

Saturday, February 27, 2021

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
