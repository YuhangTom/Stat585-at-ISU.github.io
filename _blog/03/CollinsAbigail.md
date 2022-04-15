---
author: "Abigail Collins"
title: "Blog 3: Split-Apply-Combine thoughts"
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
library("ggplot2")
library("plyr")
```

```
## --------------------------------------------------------------------------------------
```

```
## You have loaded plyr after dplyr - this is likely to cause problems.
## If you need functions from both plyr and dplyr, please load plyr first, then dplyr:
## library(plyr); library(dplyr)
```

```
## --------------------------------------------------------------------------------------
```

```
## 
## Attaching package: 'plyr'
```

```
## The following object is masked _by_ '.GlobalEnv':
## 
##     baseball
```

```
## The following objects are masked from 'package:dplyr':
## 
##     arrange, count, desc, failwith, id, mutate, rename, summarise, summarize
```

```r
library("dplyr")
library("renv") #new edits 
```

```
## 
## Attaching package: 'renv'
```

```
## The following objects are masked from 'package:stats':
## 
##     embed, update
```

```
## The following objects are masked from 'package:utils':
## 
##     history, upgrade
```

```
## The following objects are masked from 'package:base':
## 
##     autoload, load, remove
```


```r
renv::init()
```

```
## Error: init aborted
```




```r
# Baseball case study ============================================
baberuth <- subset(baseball, id == "ruthba01")
baberuth <- transform(baberuth, cyear = year - min(year) + 1)
head(baberuth)
```

```
##         id year stint team lg   g  ab   r   h X2b X3b hr rbi sb cs  bb so ibb hbp sh sf
## 1 ruthba01 1915     1  BOS AL  42  92  16  29  10   1  4  21  0 NA   9 23  NA   0  2 NA
## 2 ruthba01 1916     1  BOS AL  67 136  18  37   5   3  3  15  0 NA  10 23  NA   0  4 NA
## 3 ruthba01 1917     1  BOS AL  52 123  14  40   6   3  2  12  0 NA  12 18  NA   0  7 NA
## 4 ruthba01 1918     1  BOS AL  95 317  50  95  26  11 11  66  6 NA  58 58  NA   2  3 NA
## 5 ruthba01 1919     1  BOS AL 130 432 103 139  34  12 29 114  7 NA 101 58  NA   6  3 NA
## 6 ruthba01 1920     1  NYA AL 142 457 158 172  36   9 54 137 14 14 150 80  NA   3  5 NA
##   gidp cyear
## 1   NA     1
## 2   NA     2
## 3   NA     3
## 4   NA     4
## 5   NA     5
## 6   NA     6
```


```r
#this code is calculating the "career year" (cyear) which is the number of years since the player started playing using the ddply package (applying the transform function to the baseball dataset by playerr)
baseball_plyr <- ddply(baseball, .(id), transform, 
  cyear = year - min(year) + 1)
