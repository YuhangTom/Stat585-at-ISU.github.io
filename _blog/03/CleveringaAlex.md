---
author: "Alex Cleveringa"
title: "Blog 3"
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
library(ggplot2)
library(dplyr)
```

```
## 
## Attaching package: 'dplyr'
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

```r
baseball <- plyr::baseball
baberuth <- baseball %>%
  dplyr::filter(id == "ruthba01")

baberuth <- baberuth %>%
  dplyr::mutate(cyear = year - min(year) + 1)

baseball <- baseball %>%
  dplyr::group_by(id) %>%
  dplyr::mutate(cyear = year - min(year) + 1) %>%
  dplyr::ungroup()

qplot(cyear, rbi / ab, data = baberuth, geom = "line")
```

![center](./../figure/Blog #3-02-22-2022-10-09-17/amclever/CleveringaAlex.Rmdbaseball-1.png)

```r
baseball <- baseball %>%
  dplyr::filter(ab >= 25)

xlim <- c(min(baseball$cyear, na.rm=TRUE), 
          max(baseball$cyear, na.rm = TRUE))

ylim <- c(min(baseball$rbi / baseball$ab, na.rm = TRUE), 
          max(baseball$rbi / baseball$ab, na.rm = TRUE))

plotpattern <- function(df) {
  qplot(cyear, rbi / ab, data = df, geom = "line", 
    xlim = xlim, ylim = ylim)
}
### I don't understand what the dplyr equivalent to the d_ply 
# function of saving a pdf to an individual graph for each player.

# Trying to reorder on a smaller subset of players by decreasing 
# average rbi/ab. 
#babehank <- baseball1 %>%
#  dplyr::filter(id %in% c("ruthba01", "aaronha01")) %>%
#  dplyr::group_by(id) %>%
#  dplyr::summary(mean(rbi/ab)) %>%
#  dplyr::arrange(desc(rbi/ab)) %>%
#  dplyr::ungroup()

# Got error "Error in UseMethod("arrange") : 
#  no applicable method for 'arrange' applied to an object of class 
#"table""

#baseball1 <- baseball %>%
#  dplyr::group_by(id) %>%
#  dplyr::summary(mean(rbi/ab)) %>%
#  dplyr::arrange(desc(rbi/ab)) %>%
#  dplyr::ungroup()

# I am unable to do the next steps without this one working.
```

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**  
I'm not too familiar with many base R functions, but based on a cheat 
sheet I found, there is a sort(x) function. I thin the power of dplyr 
is that it is structured in a way that is more in line with how we 
think (do this *and then* this). I am also not aware of a function 
similar to group_by, which seems very useful for the 
split-apply-combine paradigm.

3. **In 50 to 100 words describe the split-apply-combine paradigm.**  
 The split-apply-combine paradigm is a pattern of splitting a dataset,
 applying some process on a subset of that dataset, and then putting
 it back together again. 
 This has potential uses in my research dataset because I can use this
 paradigm to remove rows with a certain name, rename them, and put
 them back in the dataset. 
 I can also split the data by a numerical range, replace numbers
 outside of the range with a number I choose as the limit, and put 
 it back together again.

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

