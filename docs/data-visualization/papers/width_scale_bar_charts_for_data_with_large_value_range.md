# Width-Scale Bar Charts for Data with Large Value Range

> **Source**: [`Width-Scale Bar Charts for Data with Large Value Range`](https://diglib.eg.org/handle/10.2312/evs20201056) | Markus Höhn, Marcel Wunderlich, Kathrin Ballweg, Tatiana von Landesberger | 2020

Tuesday, May 26, 2020

- [Altair demo](https://nbviewer.jupyter.org/github/joaopalmeiro/datavis-python-playground/blob/7aca5548f0aa72bf82f38e12eade2118aab4c38d/altair-width-scale-bar-chart/width-scale-bar-chart-hohn-et-al.ipynb).
- "(...) width-scale bar chart \[(WSB)\] that uses width, height and color to cover a large value \[or bar height\] range within one linear scale."
- "This design is inspired by the scientific notation of numbers. (...) split each value $v$ into two parts to gain a tuple of mantissa $m$ and exponent $e$ so that $v = m \times 10^e$."
- "The mantissa is linearly mapped to the height. The exponent is mapped to both the width of the bar and the color to facilitate readability. (...) all values can be displayed with _one_ scale from 0 to 10."
- "(...) orange-yellow palette as it takes advantage of the fact that the human visual system has maximum sensitivity to luminance changes for the orange-yellow hue. (...) suitable for color blind people."
- Alternatives:
  - _Linear_ and _Logarithmic_ bar charts.
  - "_Scale-stack bar charts_ use several scales to representthe values - one scale for every distinct exponent $e$. Within each scale the mantissa $m$ is represented linearly."
  - "_Order of magnitude markers_ use different elements to visualize the mantissa $m$ and the exponent $e$. The mantissa is displayed as a thin colored bar with height of $m$ in front of a thicker gray bar represent the exponent $e$. Both elements are displayed using a linear scale from 0 to 10."
- "Because the study was online, we are not able to control the display size, the brightness and contrast but we recommended a 13” or larger computer screen to take part in the study."
- "(...) we measure error (inaccuracy) and response times."
  - _Log-Error_: $e_{log} = log(response \, value / encoded \, value)$.
  - "This _Log-Error_ is used to evaluate task _Value_ and task _Ratio_. For task _Sort_ and task _Trend_ we use a binary error with _true_ and _false_ value resulting in an accuracy \[($e = 1 - accuracy$)\] for these tasks".
- "WSB design improves the accuracy and time of value reading tasks. It has no significant difference to the best performing designs for ratio and sorting/extrema tasks and shows average performance for trend analysis \[the best is the linear design\]."
