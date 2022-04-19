---
author: "Abraham Adokwei"
title: "Dplyr functionality"
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
  - I present on how to achieve results of <strong>plyr::m*ply()</strong>. The function is called once for each row, with arguments given by the column. 
  - I achieved this by applying the function <strong>dplyr::rowwise()>/strong> together with the pipe operator. 
  - 

```r
examp<- data.frame(n=c(10, 100, 50),
                   mean=c(5,5,10),
                   sd=c(1,2,1))

print(rowwise(examp) %>% rnorm())
```

```
## Error in rowwise(examp) %>% rnorm(): could not find function "%>%"
```

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

  - *merge*, *Split*,*by*, *subset*, and *tapply*
  - In most cases, these functions work pretty well. However, in some cases, they are not the best to use. For example, in some situations, it is easier to use dplyr::filter() rather than going with subset()

3. **In 50 to 100 words describe the split-apply-combine paradigm.**
  - In Statistics, we often find ourselves in situation where we need to explore our data. Exploring our data means at some point, we may have to consider the various groups or clusters in our data. The *split-apply-combine paradigm* is particularly useful in these situation. Under this workflow, we split our data into homogeneous groups, apply procedures of interest and finally assemble the results from these individual pieces. 

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

