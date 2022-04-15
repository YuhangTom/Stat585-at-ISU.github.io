---
author: "Kieran Liming"
title: "Split-Apply-Combine Baseball"
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

Looking at the baseball example, the plyr way of creating models for each player goes as follows:


```r
library(plyr)
library(dplyr)
```



```r
baseball.plyr<-baseball

baseball.plyr <- subset(baseball.plyr, ab >= 25)


baseball.plyr <- plyr::ddply(baseball.plyr, .(id), transform,
 cyear = year - min(year) + 1)

model <- function(df) {
 lm(rbi / ab ~ cyear, data = df)
}

bmodels <- plyr::dlply(baseball.plyr, .(id), model)
```

This creates a list of of lists--the latter being the output from the linear models for each player. This is much more streamlined under dplyr. To do the same process in dplyr (though the output will be a dataframe of lists), the following code is sufficient:


```r
bmodels.dplyr = baseball %>% 
  filter(ab >= 25) %>% 
  mutate(cyear = year - min(year) + 1) %>% 
  group_by(id) %>% 
  do(fit.dplyr = lm(rbi / ab ~ cyear, data = .))
```

We can see that this is much more compact, and in my opinion is easier to follow what is happening.

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

As mentioned in the paper, the base R functions that achieve the same ends as the plyr package often require using nested forloops and lots of explicit bookkeeping. The bookkeeping issue is especially burdensome if the code needs to be changed to accomodate a different task. Additionally, in base R, you need to know exactly how your output looks before running the code because you need to set up output arrays and their dimensions before your code can be run.


3. **In 50 to 100 words describe the split-apply-combine paradigm.**
 
As described succinctly in the abstract of this paper, the split-apply-combine paradigm refers to the process where you handle a large task by first breaking up the problem into manageable pieces. Then by completing or addressing each of the smaller pieces, and finally combining all the pieces back together. 

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

