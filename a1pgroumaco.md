```
# 1. Store random samples in a list
e <- vector("list", nrSamples) 
for (i in 1:nrSamples) {
  e[[i]] <- rnorm(n = 5, mean = 5, sd = 3)
}

sample_means = rep(NA, nrSamples)
for (i in 1:nrSamples){
  sample_means[i] <- mean(e[[i]])
}
```