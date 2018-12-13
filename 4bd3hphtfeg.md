```
# load the Golub data from bioconductor
source("http://www.bioconductor.org/biocLite.R")
biocLite(c("hopach"))
library(hopach)
data(golub)

# find the row index of tc4
tc4 = grep("Ras-Like Protein Tc4", golub.gnames[, 2], 
            ignore.case = TRUE)
golubFactor <- factor(golub.cl, levels=0:1, 
labels = c("ALL","AML"))

# side by side boxplot for AML and ALL
boxplot(golub[tc4, ] ~ golubFactor, ylim = c(0,2))
```