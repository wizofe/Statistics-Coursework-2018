```
# import the boot library
library(boot)

w <-
  boot(
    data = wildtype,
    statistic = function(x, i)
      median(wildtype[i]),
    R = 10000
  )

plot(w)

# calculate the 95% confidence
boot.ci(w,
        conf = 0.95,
        type = "perc")
```