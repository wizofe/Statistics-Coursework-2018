```
nsampl = 1000

# e stores the randomly generated samples
e <- vector("list", nsampl)
sample_mean = rep(NA, nsampl)

for (i in 1:nsampl) {
  e[[i]] <- rnorm(n = 20, mean = 10, sd = 5)
  sample_mean[i] <- mean(e[[i]])
}
```