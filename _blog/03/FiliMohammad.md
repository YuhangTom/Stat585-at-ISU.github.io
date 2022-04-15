---
author: "Mohammad Fili"
title: "Blog #3"
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

__Answer__:
    

```r
install.packages("dplyr")
```

```
## 
## The downloaded binary packages are in
## 	/var/folders/1x/tvy5cf5j4glg4_6g8cxvrcbm7qbgrn/T//RtmpQgoSEV/downloaded_packages
```

```r
install.packages("plyr")
```

```
## Error in install.packages : Updating loaded packages
```

```r
library(plyr)
library(dplyr)
```
    
Using `ddply` function from `plyr` package, we have:



```r
baseball_1 <- 
  ddply(baseball, .(id), transform, cyear = year - min(year) + 1)

head(baseball_1[c('id', 'cyear')])
```

```
##          id cyear
## 1 aaronha01     1
## 2 aaronha01     2
## 3 aaronha01     3
## 4 aaronha01     4
## 5 aaronha01     5
## 6 aaronha01     6
```
    
Now, using `dplyr` package, we have:
    
    
    ```r
    baseball_2 = baseball %>% 
                  group_by(id) %>% 
                  summarise(cyear = year - min(year) + 1, .groups = 'keep')
    ```
    
    ```
    ## Error in quickdf(.data[names(cols)]): length(rows) == 1 is not TRUE
    ```
    
    ```r
    head(baseball_2)
    ```
    
    ```
    ## Error in head(baseball_2): object 'baseball_2' not found
    ```
    

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

__Answer__:

For Splitting:

* `subset`
* `split`

For Applying:

* `lapply`
* `mapply`
* `sapply`
* `transform`
* `by`
* `replicate`
* `aggregate`

For Combining:

* `rbind`
* `cbind`

can be used to implement the split-apply-combine strategy:

For example, for the example in the previous part, we can use base functions to get similar results:


```r
  # Splitting
  df_id = split(baseball, baseball$id)

  # Applying
  results <- 
    lapply(df_id, function(x){transform(x, cyear = year - min(year) + 1)})
  
  # Combining
  baseball_4 = do.call('rbind', results)
  
  # Display head of the table
  head(baseball_4[, c('id', 'cyear')])
```

```
##                        id cyear
## aaronha01.37157 aaronha01     1
## aaronha01.37795 aaronha01     2
## aaronha01.38408 aaronha01     3
## aaronha01.39023 aaronha01     4
## aaronha01.39645 aaronha01     5
## aaronha01.40291 aaronha01     6
```

These function are useful; however, may not be sufficient as Hadley explained one its disadvantages: 

"The built-in R functions focus mainly on arrays and lists, not data frames, and most attempt to return an atomic data structure if possible, and if not, a list. This ambiguity of the output type is fine for interactive use, but does make programming with these functions tricky."

Second, we can do the same job in fewer lines of code which makes the code easier to debug later on, if needed.


3. **In 50 to 100 words describe the split-apply-combine paradigm.**

It is a very helpful skill in data analysis. In many cases, we are interested in splitting the data into some groups (according to one or more criteria), and then applying a certain function on each group, and then combining the results into one object and print it out. We can apply this strategy in data pre-processing, modeling, displaying the results. In fact, we have a big problem that we want to split it into smaller chunks and solve each chunk separately and then paste the results together.



Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

