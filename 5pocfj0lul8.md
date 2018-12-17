```
bootstrap_diff_median <- function(sample0, sample1) {
  resample0 <- sample(sample0, size = length(sample0), replace = TRUE)
  resample1 <-
    sample(sample1, size = length(sample1), replace = TRUE)
  diff_median <- median(resample0) - median(resample1)
  return(diff_median)
}

bootstrap_null_median <- function(sample0, val) {
  resample0 <-
    sample(sample0, size = length(sample0), replace = TRUE)
  null_median <- median(resample0) - median(val)
  return(null_median)
}

# calculate the average difference 
```