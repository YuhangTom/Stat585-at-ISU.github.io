---
author: "Zirou Zhou"
title: "plyr vs Babe Ruth"
layout: post
topic: "03"
short-topic: Split-Apply-Combine Paradigm
due-date: 2022-02-10
root: ../../
output: github_document
---

```r
library(renv)
renv::init()
```

```
## Error: init aborted
```

## Prompt:

The `plyr` package has by now been replaced by other, even faster packages, but the idea of *Split, apply, combine* is as relevant as ever.

Read the paper [The Split-Apply-Combine Strategy for Data Analysis](https://www.jstatsoft.org/article/view/v040i01) by Hadley Wickham.


Write a blog post addressing the following questions: 

1. **The R code for the split-apply-combine paper is posted with the paper. Pick one of the examples demonstrating `plyr` functionality (such as dlply or ddply, ...) and rewrite the example using functionality from the package `dplyr`. Make sure that your example actually works.**


```r
library("plyr")
baberuth <- subset(baseball, id == "ruthba01")
baberuth <- transform(baberuth, cyear = year - min(year) + 1)
baseball <- ddply(baseball, .(id), transform, 
  cyear = year - min(year) + 1)
baseball <- subset(baseball, ab >= 25)

model <- function(df) {
  lm(rbi / ab ~ cyear, data=df)
}
model(baberuth)
```

```
## 
## Call:
## lm(formula = rbi/ab ~ cyear, data = df)
## 
## Coefficients:
## (Intercept)        cyear  
##     0.20797      0.00332
```

```r
bmodels <- dlply(baseball, .(id), model)
```
Can be rewrite as

```r
library(dplyr)

bmodels3 <- lapply(baseball%>%group_split(id), model)
```


2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

The *split()* and *lapply()/sapply()* are support for the split-apply-combine strategy. 

They are not sufficient. Based on the exaple from *plyr* package, the lapply dealing with split data list will remove the id infromtion when apply to the model.

3. **In 50 to 100 words describe the split-apply-combine paradigm.**
 
First and foremost, we must choose which category will be used to separate the dataframe. We may split the original dataframe into a list by using the method *split()*. The list will then be applied to the target functions, such as *mean(), *sum()*, and *str()*, using the *lapply()/sapply()* functions, which are abbreviations for *list-apply* and *summary-apply*, respectively. After the apply procedure, these functions can realize the combine feature.

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)



