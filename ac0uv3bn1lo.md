```
# create the contingency table
t1 <- data.frame(died = c(40, 42), survived = c(47, 107))
rownames(t1)[1] <- "mutant"
rownames(t1)[2] <- "nonmutant"

# perform a chi-square test
chisq <- chisq.test(t1)
```