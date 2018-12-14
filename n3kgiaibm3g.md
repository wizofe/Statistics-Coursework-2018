```
b <- boot(data = wildtype,statistic = function(x,i) median(wildtype[i]),R = 10000)

#
```