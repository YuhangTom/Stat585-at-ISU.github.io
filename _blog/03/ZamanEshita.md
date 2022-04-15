<<<<<<< HEAD
---
author: "Firstname Lastname"
title: "Title of your post"
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
###code with plyr
baseball_a <- plyr::ddply(baseball, .(id), transform, 
  cyear = year - min(year) + 1)
###code with dplyr

library(dplyr)

bb <- baseball %>% group_by(id) %>% mutate(cyear = year-min(year)+1)
```


2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 
Base R functions that support the spilt-apply-combine strategy are split(), apply(), aperm(), stack(). I do not think they are sufficient for Split-Apply-Combine approach. Even though these functions are much more efficient than loops, still there are many limitations to them. Attaching appropriate labels to the data is very complicated here. The type of
labels needed depends on the output data structure, e.g., for arrays, dimnames are labels,
for data frames, values in additional columns are the labels. mapply() is used to match the models to their source data in order to extract informative labels. But plyr can take care of this efficiently. Also, base R functions are slower. 

3. **In 50 to 100 words describe the split-apply-combine paradigm.**
 
Often in data analysis, we need to work with huge amount of data. These data may seem to be unrelated, but they can reveal interesting relations when analyzed properly. In those cases, we might need to split the data into smaller fragments and apply the appropriate operation on a specific group or groups of data. When we are done operating on the data, we need to combine the results to generate the output. Split-apply-combine strategy helps to explore data fragments to analyze the relationship or patterns between data elements and output them in desired format.

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

