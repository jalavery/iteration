Iteration and List Columns
================
Jessica Lavery
10/29/2019

## Lists

``` r
l <- list(vec_numeric = 5:8,
         mat         = matrix(1:8, 2, 4),
         vec_logical = c(TRUE, FALSE),
         summary     = summary(rnorm(1000)))
```

### Accessing components of a list

``` r
l$vec_numeric
```

    ## [1] 5 6 7 8

``` r
# same result as above
l[1]
```

    ## $vec_numeric
    ## [1] 5 6 7 8

``` r
# TBD what the difference is between [] and [[]], use [[]]
l[[1]]
```

    ## [1] 5 6 7 8

``` r
# pull out specific elements
l[[1]][1:3]
```

    ## [1] 5 6 7

``` r
df <- list(
  a = rnorm(20, 3, 1),
  b = rnorm(20, 0, 5),
  c = rnorm(20, 10, .2),
  d = rnorm(20, -3, 1)
)
```
