```
k <-
  boot(
    data = knockout,
    statistic = function(x, i)
      median(knockout[i]),
    R = 10000
  )

plot(k)

# calculate the 95% confidence
boot.ci(k,
        conf = 0.95,
        type = c("bca"))
```