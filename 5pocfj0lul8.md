```
bootstrap_diff_median <- function(sample0,sample1){
  resample_0 <- sample(sample0,size = length(sample0),replace = TRUE)
  resample_1 <- sample(sample1,size = length(sample1),replace = TRUE)
  diff_median <- median(resample_0)-median(resample_1)
  return(diff_median)
}

bootstrap_diff_median <- function(sample0,sample1){
  resample_0 <- sample(sample0,size = length(sample0),replace = TRUE)
  resample_1 <- sample(sample1,size = length(sample1),replace = TRUE)
  diff_median <- median(resample_0)-median(resample_1)
  return(diff_median)
}
bootstrap_null_median <- function(sample0,com){
  resample_0 <- sample(sample0, size = length(sample0), replace = TRUE)
  null_median <- median(resample_0)-median(com)
  return(null_median)}

```