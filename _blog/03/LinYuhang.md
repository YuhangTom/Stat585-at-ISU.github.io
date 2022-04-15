---
author: "Yuhang LIN"
title: "The Split-Apply-Combine Strategy"
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

    I chose the baseball case study and tried to reproduce the "career year" column by replacing ```plyr::ddply``` with functionality from ```dplyr```.
    
    
    ```r
    library("dplyr")
    
    ### -------------------------
    ###    Baseball case study
    ### -------------------------
    
    ### Original plyr code for creating the "career year" for all players
    baseball.plyr <- plyr::ddply(plyr::baseball, "id", transform, cyear = year - min(year) + 1)
    
    ### dplyr code for creating the "career year" for all players
    ### Create group by id
    baseball.dplyr <- plyr::baseball %>% dplyr::group_by(id) %>%
      ### Create new column cyear as "career year
      dplyr::mutate(cyear = year - min(year) + 1) %>% 
      ### Arrange rows according to id
      dplyr::arrange(id) %>% 
      ### Change to data.frame
      as.data.frame()
    
    ### Examine the data
    str(baseball.plyr)
    ```
    
    ```
    ## 'data.frame':	21699 obs. of  23 variables:
    ##  $ id   : chr  "aaronha01" "aaronha01" "aaronha01" "aaronha01" ...
    ##  $ year : int  1954 1955 1956 1957 1958 1959 1960 1961 1962 1963 ...
    ##  $ stint: int  1 1 1 1 1 1 1 1 1 1 ...
    ##  $ team : chr  "ML1" "ML1" "ML1" "ML1" ...
    ##  $ lg   : chr  "NL" "NL" "NL" "NL" ...
    ##  $ g    : int  122 153 153 151 153 154 153 155 156 161 ...
    ##  $ ab   : int  468 602 609 615 601 629 590 603 592 631 ...
    ##  $ r    : int  58 105 106 118 109 116 102 115 127 121 ...
    ##  $ h    : int  131 189 200 198 196 223 172 197 191 201 ...
    ##  $ X2b  : int  27 37 34 27 34 46 20 39 28 29 ...
    ##  $ X3b  : int  6 9 14 6 4 7 11 10 6 4 ...
    ##  $ hr   : int  13 27 26 44 30 39 40 34 45 44 ...
    ##  $ rbi  : int  69 106 92 132 95 123 126 120 128 130 ...
    ##  $ sb   : int  2 3 2 1 4 8 16 21 15 31 ...
    ##  $ cs   : int  2 1 4 1 1 0 7 9 7 5 ...
    ##  $ bb   : int  28 49 37 57 59 51 60 56 66 78 ...
    ##  $ so   : int  39 61 54 58 49 54 63 64 73 94 ...
    ##  $ ibb  : int  NA 5 6 15 16 17 13 20 14 18 ...
    ##  $ hbp  : int  3 3 2 0 1 4 2 2 3 0 ...
    ##  $ sh   : int  6 7 5 0 0 0 0 1 0 0 ...
    ##  $ sf   : int  4 4 7 3 3 9 12 9 6 5 ...
    ##  $ gidp : int  13 20 21 13 21 19 8 16 14 11 ...
    ##  $ cyear: num  1 2 3 4 5 6 7 8 9 10 ...
    ```
    
    ```r
    str(baseball.dplyr)
    ```
    
    ```
    ## 'data.frame':	21699 obs. of  23 variables:
    ##  $ id   : chr  "aaronha01" "aaronha01" "aaronha01" "aaronha01" ...
    ##  $ year : int  1954 1955 1956 1957 1958 1959 1960 1961 1962 1963 ...
    ##  $ stint: int  1 1 1 1 1 1 1 1 1 1 ...
    ##  $ team : chr  "ML1" "ML1" "ML1" "ML1" ...
    ##  $ lg   : chr  "NL" "NL" "NL" "NL" ...
    ##  $ g    : int  122 153 153 151 153 154 153 155 156 161 ...
    ##  $ ab   : int  468 602 609 615 601 629 590 603 592 631 ...
    ##  $ r    : int  58 105 106 118 109 116 102 115 127 121 ...
    ##  $ h    : int  131 189 200 198 196 223 172 197 191 201 ...
    ##  $ X2b  : int  27 37 34 27 34 46 20 39 28 29 ...
    ##  $ X3b  : int  6 9 14 6 4 7 11 10 6 4 ...
    ##  $ hr   : int  13 27 26 44 30 39 40 34 45 44 ...
    ##  $ rbi  : int  69 106 92 132 95 123 126 120 128 130 ...
    ##  $ sb   : int  2 3 2 1 4 8 16 21 15 31 ...
    ##  $ cs   : int  2 1 4 1 1 0 7 9 7 5 ...
    ##  $ bb   : int  28 49 37 57 59 51 60 56 66 78 ...
    ##  $ so   : int  39 61 54 58 49 54 63 64 73 94 ...
    ##  $ ibb  : int  NA 5 6 15 16 17 13 20 14 18 ...
    ##  $ hbp  : int  3 3 2 0 1 4 2 2 3 0 ...
    ##  $ sh   : int  6 7 5 0 0 0 0 1 0 0 ...
    ##  $ sf   : int  4 4 7 3 3 9 12 9 6 5 ...
    ##  $ gidp : int  13 20 21 13 21 19 8 16 14 11 ...
    ##  $ cyear: num  1 2 3 4 5 6 7 8 9 10 ...
    ```
    
    ```r
    ### Check if two output matches
    ### As there is NA in the data, we either omit the NAs or only compare the column we created
    identical(na.omit(baseball.plyr), na.omit(baseball.dplyr))
    ```
    
    ```
    ## [1] TRUE
    ```
    
    ```r
    identical(baseball.plyr$cyear, baseball.dplyr$cyear)
    ```
    
    ```
    ## [1] TRUE
    ```



2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 
  
    I am not aware of the existence of this split-apply-combine strategy before.
    Followed by the example that Hadley discussed on page 4,
    in base R,
    we have ```split()``` to split,
    ```lapply``` to apply,
    and ```rbind``` to combine.
    Of course there are more functions to conduct this procedure,
    like ```apply``` and ```cbind```.
    In my point of view,
    I found them sufficient enough,
    as I have used them for quite a while.
    But I need to think for a while which function is appropriate to use under different scenarios,
    which is not ideal.
    It is not intuitive enough,
    and ```plyr``` and ```dplyr``` packages seems to make it easier,
    as we can write in a more systematic and neater way.
  

3. **In 50 to 100 words describe the split-apply-combine paradigm.**

    When a problem comes,
    we would observe the similarity between each part of the problem,
    split the input into small parts,
    apply whatever functions or operations we want,
    and then combine the output altogether to get the final result.
    This idea can somehow replace the for loops when the assumptions hold,
    and that would express the intent clearer.
 

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)


