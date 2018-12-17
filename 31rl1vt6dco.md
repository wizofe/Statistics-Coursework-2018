```
hist(enzyme, probability=T, main="Histogram of enzyme", col="purple")
lines(density(enzyme),col=2)

hist(enzyme, probability=T, main="Histogram of enzyme", col="yellow")
lines(density(normal),col=2)
```