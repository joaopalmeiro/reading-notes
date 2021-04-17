# Augmenting Code with In Situ Visualizations to Aid Program Understanding

> **Source**: [`Augmenting Code with In Situ Visualizations to Aid Program Understanding`](http://vis.csail.mit.edu/pubs/insitu-vis-debugging) | Jane Hoffswell, Arvind Satyanarayan, Jeffrey Heer | 2018 | [Repo](https://github.com/uwdata/code-augmentation)

Friday, June 26, 2020

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
