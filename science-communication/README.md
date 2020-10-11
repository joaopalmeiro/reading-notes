# Science Communication

## Table of Contents

- [Blog Posts](#blog-posts)
  - [`Case Study: The First Image of a Black Hole`](#bp1)
- [Papers/Articles](#papersarticles)
  - [`Cheerleader or watchdog?`](#p1)
  - [`Communicating with Interactive Articles`](#p2)
  - [`Translating Scientific Graphics for Public Audiences`](#p3)
  - [`Ethics and Statistics: The AAA Tranche of Subprime Science`](#p4)

## Blog Posts

The (bullet point) text enclosed in double quotation marks refers to quotes from the author(s) of the respective blog post.

---

### BP1

[`Case Study: The First Image of a Black Hole`](https://numpy.org/case-studies/blackhole-image/) | NumPy (Shaloo Shalini, Ross Barnowski, Inessa Pawson) | 2020 | [Repo](https://github.com/numpy/numpy.org/blob/master/content/en/case-studies/blackhole-image.md)

Saturday, October 10, 2020

**Quotes, notes, and takeaways**:

- Challenging data processing/reduction pipeline (from petabytes to megabytes).
- "(...) EHT [(Event Horizon Telescope )] generates over 350 Terabytes worth of observed data per day, stored on high-performance helium filled hard drives."
- "The EHT collaboration met these [image reconstruction] challenges by having independent teams evaluate the data using both established and cutting-edge image reconstruction techniques to verify that the resulting images were consistent."
- "(...) the [`eht-imaging`](https://github.com/achael/eht-imaging) Python package provides tools for simulating and performing image reconstruction on VLBI data. NumPy is at the core of array data processing (...)."
- "The standard astronomical file formats and time/coordinate transformations were handled by [Astropy](https://www.astropy.org/) while Matplotlib was used in visualizing data throughout the analysis pipeline, including the generation of the final image of the black hole."
- pandas, SciPy, and Jupyter were also used.
- [PyWavelets](https://pywavelets.readthedocs.io/en/latest/).
- It is interesting to see that the collaboration _mindset_ also includes software.

---

## Papers/Articles

The (bullet point) text enclosed in double quotation marks refers to quotes from the author(s) of the respective paper/article.

---

### P1

[`Cheerleader or watchdog?`](https://www.nature.com/articles/4591033a) | _Nature_ **459**, 1033 | 2009

Tuesday, September 29, 2020

**Quotes, notes, and takeaways**:

- Focused on science journalism and the interaction between scientists and journalists.
- Science journalism as a non-opinionated science _loudspeaker_ vs. science critic.
- The article also addresses the crisis in journalism and the importance of the scientific community collaborating with the journalistic community (in terms of communication, in terms of recognition, and in terms of journalism programs, for example).
- "Many [scientists] tend to think of science journalism as a kind of public-relations service, existing purely to explain new scientific findings to the masses."
- "(...) society needs to see science scrutinized as well as regurgitated if it is to give science its trust, and journalists are an essential part of that process."
- "They [(science and journalism)] are built on the same foundation — the belief that conclusions require evidence; that the evidence should be open to everyone; and that everything is subject to question."

---

### P2

[`Communicating with Interactive Articles`](https://distill.pub/2020/communicating-with-interactive-articles/) | Fred Hohman, Matt Conlen, Jeffrey Heer, Duen Horng (Polo) Chau | 2020 | [Repo](https://github.com/distillpub/post--communicating-with-interactive-articles)

Sunday, October 4, 2020

**Quotes, notes, and takeaways**:

- Interactive articles: "Because diverse communities create interactive content, this medium goes by many different names and has not yet settled on a standardized format nor definition. (...) While these all slightly differ in their technical approach and target audience, they all largely leverage the interactivity of the modern web."
  - [Wikipedia page](https://en.wikipedia.org/wiki/Explorable_explanation) for "Explorable explanation".
- Possible domains:
  - Research dissemination:
    - Opportunity: "Remove research debt, onboard new researchers".
    - Challenge: "No clear incentive structure for researchers".
  - Journalism.
  - Education.
  - Policy and decision making:
    - Challenge: "May require greater numeracy and graphicacy in audience".
- "(...) while the technology to distribute our ideas has grown (...), the interfaces have remained largely the same."
- "The most popular publishing platforms, for example WordPress and Medium, choose to prioritize social features and ease-of-use while limiting the ability for authors to communicate using the dynamic features of the web."
- Belief elicitation (interaction technique).
- Five affordances of interactive articles:
  - "Connecting People and Data."
  - "Making Systems Playful."
  - "Prompting Self-Reflection."
    - "Letting a reader first guess about data and only showing the ground truth afterwards challenges a reader's prior beliefs and has been shown to improve their recall of information [(through a click-and-drag chart/interface, for example)]."
    - "In the case of 'You Draw It,' readers were also shown the predictions that others made, adding a social comparison element to the experience. This additional social information was not shown to necessarily be effective for improving recall."
  - "Personalizing Reading."
    - "(...) automatically modifying text and multimedia based on a reader's individual features or input (...)."
  - "Reducing Cognitive Load."
    - Details-on-demand (interaction technique).
  - The authors colored the boundaries of the boxes of each affordance with the same color used in the line under each respective title.
- "(...) an audience which finds content to be aesthetically pleasing is more likely to have a positive attitude towards it."
- "While engagement itself may not be an end goal of most research communications, the ability to influence both audience attitude and the amount of time that is spent is a useful lever to improve learning: (...) time spent (...) and emotion (...) are predictive of learning outcomes."
- "Multiple representations give multiple perspectives."
- "Scientific data which is inherently **time varying** may be shown using an animation to connect viewers more closely with the original data, as compared to seeing an abstracted static view."
- "(...) by utilizing **animation**, it became possible for the authors to design a **unit visualization** in which each data point shown represented an individual (...)."
- "Using **person-shaped glyphs** (as opposed to abstract symbols like circles or squares) has been shown **not** to produce additional empathic responses (...)."
- "[Michael] Correll argues that much of the power of visualization comes from **abstraction**, but quantization stymies [(hinders)] empathy. He instead suggests anthropomorphizing data, borrowing journalistic and rhetoric techniques to create novel designs or interventions to foster empathy in readers when viewing visualizations."
- "(...) an ongoing debate within the data journalism community has been whether articles which utilize scroll-based graphics (scrollytelling) are more effective than those which use step-based graphics (slideshows)."
  - "[McKenna et al.](https://onlinelibrary.wiley.com/doi/abs/10.1111/cgf.13195) found that their study participants largely preferred content to be displayed with a step- or scroll-based navigation as opposed to traditional static articles, but **did not** find a significant difference in engagement between the two layouts."
  - "[Zhi et al.](https://onlinelibrary.wiley.com/doi/abs/10.1111/cgf.13719) found that performance on comprehension tasks was better in slideshow layouts than in vertical scroll-based layouts."
  - "Both studies focused on people using **desktop** (rather than mobile) devices."
- "Interactive articles commonly communicate a **single idea** or concept using **multiple representations**."
- "The Multimedia Principle states that **people learn better from words and pictures** rather than words or pictures alone, as people can process information through both a visual channel and auditory channel simultaneously."
- "While testing may call to mind stressful educational experiences for many, quizzes included in web articles can be low stakes: there is no need to record the results or grade readers."
- "(...) 'personalized spatial analogies,' presenting distance measurements in regions where readers are geographically familiar with, help people more concretely understand new distance measurements within news stories."
- "In practice, the solidified standard for details-on-demand in data visualization manifests as a tooltip, typically summoned on a cursor mouseover (...)."
- "(...) text documents and other long-form textual mediums have also experimented with letting readers choose a variable level of detail to read."
  - [Example](https://parametric.press/issue-01/call-for-proposals/).
- "Details-on-demand can also be used as a method for previewing content without committing to another interaction or change of view."
- "The act of creating a successful interactive article is **closer to building a website** than writing a blog post (...)."
- "The current generation of authoring tools do not acknowledge this collaboration [between several people with different skills]."
- There's a "(...) need for improved tooling in this area, specifically around the archiving of interactive articles."
  - "Specific features should include supporting mobile-friendly adaptations of interactive graphics (...), creating content for different platforms besides just the web, and tools that allow people to create interactive content without code."
- "We were also forced to craft designs [for _The Parametric Press_] under a more realistic set of constraints (...): when creating a visualization it is **not enough** to choose the most effective visual encodings, the graphics also had to be aesthetically appealing, adhere to a house style, have minimal impact on page load time and runtime performance, be legible on both mobile and desktop devices, and not be overly burdensome to implement."
- "There is **limited empirical evaluation** of the effectiveness of interactive articles. The problem is exacerbated by the fact that large publishers are unwilling to share internal metrics, and laboratory studies may not generalize to real world reading trends."

---

### P3

[`Translating Scientific Graphics for Public Audiences`](https://c4pgv.dbvis.de/Qiao_Hullman_2018.pdf) | Xiaoli Qiao, Jessica Hullman | 2018

Sunday, October 4, 2020

**Quotes, notes, and takeaways**:

- "(...) it remains rare for many scientists to have to communicate to the public directly."
- The authors qualitatively analyzed "(...) 20 diagrams that represent journalists' redesigns of scientific graphics targeted at a general audience."
  - The authors limited their choices "(...) to graphics that were evidently derived from the original graphics."
  - The authors "(...) adopted an open-ended coding approach in which each author independently analyzed the same subset of samples. After analyzing the first subset, [the authors] (...) labeled the design strategies and created a basic taxonomy. [The authors] (...) then applied the taxonomy to the rest of [the] (...) samples, adding new labels when necessary, and resolving disagreements."
- Using bold text to identify techniques/strategies is a very good way to highlight the most important information.
- Five categories of techniques:
  - "Simplification":
    - "(...) simplify the language."
      - "(...) spell out acronyms (...)."
      - "(...) rewriting existing labels in simpler language (...)."
      - "(...) adding a description of the unit or scale (...)."
    - "(...) simplify the interpretation."
      - "(...) break the visualization into steps."
      - "Changing the measurement (...)."
      - "(...) intentionally leave out some information (...)."
      - Tricky: "(...) remove visualization of uncertainty (such as by removing error bars or descriptions of margins of error)."
    - "(...) simplification is often **not** addressed directly in more canonical examples of visualization guidance (...)."
  - "Optimizing the Visual Presentation":
    - "(...) change the colors (...)."
    - "(...) change the visual encoding (...)."
      - In one example, "(...) the researchers used a diverging color palette to show temperature from low to high, but the journalist, in the edited version, changed it to a simpler sequential color scheme (...)."
    - "(...) add a [double] visual encoding (...)."
    - "(...) add a visualization of data [(table)] (...)."
    - "(...) change orientation or ordering of parts of a figure, typically for aesthetic reasons."
  - "Adding Explanation":
    - "(...) explanation of the content (...)."
      - "(...) add title (...)."
      - "(...) provide background information or summary (...)."
    - "(...) explanation of the graph (...)."
      - "(...) add labels to part of the diagram (...)."
      - "(...) indicate how to read the graph (...) or directly interpret the pattern shown in the original graph, both typically through annotation."
  - "Making Information Relatable":
    - "(...) use more realistic illustrations."
    - "(...) add a reference to a familiar object."
    - "Adding pictorial objects purely to support recognition of some object or entity conflicts with canonical guidance like the data-ink maximization ratio (...)."
    - "(...) provide a typical case [(baseline)] for the audience to better understand the special case (...)."
  - "Miscellaneous":
    - "(...) added or changed information groupings from the original diagram."
    - "(...) add new data or information."
- "These strategies appear to be influenced by principles that run **orthogonal** to most canonical visualization design guidance, which focuses on the clarity of the encodings but does not necessarily address how to scaffold understanding through textual and graphical elements."

---

### P4

[`Ethics and Statistics: The AAA Tranche of Subprime Science`](https://stat.columbia.edu/~gelman/research/published/ChanceEthics10.pdf) | Andrew Gelman, Eric Loken | 2014

Sunday, October 11, 2020

**Quotes, notes, and takeaways**:

- One of the main roles of statistics/quantitative research is to recognize and communicate uncertainty (and variation/variance), particularly important because "(...) we have a tendency to think more categorically about things as being true or false, there or not there (...)."
- Based on the above point, statistics should not be used "(...) to overstate confidence."
- The authors use an analogy ("(...) AAA-class bonds created during the mid-2000s that led to the subprime mortgage crisis.") to talk about research, especially statistical significance and the publication/peer review (qualitative) process, to highlight some problems with these instruments (commonly considered as _seals of approval_).
- The authors also complement the article with an analogy about food safety certification.
- The (main) motivation for the article is "(...) to stress how it [(the current system)] is used as a way of laundering uncertainty, creating AAA tranches of strong claims from masses of data and analyses of varying quality."
- In this way, the authors think it is necessary "(...) to accept large levels of uncertainty and to move beyond the paradigm in which effective certainty can be obtained via statistical significance and peer review."
- Statistical significance comes from "(...) high-certainty statements selected out of the many less-reliable claims."
- "The convention is to treat published claims as true unless demonstrated otherwise."
- "The two-step process — first the achievement of statistical significance, then publication — corresponds with the movement of a scientific hypothesis from the hazy [(_nebulosa_)] zone of uncertain speculation to presumed certainty."
- Three reasons why peer review does not guarantee error filtering:
  - "(...) any paper is publishable if you try enough outlets."
  - "(...) journals select on novelty as much as correctness."
  - "(...) reviewers and publishers may be independent with respect to a specific article they review, but they are not independent in that they participate in related projects and in the broader scientific enterprise where publications are the currency for success and promotion."
- The authors "(...) believe that what many researchers (...) are more likely to defend is a general _research hypothesis_, rather than the specific empirical findings."
- "(...) selection on statistical significance induces a positive bias in the magnitude of any comparison, and the reported estimate represents just one possible comparison that could have been performed on these data."
- The authors also speak of mechanisms (mitigators) that would involve money, such as scientific prediction markets.
- "(...) scientific prediction markets could be a step forward, just because it would facilitate clear predictive statements about replications. If a researcher believes in his or her theory, even while not willing to bet his or her published quantitative finding would reappear in a replication, that's fine, but it would be good to see such a statement openly made."
- The authors "(...) think the problem is that often researchers do not admit uncertainty or variation; they think they've already made their discovery, and they think of various data-collection and data-analysis rules as technicalities that should not get in the way of science."
- "A few significant _p_-values give the illusion of a high rating to the whole set of results, and this illusion of certainty is then used to justify a discussion section devoted to the general scientific hypothesis."
- To keep in mind: "Documenting the details of research studies, including all the relevant decisions in the design and the data analysis, is important for being able to reproduce, evaluate, and replicate results."
- "(...) academic researchers may feel freer to inflate the importance of their findings because they are removed from decisionmaking."
