
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="888" alt="Visit QuantNet">](http://quantlet.de/)

## [<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/) **SRM_fig5.5** [<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/)

```yaml

Name of Quantlet : SRM_fig5.5

Published in : SRM - Stochastische Risikomodellierung und statistische Methoden

Description : 'Produces the plots of evaluating denisities of Archimedean copulae under (size=500,
size of parameters=3, dimension=2) and (size=500, size of parameters=6, dimension=2).'

Keywords : copula, plot, time-series, archimedean, density, visualization

Author : Torsten Becker

Example : Plots from the functions for evaluating densities of Archimedean copulae.

```

![Picture1](SRM_fig5.5.png)


### R Code:
```r

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
