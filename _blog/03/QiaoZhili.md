---
author: "Zhili Qiao"
title: "Stat 585 Blog 3"
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

1. **The R code for the split-apply-combine paper is posted with the paper. Pick one of the examples demonstrating `plyr` functionality (such as plyr::dlply or plyr::ddply, ...) and rewrite the example using functionality from the package `dplyr`. Make sure that your example actually works.**

`dplyr` package focuses specifically on dataframes. I think the **plyr::dlply** function in `plyr` package is the same as the **group_map** function (used together with **group_by**) in `dplyr` package. The example is shown below:

**plyr::dlply**






```r
baseball <- plyr::ddply(baseball, .(id), transform, 
  cyear = year - min(year) + 1)
baseball <- subset(baseball, ab >= 25)

model <- function(df) {
  lm(rbi / ab ~ cyear, data=df)
}

bmodels <- plyr::dlply(baseball, .(id), model)
print(bmodels[[1]]$coefficients)
```

```
## (Intercept)       cyear 
##    0.183294    0.000148
```

**group_map**


```r
bmodels1 = baseball %>% group_by(id) %>%
  group_map(~ lm(rbi / ab ~ cyear, data = .x))
print(bmodels1[[1]]$coefficients)
```

```
## (Intercept)       cyear 
##    0.183294    0.000148
```

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

The **apply()** set of functions in base R utilizes this strategy. I think **plyr::aaply()** is just a high-dimensional (>2) generalization of **apply()**, which is specifically useful in the analysis of panel data or time-series data. 

I find this blog [https://privefl.github.io/blog/why-loops-are-slow-in-r/](https://privefl.github.io/blog/why-loops-are-slow-in-r/) talking about how apply functions is faster than for loop, in terms of iteratively generating random variables. It should have something to do with stuffs like reallocation of computer memories.

However I did some simulation on calculations of array slices, and I really didn't find **apply()** or **plyr::aaply()** in `dplyr` more sufficient than the simple for loop. The speed of **plyr::aaply()** seems to be faster than **apply()** when dimension is high, but the for loop is the fastest all the time.


```r
simulation = function(n){
  u = rnorm(n^2)
  u = array(u, rep(n, 2))
  
  t1 = Sys.time()
  a = apply(u, 2, function(y){mean(y)})
  t1 = Sys.time() - t1
  
  t2 = Sys.time()
  a = plyr::aaply(u, 2, function(y){mean(y)})
  t2 = Sys.time() - t2
  
  c = c()
  t3 = Sys.time()
  for(i in 1:n){
    c = c(c, mean(u[, i]))
  }
  t3 = Sys.time() - t3
  
  d = array(c(t1, t2, t3), c(1, 3))
  colnames(d) = c('apply', 'plyr::aaply', 'for loop')
  rownames(d) = c(paste('n =', n))
  
  print(d)
}

simulation(100)
```

```
##         apply plyr::aaply for loop
## n = 100 7e-04      0.0102 0.000553
```

```r
simulation(1000)
```

```
##           apply plyr::aaply for loop
## n = 1000 0.0214      0.0908   0.0146
```

```r
simulation(20000)
```

```
##           apply plyr::aaply for loop
## n = 20000   8.2        6.67     6.54
```

3. **In 50 to 100 words describe the split-apply-combine paradigm.**

As its name suggests, the split-apply-combine proceeds by

  - Slicing the array/dataframe/list according to one or more dimension(s)/variable(s)/each element in list
  
  - Mapping a function onto each slice, compute the output
  
  - Join all outputs to reconstruct an array/dataframe/list

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

