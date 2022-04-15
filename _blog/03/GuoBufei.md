---
author: "Bufei Guo"
title: "Split-Apply-Combine paper example demostrating"
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

I use the code in Baseball case study to demonstrate `plyr` functions.
First calculate "career year" for every player, the number of years since the player started playing, by applying `R` base function *transform* to each *id* using `plyr` function *ddply*

```r
install.packages("plyr",repos = "http://cran.us.r-project.org")
```

```
## Error in install.packages : Updating loaded packages
```

```r
baseball <- plyr::ddply(plyr::baseball, plyr::.(id), transform, cyear = year - min(year) + 1)
```

Restrict the data to focus on records with number of times at bat, **ab** greater than 25, then fit a linear model to each player and then exploring the results. First define the linear regression function and store it in `model`. Then apply `model` function to each player using function `dlply`. Finally extract the results from OLS and store it in *bcoefs*.

```r
baseball <- subset(baseball, ab>=25)
model <- function(df){
  lm(rbi/ab~cyear, data=df)
}
bmodels <- plyr::dlply(baseball, plyr::.(id), model)
rsq <- function(x) summary(x)$r.squared
bcoefs <- plyr::ldply(bmodels, function(x) c(coef(x), rsquare = rsq(x)))
names(bcoefs)[2:3] <- c("intercept", "slope")
head(bcoefs)
```

```
##          id  intercept         slope     rsquare
## 1 aaronha01 0.18329371  0.0001478121 0.000862425
## 2 abernte02 0.00000000            NA 0.000000000
## 3 adairje01 0.08670449 -0.0007118756 0.010230121
## 4 adamsba01 0.05905337  0.0012002168 0.030184694
## 5 adamsbo03 0.08867684 -0.0019238835 0.108372596
## 6 adcocjo01 0.14564821  0.0027382939 0.229040266
```

###### `dplyr` substitution
I use `dplyr` function filter to select all **ab** greater than 25 and arrange the dataset by **id** in ascending order. Then group it by **id** and calculate career year for each player. The output is stored in *baseball2*.


```r
renv::init()
```

```
## Error: init aborted
```

```r
install.packages("dplyr",repos = "http://cran.us.r-project.org")
library(dplyr)
```


```r
dat <- plyr::baseball
baseball2 <- dat%>%filter(ab>=25)%>%arrange(id)%>% group_by(id)%>%mutate(cyear= year - min(year) + 1)
```

I use *group_map* function in `dplyr` to run linear regression for each id. The results of OLS is stored in *bmodels2*, which is a list of lists with each elements being output of *lm* function. `R` base function *lapply* and *do.call* are used to extract OLS coefficients and cofficient of determinant from *bmodels2*.

```r
bmodels2 <- baseball2 %>% group_map(~model(.x))
bcoefs2 <- lapply(bmodels, function(x) t(c(coef(x), rsq(x))))
bcoefs2 <-  do.call(rbind, lapply(bcoefs2, data.frame))
colnames(bcoefs2) <- c("intercept", "slope", "rsquare")
head(bcoefs2)
```

```
##            intercept         slope     rsquare
## aaronha01 0.18329371  0.0001478121 0.000862425
## abernte02 0.00000000            NA 0.000000000
## adairje01 0.08670449 -0.0007118756 0.010230121
## adamsba01 0.05905337  0.0012002168 0.030184694
## adamsbo03 0.08867684 -0.0019238835 0.108372596
## adcocjo01 0.14564821  0.0027382939 0.229040266
```

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

The "apply" functions, i.e. *apply*,*lapply* and *mapply*. They take vectors or lists as input and operate on each part of the input elements. Also there are functions that could be used together/separately to perform split-apply-combine strategy, like *split* and *Reduce*. The former one splits data into groups and the later one collapses elements of the input. They might not be sufficient when dealing with more complex data sets or under circumstances when someone want both easy-written code and well-formated output. For example, if I am going to perform linear regression on dataset baseball using base functions, I need to first split the data set by *id*. Creating the new variable *cyear* might not be easy in this case, one option is to use `lapply(dat, function(x) x$cyear=x$year-min(x$year)+1)` to first calculate the *cyear*, where *dat* is baseball data split by *id*, and add the new variable *cyear* to split dataset using *cbind*. Then I can perfomr OLS on each element of the split list. Only use base functions requires a lot more efforts and how to operate on more complex datasets are not so obvious only using base functions.

3. **In 50 to 100 words describe the split-apply-combine paradigm.**
 
split-apply-combine break up a big problem into managable pieces, operate on each piece independently and put all the pieces back together. This strategy split the problem by seizing the similarities between problems. It provides a replacement for loops for a large set of practical problems.

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

