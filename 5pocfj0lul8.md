```
diff.medians <- median(wildtype) - median(knockout)
nboot <- 5000
n <- length(wildtype)
diff.medians.boot <- rep(0, nboot)

for (i in 1:nboot) {
  wildtype.boot <- sample(wildtype, n, replace = T)
  knockout.boot <- sample(knockout, n, replace = T)
  diff.medians.boot[i] <-
    median(wildtype.boot) - median(knockout.boot)
}

hist(diff.medians.boot,
     col = "green",
     nclass = 20,
     main = "")

title("Bootstrap distribution of difference between medians",
      cex.main = 1.0)

# Compute 95% CLT based Bootstrap confidence intervals
# for difference between medians
ci.lower.sd <- diff.medians - 1.96 * sd(diff.medians.boot)
ci.upper.sd <- diff.medians + 1.96 * sd(diff.medians.boot)
c(ci.lower.sd, ci.upper.sd)

# Compute 95% Boostrap percentile confidence intervals
# for difference between medians
ci.lower.perc <- sort(diff.medians.boot)[0.05 * nboot / 2 + 1]
ci.upper.perc <- sort(diff.medians.boot)[nboot - 0.05 * nboot / 2]
c(ci.lower.perc, ci.upper.perc)
```