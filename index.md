---
title       : Tooth Growth in Guinea Pigs
subtitle    : The effect of Vitamin C
author      : by weisdata
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
github: 
  user: WChen1127
  repo: slidify_toothgrowth
---

## Introduction

Like other rodents, Guinea pigs have teeth that growth continuously while gnawing on their surface. As such, Guniea pigs can keep their teeth at a relatively constant length. It is well established that Vitamin C has play a key role in the tooth growth and maintenance.

This app is used to show the effect of two different Vitamin C delivery methods on the steady-state length of teeth of Guinea pigs.

Access to my shiny app: https://weisdata.shinyapps.io/ToothGrowth/

--- 

## Groups Comparison: 
- Plots: lengths of each of the guinea pigs’ teeth at the three dose levels, conditioned on the supplement used, Orange Juice(OJ) or Ascorbic Acid(VC).


```r
library(ggplot2)
data(ToothGrowth)
qplot(dose, len, data=ToothGrowth, geom=c("point", "smooth"), method="lm", formula = y~x, color= dose, main="Length by Dose", facets = . ~ supp, xlab="Dose Level", ylab="Length")
```

<img src="assets/fig/simple-plot.png" title="plot of chunk simple-plot" alt="plot of chunk simple-plot" style="display: block; margin: auto;" />
--- 

--- 

## Comparison Results

1. The lengths of guinea pigs' teeth, on average, increased as given more doses of vitamine C, either orange juice or ascorbic acid. 
2. The guinea pigs given orange juice had, on average, longer teeth at than the guinea pigs given ascorbic acid, at the two lower dosage levels.
3. At the highest dosage level, however, there is barely any visible difference between the lengths of the teeth in the guinea pigs.




--- 

## Access
Shiny app: https://weisdata.shinyapps.io/ToothGrowth/
GitHub: https://github.com/WChen1127/slidify_toothgrowth





