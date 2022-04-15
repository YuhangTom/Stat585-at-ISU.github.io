---
author: "Danyang Zhang"
title: "Split-Apply-Combine Paradigm"
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
# An example with "ddply"
baseball.1 <- ddply(baseball, .(id), transform, cyear = year - min(year) + 1)
head(baseball.1)
```

```
##          id year stint team lg   g  ab   r   h X2b X3b hr rbi sb cs bb so ibb hbp sh sf
## 1 aaronha01 1954     1  ML1 NL 122 468  58 131  27   6 13  69  2  2 28 39  NA   3  6  4
## 2 aaronha01 1955     1  ML1 NL 153 602 105 189  37   9 27 106  3  1 49 61   5   3  7  4
## 3 aaronha01 1956     1  ML1 NL 153 609 106 200  34  14 26  92  2  4 37 54   6   2  5  7
## 4 aaronha01 1957     1  ML1 NL 151 615 118 198  27   6 44 132  1  1 57 58  15   0  0  3
## 5 aaronha01 1958     1  ML1 NL 153 601 109 196  34   4 30  95  4  1 59 49  16   1  0  3
## 6 aaronha01 1959     1  ML1 NL 154 629 116 223  46   7 39 123  8  0 51 54  17   4  0  9
##   gidp cyear
## 1   13     1
## 2   20     2
## 3   21     3
## 4   13     4
## 5   21     5
## 6   19     6
```

```r
# Rewrite the above example using functionality from the package "dplyr"
baseball.2 <- baseball %>% 
  group_by(id) %>% 
  mutate(cyear = year - min(year) + 1) %>% 
  ungroup() %>% 
  arrange(id, cyear) %>% 
  print(n = 5)
```

```
## # A tibble: 21,699 × 23
##   id         year stint team  lg        g    ab     r     h   X2b   X3b    hr   rbi
##   <chr>     <int> <int> <chr> <chr> <int> <int> <int> <int> <int> <int> <int> <int>
## 1 aaronha01  1954     1 ML1   NL      122   468    58   131    27     6    13    69
## 2 aaronha01  1955     1 ML1   NL      153   602   105   189    37     9    27   106
## 3 aaronha01  1956     1 ML1   NL      153   609   106   200    34    14    26    92
## 4 aaronha01  1957     1 ML1   NL      151   615   118   198    27     6    44   132
## 5 aaronha01  1958     1 ML1   NL      153   601   109   196    34     4    30    95
##      sb    cs    bb    so   ibb   hbp    sh    sf  gidp cyear
##   <int> <int> <int> <int> <int> <int> <int> <int> <int> <dbl>
## 1     2     2    28    39    NA     3     6     4    13    84
## 2     3     1    49    61     5     3     7     4    20    85
## 3     2     4    37    54     6     2     5     7    21    86
## 4     1     1    57    58    15     0     0     3    13    87
## 5     4     1    59    49    16     1     0     3    21    88
## # … with 21,694 more rows
```

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

"Aggregate", "apply", "by", "lapply", "mapply", "replicate", "sapply", "tapply", "sweep". In my opinion, they are not sufficient as they have requirements on the input data structure and are not flexible to assign the output data structure, wheres the tools of plyr abstract away from the details of the underlying data structure.

3. **In 50 to 100 words describe the split-apply-combine paradigm.**

The split-apply-combine paradigm splits up a certain type of input (that can be an array, a list, or a data frame) into pieces, applies a processing function to each piece in turn independently, and recombines the pieces back together again. The output type (that can be an array, a list, a data frame, or discarded) defines how the pieces will be joined back together and how they will be labelled.
