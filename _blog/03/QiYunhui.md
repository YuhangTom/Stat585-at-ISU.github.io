---
author: "Yunhui Qi"
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

The example form the paper:


```r
library(plyr) 
```




```r
baseball <- subset(plyr::baseball, ab >= 25)
model <- function(df) {
  lm(rbi / ab ~ year, data = df)
  }
bmodels <- plyr::dlply(baseball, plyr::.(id), model)
rsq <- function(x) summary(x)$r.squared
bcoefs <-  plyr::ldply(bmodels, function(x) c(coef(x), rsquare = rsq(x)))
names(bcoefs)[2:3] <- c("intercept", "slope")
head(bcoefs)
```

```
##          id  intercept         slope     rsquare
## 1 aaronha01 -0.1053833  0.0001478121 0.000862425
## 2 abernte02  0.0000000            NA 0.000000000
## 3 adairje01  1.4798449 -0.0007118756 0.010230121
## 4 adamsba01 -2.2273596  0.0012002168 0.030184694
## 5 adamsbo03  3.8306302 -0.0019238835 0.108372596
## 6 adcocjo01 -5.1912867  0.0027382939 0.229040266
```



Rewrite of the example using dplyr::do():


```r
library(dplyr)
getfit <- function(x){
  fit=lm(rbi / ab ~ year, data = x)
  return(data.frame(intercept=coef(fit)[1],
                   slope=coef(fit)[2],
                   rsquared=summary(fit)$r.squared))
}
bcoef_do <- baseball %>% 
              group_by(id) %>%
              do(getfit(.))
head(bcoef_do)
```

```
## # A tibble: 6 × 4
## # Groups:   id [6]
##   id        intercept     slope rsquared
##   <chr>         <dbl>     <dbl>    <dbl>
## 1 aaronha01    -0.105  0.000148 0.000862
## 2 abernte02     0     NA        0       
## 3 adairje01     1.48  -0.000712 0.0102  
## 4 adamsba01    -2.23   0.00120  0.0302  
## 5 adamsbo03     3.83  -0.00192  0.108   
## 6 adcocjo01    -5.19   0.00274  0.229
```


Rewrite of the example using dplyr::summarise()


```r
bcoef_summarise <- baseball %>% 
                   group_by(id) %>%
                   summarise(intercept=coef(lm(rbi / ab ~ year))[1],
                             slope=coef(lm(rbi / ab ~ year))[2],
                             rsquared=summary(lm(rbi / ab ~ year))$r.squared)
head(bcoef_summarise)
```

```
## # A tibble: 6 × 4
##   id        intercept     slope rsquared
##   <chr>         <dbl>     <dbl>    <dbl>
## 1 aaronha01    -0.105  0.000148 0.000862
## 2 abernte02     0     NA        0       
## 3 adairje01     1.48  -0.000712 0.0102  
## 4 adamsba01    -2.23   0.00120  0.0302  
## 5 adamsbo03     3.83  -0.00192  0.108   
## 6 adcocjo01    -5.19   0.00274  0.229
```


2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 


The base R provide several functions that may be used to support the split-apply-combine strategy:

apply: apply a function to each row or column of a matrix. It will not work if your subset contains more than 1 row/column.

lapply: list version of apply

sapply: apply function to sub class(sub list, elements)

mapply: multivariate version of sapply.

tapply: apply a function to subsets of a vector.

by: apply a function to subsets of a dataframe.

I feel in most cases, base R can complete the split-apply-combine tasks. But they are not flexiable. And I think the biggest disadvantage is that these base R functions give no control on the type of output. For example, in my answer to question 1, we can also use by(), but the output will be a list instead of a data frame. We need one more step to get data frame for the following analysis.


```r
bcoef_by <- by(baseball, baseball$id, getfit)
head(bcoef_by)
```

```
## $aaronha01
##              intercept        slope    rsquared
## (Intercept) -0.1053833 0.0001478121 0.000862425
## 
## $abernte02
##             intercept slope rsquared
## (Intercept)         0    NA        0
## 
## $adairje01
##             intercept         slope   rsquared
## (Intercept)  1.479845 -0.0007118756 0.01023012
## 
## $adamsba01
##             intercept       slope   rsquared
## (Intercept)  -2.22736 0.001200217 0.03018469
## 
## $adamsbo03
##             intercept        slope  rsquared
## (Intercept)   3.83063 -0.001923883 0.1083726
## 
## $adcocjo01
##             intercept       slope  rsquared
## (Intercept) -5.191287 0.002738294 0.2290403
```

```r
mode(bcoef_by)
```

```
## [1] "list"
```





3. **In 50 to 100 words describe the split-apply-combine paradigm.**
 
The split-apply-combine strategy includes split a large data sets into subsets, apply a function to each subsets, and combine the results into one object. 

We can use the family of apply functions in base R or  functions group_by(), summarise(), do() in dplyr to fulfill this task. 

Pass the large dataset to group_by(), it will be splitted into subsets, use summarise() to apply specific functions to each subset and combine the results into one data frame.

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

