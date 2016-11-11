
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="888" alt="Visit QuantNet">](http://quantlet.de/)

## [<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/) **SRM_fig1.1** [<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/)

```yaml

Name of Quantlet : SRM_fig1.1

Published in : SRM - Stochastische Risikomodellierung und statistische Methoden

Description : 'Produces the curves for the binomial distribution function and the pseudoinverse
function under the probability=0.4 and the size=5.'

Keywords : plot, curve, binomial, distribution, function, visualization

Author : Viktor Sandor

Example : 'Produces the curves of binomial distribution function with the parameters size and
probability.'

```

![Picture1](SRM_fig1.1.png)


### R Code:
```r

## clear history
rm(list = ls(all = TRUE))
graphics.off()

## Zeichne die verallg. Inf fuer B(5,0.4)
par(mfrow = c(1, 2))
p = 0.4
n = 5

curve(pbinom(x, n, p), from = -1, to = 6, type = "s", ylab = expression(), 
      lwd = 3, col = "black")
title("Verteilungsfunktion")

curve(qbinom(x, n, p), from = 0, to = 1, type = "s", ylab = expression(), 
      xlab = expression(u), lwd = 3, col = "black")
title("Pseudoinverse")

```
