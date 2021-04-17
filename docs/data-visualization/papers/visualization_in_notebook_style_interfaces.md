# Visualization in Notebook-Style Interfaces

> **Source**: [`Visualization in Notebook-Style Interfaces`](https://diglib.eg.org/handle/10.2312/visgap20201104) | Johanna Schmidt, Thomas Ortner | 2020

Thursday, June 11, 2020

- _Profile_ as a term for "(...) verifying the quality of the data and understanding its structure (...)".
- "(...) data science in many cases converged to stitching together several different tools in every workflow stage to achieve the intended final data analysis goal."
- Jupyter Notebook is an example of a literate/narrative programming tool.
- The authors "(...) argue for a stronger focus on notebook-style visualization techniques in visualization research which seamlessly integrate into existing literate programming environments."
  - I think a recent example would be Facebook's [HiPlot](https://facebookresearch.github.io/hiplot/), which was also adapted to work on notebooks.
- A tool like [Visplore](http://www.visplore.com/) or a dashboard has a wider layout (vertical alignment), while a tool like Jupyter Notebook has a longer layout (horizontal alignment).
- "In an iterative workflow and when trying out alternatives, notebooks better preserve the story of the previous steps (_provenance_), which can even easily be shared with others (_collaboration_)."
- "The narrative style of notebooks naturally creates a log of the complete workflow (...)".
- "The cell structure and narrative approach of notebooks allows for keeping track of the analysis steps in the workflow, something that is lost in the linked-view environment of standalone tools."
- [litvis](https://github.com/gicentre/litvis) (Markdown + Vega + [Elm](https://elm-lang.org/)).
- "Placing **Visualizations** in the **Data Workflow**": "(...) we should work on standardized data interfaces for visualization for both input and output data. Input data is defined as the data used for the visualization. Output data is defined as data created by interacting with the visualization (e.g., selections, filtering)."
  - The main idea of this point, as far as I realized, is to integrate visualizations as an auxiliary tool during the data preparation stage, and not just as a tool to use after this stage, for example.
