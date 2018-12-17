```
hist(enzyme, probability=T, main="Histogram of enzyme", col="purple")
lines(density(enzyme),col=2)

hist(metabolite, probability=T, main="Histogram of enzyme", col="yellow")
lines(density(metabolite),col=2)
```