baseball_plyr
```

```
##           id year stint team lg   g  ab   r   h X2b X3b hr rbi sb cs bb so ibb hbp sh
## 1  aaronha01 1954     1  ML1 NL 122 468  58 131  27   6 13  69  2  2 28 39  NA   3  6
## 2  aaronha01 1955     1  ML1 NL 153 602 105 189  37   9 27 106  3  1 49 61   5   3  7
## 3  aaronha01 1956     1  ML1 NL 153 609 106 200  34  14 26  92  2  4 37 54   6   2  5
## 4  aaronha01 1957     1  ML1 NL 151 615 118 198  27   6 44 132  1  1 57 58  15   0  0
## 5  aaronha01 1958     1  ML1 NL 153 601 109 196  34   4 30  95  4  1 59 49  16   1  0
## 6  aaronha01 1959     1  ML1 NL 154 629 116 223  46   7 39 123  8  0 51 54  17   4  0
## 7  aaronha01 1960     1  ML1 NL 153 590 102 172  20  11 40 126 16  7 60 63  13   2  0
## 8  aaronha01 1961     1  ML1 NL 155 603 115 197  39  10 34 120 21  9 56 64  20   2  1
## 9  aaronha01 1962     1  ML1 NL 156 592 127 191  28   6 45 128 15  7 66 73  14   3  0
## 10 aaronha01 1963     1  ML1 NL 161 631 121 201  29   4 44 130 31  5 78 94  18   0  0
## 11 aaronha01 1964     1  ML1 NL 145 570 103 187  30   2 24  95 22  4 62 46   9   0  0
## 12 aaronha01 1965     1  ML1 NL 150 570 109 181  40   1 32  89 24  4 60 81  10   1  0
## 13 aaronha01 1966     1  ATL NL 158 603 117 168  23   1 44 127 21  3 76 96  15   1  0
## 14 aaronha01 1967     1  ATL NL 155 600 113 184  37   3 39 109 17  6 63 97  19   0  0
## 15 aaronha01 1968     1  ATL NL 160 606  84 174  33   4 29  86 28  5 64 62  23   1  0
## 16 aaronha01 1969     1  ATL NL 147 547 100 164  30   3 44  97  9 10 87 47  19   2  0
## 17 aaronha01 1970     1  ATL NL 150 516 103 154  26   1 38 118  9  0 74 63  15   2  0
## 18 aaronha01 1971     1  ATL NL 139 495  95 162  22   3 47 118  1  1 71 58  21   2  0
## 19 aaronha01 1972     1  ATL NL 129 449  75 119  10   0 34  77  4  0 92 55  15   1  0
## 20 aaronha01 1973     1  ATL NL 120 392  84 118  12   1 40  96  1  1 68 51  13   1  0
## 21 aaronha01 1974     1  ATL NL 112 340  47  91  16   0 20  69  1  0 39 29   6   0  1
## 22 aaronha01 1975     1  ML4 AL 137 465  45 109  16   2 12  60  0  1 70 51   3   1  1
## 23 aaronha01 1976     1  ML4 AL  85 271  22  62   8   0 10  35  0  1 35 38   1   0  0
## 24 abernte02 1955     1  WS1 AL  40  26   1   4   0   0  0   0  0  0  0  6   0   0  4
## 25 adairje01 1959     1  BAL AL  12  35   3  11   0   1  0   2  0  0  1  5   0   0  0
## 26 adairje01 1961     1  BAL AL 133 386  41 102  21   1  9  37  5  2 35 51   4   2  1
## 27 adairje01 1962     1  BAL AL 139 538  67 153  29   4 11  48  7  7 27 77   1   2  4
## 28 adairje01 1963     1  BAL AL 109 382  34  87  21   3  6  30  3  3  9 51   2   2  3
## 29 adairje01 1964     1  BAL AL 155 569  56 141  20   3  9  47  3  2 28 72  10   1  4
## 30 adairje01 1965     1  BAL AL 157 582  51 151  26   3  7  66  6  4 35 65   7   2  4
## 31 adairje01 1966     1  BAL AL  17  52   3  15   1   0  0   3  0  0  4  8   0   0  1
## 32 adairje01 1966     2  CHA AL 105 370  27  90  18   2  4  36  3  2 17 44   0   1  9
## 33 adairje01 1967     1  CHA AL  28  98   6  20   4   0  0   9  0  1  4 17   0   1  2
## 34 adairje01 1967     2  BOS AL  89 316  41  92  13   1  3  26  1  4 13 35   0   2  4
## 35 adairje01 1968     1  BOS AL  74 208  18  45   1   0  2  12  0  0  9 28   2   1  6
## 36 adairje01 1969     1  KCA AL 126 432  29 108   9   1  5  48  1  3 20 36   4   3  2
## 37 adairje01 1970     1  KCA AL   7  27   0   4   0   0  0   1  0  1  5  3   1   0  1
## 38 adamsba01 1909     1  PIT NL  25  39   0   2   0   1  0   1  0 NA  2 NA  NA   0  5
## 39 adamsba01 1910     1  PIT NL  34  83   9  16   3   0  0   6  0 NA  9 23  NA   0  5
## 40 adamsba01 1911     1  PIT NL  40 103   9  26   5   1  0  10  0 NA  3 17  NA   0  1
## 41 adamsba01 1912     1  PIT NL  28  53   5  12   3   1  0   3  0 NA  8  9  NA   0  1
## 42 adamsba01 1913     1  PIT NL  43 114  13  33   6   2  0  13  0 NA  1 16  NA   0  3
## 43 adamsba01 1914     1  PIT NL  40  97   8  16   0   2  1   4  0 NA  3 29  NA   1  2
##    sf gidp cyear
## 1   4   13     1
## 2   4   20     2
## 3   7   21     3
## 4   3   13     4
## 5   3   21     5
## 6   9   19     6
## 7  12    8     7
## 8   9   16     8
## 9   6   14     9
## 10  5   11    10
## 11  2   22    11
## 12  8   15    12
## 13  8   14    13
## 14  6   11    14
## 15  5   21    15
## 16  3   14    16
## 17  6   13    17
## 18  5    9    18
## 19  2   17    19
## 20  4    7    20
## 21  2    6    21
## 22  6   15    22
## 23  2    8    23
## 24  0    1     1
## 25  0    0     1
## 26  4    6     3
## 27  3   15     4
## 28  5   17     5
## 29  3   20     6
## 30  2   26     7
## 31  1    1     8
## 32  5   14     8
## 33  1    5     9
## 34  2   10     9
## 35  0   10    10
## 36  4   24    11
## 37  0    1    12
## 38 NA   NA     1
## 39 NA   NA     2
## 40 NA   NA     3
## 41 NA   NA     4
## 42 NA   NA     5
## 43 NA   NA     6
##  [ reached 'max' / getOption("max.print") -- omitted 16286 rows ]
```

Code to do this using the "dplyr" package

```r
baseball_dplyr<- baseball%>%
  dplyr::group_by(id)%>%
  mutate(cyear = year - min(year) + 1)
