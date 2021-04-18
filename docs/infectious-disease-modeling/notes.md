# Notes

## Developing the SIR Model

> **Source**: Imperial College London's "[Developing the SIR Model](https://www.coursera.org/learn/developing-the-sir-model)" Coursera course.

- Model output: Projected future (in addition, we have to account for uncertainty).
- Three essential things to understand a disease:
  - Biology.
  - Transmission dynamics.
  - Social and behavioral factors.
- How do the relevant variables change over time? **Differential equations**.
- Carrying capacity (_K_): Maximum population size (resources are not unlimited).
- Rates are in units of inverse time (_per time_).
- The inverse of a rate gives the average duration that people spend in a specific compartment (_Infected_ or _Recovered_, for example).

### Snippets

**Example of the `ode()` function** (`deSolve` package):

```r
result <- ode(
  y = initial_state_vars,
  times = ordered_timepoints_vector,
  func = differential_equation_fn,
  parms = parameters
)
result <- as.data.frame(result)
```

**Combine `with()` and `as.list()` to access named elements directly**:

```r
# Before
logistic_fn <- function(time, state, parameters) {
  dN <- parameters["alpha"] * state["N"] * (1 - (state["N"] / parameters["K"]))

  return(list(c(dN)))
}

# After
logistic_fn <- function(time, state, parameters) {
  with(as.list(c(state, parameters)), {
    dN <- alpha * N * (1 - (N / K))

    return(list(c(dN)))
  })
}
```
