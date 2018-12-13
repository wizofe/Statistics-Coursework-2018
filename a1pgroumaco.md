```
nrSamples = 1000
e <- list(mode = "vector", length = nrSamples)

for (i in 1:nrSamples) {
  e[[i]] <- rnorm(n = 20, mean = 10, sd = 5)
}

sample_mean <- matrix(NA, 1000, 1)

for (i in 1:1000) {
  sample_mean[i] <- mean(e[[i]])
}

```