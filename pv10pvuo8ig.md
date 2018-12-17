```
x <- metabolite
y <- enzyme
#fit first degree polynomial equation:
fit  <- lm(y~x)
fit2 <- lm(y~poly(x,2,raw=TRUE))
fit3 <- lm(y~poly(x,3,raw=TRUE))
fit4 <- lm(y~poly(x,4,raw=TRUE))

xx <- seq(0,100, length=100)
plot(x,y,pch=19,ylim=c(0,150))
lines(xx, predict(fit, data.frame(x=xx)), col="red")
lines(xx, predict(fit2, data.frame(x=xx)), col="green")
lines(xx, predict(fit3, data.frame(x=xx)), col="blue")
lines(xx, predict(fit4, data.frame(x=xx)), col="purple")
```