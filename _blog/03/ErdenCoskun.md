---
author: "Coskun Erden"
title: "Split-Apply-Combine"
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
library(plyr)
library(dplyr)
```



```r
data(baseball)

# Code from the paper:
baseball <- plyr::ddply(baseball, .(id), transform, cyear = year - min(year) + 1)

head(baseball, 5)
```

```
##          id year stint team lg   g  ab   r   h X2b X3b hr rbi sb cs bb so ibb hbp sh sf
## 1 aaronha01 1954     1  ML1 NL 122 468  58 131  27   6 13  69  2  2 28 39  NA   3  6  4
## 2 aaronha01 1955     1  ML1 NL 153 602 105 189  37   9 27 106  3  1 49 61   5   3  7  4
## 3 aaronha01 1956     1  ML1 NL 153 609 106 200  34  14 26  92  2  4 37 54   6   2  5  7
## 4 aaronha01 1957     1  ML1 NL 151 615 118 198  27   6 44 132  1  1 57 58  15   0  0  3
## 5 aaronha01 1958     1  ML1 NL 153 601 109 196  34   4 30  95  4  1 59 49  16   1  0  3
##   gidp cyear
## 1   13     1
## 2   20     2
## 3   21     3
## 4   13     4
## 5   21     5
```

```r
# Corresponding code by using dplyr functionality:
baseball <- baseball %>% group_by(id) %>% mutate(cyear = year - min(year)+1)

head(baseball, 5)
```

```
## # A tibble: 5 × 23
## # Groups:   id [1]
##   id        year stint team  lg        g    ab     r     h   X2b   X3b    hr   rbi    sb
##   <chr>    <int> <int> <chr> <chr> <int> <int> <int> <int> <int> <int> <int> <int> <int>
## 1 aaronha…  1954     1 ML1   NL      122   468    58   131    27     6    13    69     2
## 2 aaronha…  1955     1 ML1   NL      153   602   105   189    37     9    27   106     3
## 3 aaronha…  1956     1 ML1   NL      153   609   106   200    34    14    26    92     2
## 4 aaronha…  1957     1 ML1   NL      151   615   118   198    27     6    44   132     1
## 5 aaronha…  1958     1 ML1   NL      153   601   109   196    34     4    30    95     4
## # … with 9 more variables: cs <int>, bb <int>, so <int>, ibb <int>, hbp <int>,
## #   sh <int>, sf <int>, gidp <int>, cyear <dbl>
```


2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 
I know apply, lapply, tapply, mapply, rbind, cbind, and split base R functions that can be used for implementing split-apply-combine strategy. However, I do not think these functions are sufficient. I use dplyr functions when I use split-apply-combine strategy. Group_by, filter, and select  functions are very helpful for splitting a data frame and functions such as left_join, right_join, inner_join etc. are very useful for for merging two data frames.  

3. **In 50 to 100 words describe the split-apply-combine paradigm.**

Split-apply-combine is a data-analysis strategy that works well for tasks with large scale datasets. In this strategy, we break down a large data collection into manageable chunks (Split) by using relevant functions. Then we implement a function to each component (Apply) that we created in the previous step. In the third step, we reassemble these components (Combine).


 

