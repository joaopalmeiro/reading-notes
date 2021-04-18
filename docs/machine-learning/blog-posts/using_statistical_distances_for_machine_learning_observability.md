# Using Statistical Distances for Machine Learning Observability

> **Source**: [`Using Statistical Distances for Machine Learning Observability`](https://towardsdatascience.com/using-statistical-distance-metrics-for-machine-learning-observability-4c874cded78) | Aparna Dhinakaran | 2020

Monday, March 29, 2021

- ML Observability.
- Statistical distances: measures to quantify the distance between two distributions.
- They can be used to check:
  - Model inputs (data or output from an upstream model):
    - Feature distribution in training vs. feature distribution in production (over a certain time window).
    - Feature distribution in production (time window A) vs. feature distribution in production (time window B).
  - Model outputs:
    - Prediction distribution in training vs. prediction distribution in production.
    - Prediction distribution in production (time window A) vs. prediction distribution in production (time window B).
    - Prediction distribution for model A vs. prediction distribution for model B (in the same time window).
  - Actuals (ground truth):
    - "In some cases, the ground truth might not be available within a short time horizon after prediction."
    - Actuals distribution in training vs. actuals distribution in production.
- The reference distribution "(...) can be a distribution across a fixed time window (distribution doesn't change) or a moving time window (distribution can change)."
- Identifying whether there has been a distribution change in a feature can also be useful to see if it can be dropped (if it is not impacting the model's performance). "While a feature distribution change should be investigated, it does not always mean that there will be a correlated performance issue."
- HERE
