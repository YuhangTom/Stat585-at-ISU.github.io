---
author: "Gabrielle Collins"
title: "Plyr vs Dplyr functionality"
layout: post
topic: "03"
short-topic: Split-Apply-Combine Paradigm
due-date: 2022-02-10
root: ../../
output: github_document
---

## Prompt:

The `plyr` package has by now been replaced by other, even faster packages, but the idea of *Split, apply, combine* is as relevant as ever.

Read the paper [The Split-Apply-Combine Strategy for Data Analysis](https://www.jstatsoft.org/article/view/v040i01) by Hadley Wickham.


Write a blog post addressing the following questions: 

1. **The R code for the split-apply-combine paper is posted with the paper. Pick one of the examples demonstrating `plyr` functionality (such as dlply or ddply, ...) and rewrite the example using functionality from the package `dplyr`. Make sure that your example actually works.**

```r
library(renv)
library(plyr)
library(dplyr)
```

```r
renv::init()
```

```
## Error: init aborted
```
 
 ```r
 # plyr code in paper
 baseball <- ddply(baseball, .(id), transform, 
                  cyear = year - min(year) + 1)
 
 
 # dplyr code
 baseball1 <- baseball %>%
  group_by(id) %>%
  mutate(cyear = year - min(year) + 1)
 ```

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 
Functions in base R that support this strategy are 'split()', 'apply()', 'rbind()' and 'cbind()'. I don't think these are sufficient and hardly ever use them in my own work because they are limited by the type of data they can work with, and usually result in messy, unneccassary code compared to using 'dplyr' commands. Based on my own experience, the majority of code written using the split-apply-combine strategy in base R can be written much more quickly and efficiently using 'dplyr' functionality. 
3. **In 50 to 100 words describe the split-apply-combine paradigm.**
 The split-apply-combine paradigm is the process of first breaking your data into smaller groups or subsets, based on some known difference. You then apply whatever methods or functions chosen within each subset of data, and then recombine the results in a readable way. This process is subconsciously used all the time in statistics and appears to be a focal point of many of the packages and functions created in R.

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

