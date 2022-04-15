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
In plyr if we want to calculate the career year for each player we should write this code:
baseball <- ddply(baseball, .(id), transform, + cyear = year - min(year) + 1) 
In dplyer we will have:
baseball_players <- group_by (baseball, id) 
career_year <- group_map (baseball_players, cyear = year - min(year) +1)
we have to use summarize() function in dplyr to aggregate and combine data again. 
2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

If we want to use basic R functions to do Split-Apply-Combine strategy, we should use split() to break the data into subsets, and mapply(), lapply(), or sapply() to operate on each subset, and finally use rbind() to combine the various outputs. The mapply() function is a multivariate apply of sorts which applies a function in parallel over a set of arguments. The lapply() function is applied for operations on list objects and returns a list object of same length of original set. The sapply() function takes list, vector or data frame as input and gives output in vector or matrix. These functions might be sufficient in some cases, but sophisticated packages such as plyr and dplyr are much more useful and efficient and they can be used for all types of problems. 

3. **In 50 to 100 words describe the split-apply-combine paradigm.**

Sometimes when we want to do data analysis we face a big problem that might be complicated. This can happen in every stage of data mining process such as data preparation, modeling, or summarization and visualization. One approach that can be very helpful is Split-Apply-Combine strategy. This refers to the process of breaking data into smaller subsets, operate on each subset separately, and then combine them together again. In this way, we will be able to break the problem into manageable pieces.  

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

