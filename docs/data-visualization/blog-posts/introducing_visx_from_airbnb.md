# Introducing visx from Airbnb

> **Source**: [`Introducing visx from Airbnb`](https://medium.com/airbnb-engineering/introducing-visx-from-airbnb-fd6155ac4658) | Chris Williams, Harrison Shoff | 2020 | [Repo](https://github.com/airbnb/visx)

Wednesday, September 23, 2020

- visx is a "(...) collection of expressive, low-level visualization primitives for React."
- visx is formerly known as vx.
- It was rewritten in TypeScript.
- D3 + React = visx.
  - In the end, it's "(...) just React."
- _Selling points_:
  - "Keep bundle sizes down."
    - "visx is split into (...) [more than 30] packages."
  - "Un-opinionated on purpose."
    - visx can be integrated with the various options available for state management, animation, CSS-in-JS, among others.
  - "Not a charting library."
    - It is an interesting option to build a charting library through its primitives.
- Target group: Front-end developers.
- Requirements:
  - "Learnable."
    - "Ideally, engineers should be able to learn a visualization library as quickly as other frontend packages."
  - "Expressive."
    - "(...) it needs to support both simple charts (...) and highly custom visualizations for internal data products."
  - "Performant."
    - In terms of the bundle size mainly.
- Why not just use D3?
  - "(...) D3 and React both want to own DOM manipulation, we've found that it's best to only use D3 for the math and React for the DOM because two mental models for updating the DOM opens the door for bugs to sneak in."
- "(...) existing React visualization libraries are often _high-level abstractions and optimized for ease of use_ (...) _at the expense of expressivity_. None offer the expressivity of D3 primitives and many don't allow for the optimization we want in production because computation, animations, state management, styles, and rendering are all encapsulated."
- visx leverages D3 in some packages "(...) for math and layout calculations, and functionally mirror the underlying D3 package with a declarative React API (...)."
- The authors will soon add screenshot/visual regression testing with [Happo](https://happo.io/).
