---
author: "Saqlain Ali"
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

library("plyr")
library(dplyr)


baseball <- ddply(baseball, .(id), transform, 
                  cyear = year - min(year) + 1)

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

Functions such as split(), lapply() and rbind() support the split-apply-combine strategy. These are sufficient but are complicated. The most difficult task while using these functions is to attach the appropriate labels to the output data. Thus mapply() is used to match the models to their source data. But on the otherhand while using 'plyr' function it takes care of adding the appropriate labels and the code is really conscise.


3. **In 50 to 100 words describe the split-apply-combine paradigm.**

We break up a complex problem into small manageable pieces, operate on each piece independently and then put back all the pieces together. This strategy of breaking up a big problem and combining is called split-apply-combine strategy. At first, we split the data into groups based on some criteria and then apply a function to each group independently. Lastly, we combine all the data into some form of data structures like arrays, lists or dataframes.

 

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

