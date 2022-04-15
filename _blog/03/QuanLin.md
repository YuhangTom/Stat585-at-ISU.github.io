---
author: "Lin Quan"
title: "The split-apply-combine strategy"
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
if("dplyr" %in% (.packages())){
          detach("package:dplyr", unload=TRUE) 
          detach("package:plyr", unload=TRUE) 
} 
library(plyr)
library(dplyr)
```

```
## 
## Attaching package: 'dplyr'
```

```
## The following objects are masked from 'package:plyr':
## 
##     arrange, count, desc, failwith, id, mutate, rename, summarise, summarize
```

```
## The following object is masked from 'package:ggplot2':
## 
##     vars
```

```
## The following objects are masked from 'package:stats':
## 
##     filter, lag
```

```
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```
Rewriting the baseball example:


```r
## example using `ddply` in `plyr`
baseball <- plyr::ddply(baseball,.(id),transform,cyear=year-min(year)+1)

## using `group_by`and `mutate` in `dplyr`
baseball_d <- dplyr::mutate(dplyr::group_by(baseball,id),cyear=year-min(year)+1)
```


2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

For me, `split()`,`apply()`,`rbind()` and `cbind()` can support the split-apply-combine strategy. `split()` is used to divide data into the pieces. `apply()` (`lapply()`,`mapply()`,etc) are the apply functions. `rbind()` and `cbind()` are used to combine the pieces into a single data. 

In my opinion, these are not sufficient. They can accomplish the basic task, but we need more efforts when using these functions. When we face the same problem, we need to use three or more functions together. Each function has its own limitation. The code will be much more complicated. For example, when using `rbind()` in a data frame, we need to match column numbers and names. It will increases the length of the code. 

3. **In 50 to 100 words describe the split-apply-combine paradigm.**
 
The split-apply-combine is an excellent strategy for solving the problem. First, we split the big data into pieces. we extract a subset of the data for which it is easy to solve the problem. Then, we use functions to solve each part of the problem. The operation on each piece is independent. At last, these pieces are joined back together again.
 
Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

