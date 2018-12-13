```
nsampl = 1000

e <- vector("list", nsampl)
for (i in 1:nsampl) {
  e[[i]] <- rnorm(n = 20, mean = 10, sd = 5)
}

sample_means = rep(NA, nsampl)
for (i in 1:nsampl) {
  sample_means[i] <- mean(e[[i]])
}

```