baseball_dplyr
```

```
## # A tibble: 16,329 × 23
## # Groups:   id [1,152]
##    id       year stint team  lg        g    ab     r     h   X2b   X3b    hr   rbi    sb
##    <chr>   <int> <int> <chr> <chr> <int> <int> <int> <int> <int> <int> <int> <int> <int>
##  1 ansonc…  1871     1 RC1   ""       25   120    29    39    11     3     0    16     6
##  2 forced…  1871     1 WS3   ""       32   162    45    45     9     4     0    29     8
##  3 matheb…  1871     1 FW1   ""       19    89    15    24     3     1     0    10     2
##  4 startj…  1871     1 NY2   ""       33   161    35    58     5     1     1    34     4
##  5 suttoe…  1871     1 CL1   ""       29   128    35    45     3     7     3    23     3
##  6 whited…  1871     1 CL1   ""       29   146    40    47     6     5     1    21     2
##  7 yorkto…  1871     1 TRO   ""       29   145    36    37     5     7     2    23     2
##  8 ansonc…  1872     1 PH1   ""       46   217    60    90    10     7     0    50     6
##  9 burdoj…  1872     1 BR2   ""       37   174    26    46     3     0     0    15     0
## 10 forced…  1872     1 TRO   ""       25   130    40    53    11     0     0    16     2
## # … with 16,319 more rows, and 9 more variables: cs <int>, bb <int>, so <int>,
## #   ibb <int>, hbp <int>, sh <int>, sf <int>, gidp <int>, cyear <dbl>
```

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

I am most familiar with the base R functions split(), apply(), and rbind()/cbind(), which are also discussed in the paper. In my opinion, these are not the most sufficient way to analyze data, especially when working with large data. These functions take multiple "steps" (or lines of code) to get results. When you use packages such as "dplyr", you can essentially get the same results from all of those functions in one step (or "r chunk" with multiple "pipes"). Additionally, when you use split and apply/lapply/sapply/mapply, you need to specify and keep track of the location (columns/rows) to which you are applying the functions. This can get messy and confusing rather quickly. "dplyr" may be a better option because it allows you to use group_by/mutate which only require variable names. I also think that "dplyr" is easier to read and understand logically as piping runs your code in a clear logical order. In summary, although base R functions do work and may be easy to use in simple analysis, I believe packages (such as dlpyr/plyr) allow for quicker, more digestible/understandable analysis. 



3. **In 50 to 100 words describe the split-apply-combine paradigm.**

Essentially all analysis builds upon the idea of "split-apply-combine". The "split" refers to the necessary breakdown of the data to do the analysis. It is ideal to subset your data to only the relevant information (ie split) to optimally perform analysis on the variables of interest. The "apply" portion refer to the actual analysis being done at that given step. Perhaps you need to take the mean of a column in one step, and transform a column in another step, this refers to the "apply" being done to each "split". Finally, after your analysis is complete, you combine the results into one readable set of data. This will allow for interpretation, comparison, and understanding of the "apply" steps. Therefore, completing your analysis.


 

Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)

