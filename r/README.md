# R

## Notes

- `<-`: Assignation.
- Atomic vectors are vectors whose elements are all of the same type.
- Lists are also known as generic vectors.
- Attributes: Metadata for objects. They can be accessed using the `attributes()` function.

## Packages

- [deSolve](http://desolve.r-forge.r-project.org/): A package for differential equations.

## Snippets

**Integer vector**:

```r
v <- as.integer(c(1, 2, 3))
v <- c(1L, 2L, 3L)
```

**Selecting from a list (`[]` vs. `[[]]`)**:

```r
l <- list(4, 5, 6)
l[1] # It returns a list
l[[1]] # It returns the element itself, `4`, not a list
```
