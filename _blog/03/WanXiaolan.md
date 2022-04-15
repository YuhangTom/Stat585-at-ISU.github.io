---
title: "blog #3"
author: "Xiaolan Wan"
layout: blog
due-date: '2022-02-10'
root: ../../
topic: '03'
output: github_document
---
  
  ## Prompt:
  
The `plyr` package has by now been replaced by other, even faster packages, but the idea of *Split, apply, combine* is as relevant as ever.

Read the paper [The Split-Apply-Combine Strategy for Data Analysis](https://www.jstatsoft.org/article/view/v040i01) by Hadley Wickham.


Write a blog post addressing the following questions: 
  
1. **The R code for the split-apply-combine paper is posted with the paper. Pick one of the examples demonstrating `plyr` functionality (such as dlply or ddply, ...) and rewrite the example using functionality from the package `dplyr`. Make sure that your example actually works.**
  
I picked the functionality `ddply`, as shown in the Baseball Case Study, which calculates the “career year” using `ddply`. I rewrote this example using `mutate` function from the package `dplyr`. 


```r
install.packages("dplyr")
```

```
## 
## The downloaded binary packages are in
## 	/var/folders/1x/tvy5cf5j4glg4_6g8cxvrcbm7qbgrn/T//RtmpQgoSEV/downloaded_packages
```

```r
library("dplyr")
install.packages("plyr")
```

```
## Error in install.packages : Updating loaded packages
```

```r
library("plyr")
baseball %>% 
  group_by(id) %>% 
  dplyr::mutate(cyear = year - min(year) + 1) %>% 
  ungroup() %>% arrange(id, year) %>% as.data.frame() 
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
## 25 abernte02 1956     1  WS1 AL   5  11   1   2   0   0  0   1  0  0  0  5   0   0  0
## 26 abernte02 1957     1  WS1 AL  26  24   3   4   1   0  0   1  0  0  1  5   0   1  2
## 27 abernte02 1960     1  WS1 AL   2   1   1   1   0   0  0   0  0  0  0  0   0   0  0
## 28 abernte02 1963     1  CLE AL  43   5   1   2   1   0  0   0  0  0  1  2   0   0  1
## 29 abernte02 1964     1  CLE AL  53   6   0   0   0   0  0   0  0  0  0  3   0   0  1
## 30 abernte02 1965     1  CHN NL  84  18   1   3   0   0  0   2  0  0  0  7   0   1  3
## 31 abernte02 1966     1  CHN NL  20   4   0   0   0   0  0   0  0  0  0  2   0   0  0
## 32 abernte02 1966     2  ATL NL  38   8   0   2   0   0  0   0  0  0  1  3   0   0  0
## 33 abernte02 1967     1  CIN NL  70  17   0   1   0   0  0   2  0  0  0 10   0   0  0
## 34 abernte02 1968     1  CIN NL  78  17   2   0   0   0  0   0  0  0  3 12   0   0  0
## 35 abernte02 1969     1  CHN NL  56   8   1   2   1   0  0   1  0  0  0  2   0   0  0
## 36 abernte02 1970     3  KCA AL  36  14   1   3   0   0  0   2  0  0  0  5   0   0  3
## 37 abernte02 1970     1  CHN NL  11   0   0   0   0   0  0   0  0  0  0  0   0   0  0
## 38 abernte02 1970     2  SLN NL  11   3   0   0   0   0  0   0  0  0  0  2   0   0  0
## 39 abernte02 1971     1  KCA AL  63  13   0   1   0   0  0   0  0  0  0  7   0   0  1
## 40 abernte02 1972     1  KCA AL  45   6   0   0   0   0  0   0  0  0  0  3   0   0  0
## 41 adairje01 1958     1  BAL AL  11  19   1   2   0   0  0   0  0  0  1  7   0   0  0
## 42 adairje01 1959     1  BAL AL  12  35   3  11   0   1  0   2  0  0  1  5   0   0  0
## 43 adairje01 1960     1  BAL AL   3   5   1   1   0   0  1   1  0  0  0  0   0   0  0
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
## 25  0    0     2
## 26  0    2     3
## 27  0    0     6
## 28  0    0     9
## 29  0    0    10
## 30  0    0    11
## 31  0    0    12
## 32  0    0    12
## 33  0    1    13
## 34  0    0    14
## 35  0    0    15
## 36  0    0    16
## 37  0    0    16
## 38  0    0    16
## 39  0    0    17
## 40  0    0    18
## 41  0    0     1
## 42  0    0     2
## 43  0    0     3
##  [ reached 'max' / getOption("max.print") -- omitted 21656 rows ]
```

2. **Which (base R) functions do you know that support the split-apply-combine strategy? In your opinion, are these sufficient? State why or why not?**. 

In base `R`, `split`, `aggregate`, and `apply` family support the split-apply-combine strategy. These functions are not sufficient due to limitation on readability and dealing with complicated data structures.


3. **In 50 to 100 words describe the split-apply-combine paradigm.**
  
The application of split-apply-combine paradigm is a data analysis pattern where  a big problem is split into manageable pieces, 
a function is  applied to operate on each piece independently, and the results are then combined to put all the pieces back together.  This strategy  is useful and important, and can be used by many existing tools: GroupBy function in SQL and Python, LOD in Tableau, and  plyr functions in R.





Submit to your repo. Make sure that all of the github actions pass (check menu item Actions - all of the actions should have green checks)



