
![http://quantnet.wiwi.hu-berlin.de/style/banner.png](http://quantnet.wiwi.hu-berlin.de/style/banner.png)

## ![qlogo](http://quantnet.wiwi.hu-berlin.de/graphics/quantlogo.png) **SRM_fig5.5**


```yaml

Name of Quantlet : SRM_fig5.5

Published in : SRM - Stochastische Risikomodellierung und statistische Methoden

Description : 'Produces the plots of evaluating denisities of Archimedean copulae under (size=500, 
size of parameters=3, dimension=2) and (size=500, size of parameters=6, dimension=2).'

Keywords : 'copula, plot, time-series, archimedean, density, visualization'

See also : 

Author : Torsten Becker

Submitted :

Example : Plots from the functions for evaluating densities of Archimedean copulae.

```


![Picture1](SRM_fig5.5.png)


```R

## clear history
rm(list = ls(all = TRUE))
graphics.off()

## install and load packages
libraries = c("QRM")
lapply(libraries, function(x) if (!(x %in% installed.packages())) {
  install.packages(x)
})
lapply(libraries, library, quietly = TRUE, character.only = TRUE)

par(mfrow = c(1, 2))
plot(rcopula.clayton(500, 3, 2), pch = 19, ann = F, cex = 0.6, cex.axis = 0.6)
plot(rcopula.frank(500, 6, 2), pch = 19, ann = F, cex = 0.6, cex.axis = 0.6)

```
