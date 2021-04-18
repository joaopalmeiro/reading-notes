# ViCE: Visual Counterfactual Explanations for Machine Learning Models

> **Source**: [`ViCE: Visual Counterfactual Explanations for Machine Learning Models`](https://arxiv.org/abs/2003.02428) | Oscar Gomez, Steffen Holter, Jun Yuan, Enrico Bertini | 2020 | [Repo](https://github.com/5teffen/ViCE)

Friday, October 2, 2020

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
