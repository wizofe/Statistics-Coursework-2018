```
# create the contingency table
t1 <- data.frame(died = c(40, 42), survived = c(47, 107))

cchisq.test(t1)
```