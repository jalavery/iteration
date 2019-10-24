Iteration
================
Jessica Lavery
10/24/2019

# First function

``` r
x = rnorm(25, mean = 5, sd = 3)
x_again = rnorm(25, mean = 6, sd = 0.3)
y <- rnorm(25, mean = 4, sd = 0.13)

# compute z-score
mean_and_sd <- function(input_x) {
  if (!is.numeric(input_x)) {
    stop("x should be numeric")
  } else if (length(input_x) < 3) {
    stop("Cannot be computed on vectors of length <3")
  }
  
  # option 1 for output: tibble
  # tibble(mean_input = mean(input_x), 
  #        sd_input = sd(input_x))
  
  # option 2 for ouptut: list
  list(mean_input = mean(input_x), 
         sd_input = sd(input_x))
}

mean_and_sd(x)
```

    ## $mean_input
    ## [1] 5.727298
    ## 
    ## $sd_input
    ## [1] 3.366795

``` r
mean_and_sd(y)
```

    ## $mean_input
    ## [1] 3.987507
    ## 
    ## $sd_input
    ## [1] 0.113983

## Multiple inputs
