```
sd_sample_mean <- function(k, m, s) {
  nsampl = 1000
  for (i in 1:nsampl) {
    e[[i]] <- rnorm(n = k, mean = m, sd = s)
  }
  
  # store the mean of the samples
  e <- vector("list", nsampl)

  sample_mean = rep(NA, nsampl)
  for (i in 1:nsampl) {
    sample_mean[i] <- mean(e[[i]])
  }
  
  return(sd(sample_mean))
}
```