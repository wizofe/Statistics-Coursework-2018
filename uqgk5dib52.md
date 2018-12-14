```
a <-
  boot(
    data = knockout,
    statistic = function(x, i)
      median(knockout[i]),
    R = 10000
  )

# calculate the 95% confidence
boot.ci(a,
        conf = 0.95,
        type = c("norm", "basic", "perc", "bca"))
```