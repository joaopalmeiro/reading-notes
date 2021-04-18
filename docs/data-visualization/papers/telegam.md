# TeleGam: Combining Visualization and Verbalization for Interpretable Machine Learning

> **Source**: [`TeleGam: Combining Visualization and Verbalization for Interpretable Machine Learning`](https://fredhohman.com/papers/telegam) | Fred Hohman, Arjun Srinivasan, Steven Drucker | 2019 | [Repo](https://github.com/poloclub/telegam)

Sunday, October 11, 2020

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
