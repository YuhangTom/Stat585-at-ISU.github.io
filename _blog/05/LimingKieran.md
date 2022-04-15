---
author: "Kieran Liming"
title: "Title of your post"
layout: post
topic: "05"
short-topic: Fixing github actions
due-date: 2022-02-24
root: ../../
output: github_document
---

## Prompt:

Remember the github action disaster of blog #3? :)
This week, we will try to tackle the cleanup, and you write a paragraph or two about your experience with it. 

Read the vignette [Introduction to renv](https://rstudio.github.io/renv/articles/renv.html) for the `renv` R package by Kevin Ushey.

Then do:

1. **Install the R package `renv` on your local machine.**

2. **In the project for blog 3, initialize the workflow used by the `renv` package.**


```r
library(renv)
renv::init()
```

```
## Error: init aborted
```

3. **Add all dependencies to the environment (implicitly by installing all the depepndencies or explicilty by listing dependencies in a DESCRIPTION file).**


```r
renv::dependencies()
```

```
## Finding R package dependencies ... [48/575] [49/575] [50/575] [51/575] [52/575] [53/575] [54/575] [55/575] [56/575] [57/575] [58/575] [59/575] [60/575] [61/575] [62/575] [63/575] [64/575] [65/575] [66/575] [67/575] [68/575] [69/575] [70/575] [71/575] [72/575] [73/575] [74/575] [75/575] [76/575] [77/575] [78/575] [79/575] [80/575] [81/575] [82/575] [83/575] [84/575] [85/575] [86/575] [87/575] [88/575] [89/575] [90/575] [91/575] [92/575] [93/575] [94/575] [95/575] [96/575] [97/575] [98/575] [99/575] [100/575] [101/575] [102/575] [103/575] [104/575] [105/575] [106/575] [107/575] [108/575] [109/575] [110/575] [111/575] [112/575] [113/575] [114/575] [115/575] [116/575] [117/575] [118/575] [119/575] [120/575] [121/575] [122/575] [123/575] [124/575] [125/575] [126/575] [127/575] [128/575] [129/575] [130/575] [131/575] [132/575] [133/575] [134/575] [135/575] [136/575] [137/575] [138/575] [139/575] [140/575] [141/575] [142/575] [143/575] [144/575] [145/575] [146/575] [147/575] [148/575] [149/575] [150/575] [151/575] [152/575] [153/575] [154/575] [155/575] [156/575] [157/575] [158/575] [159/575] [160/575] [161/575] [162/575] [163/575] [164/575] [165/575] [166/575] [167/575] [168/575] [169/575] [170/575] [171/575] [172/575] [173/575] [174/575] [175/575] [176/575] [177/575] [178/575] [179/575] [180/575] [181/575] [182/575] [183/575] [184/575] [185/575] [186/575] [187/575] [188/575] [189/575] [190/575] [191/575] [192/575] [193/575] [194/575] [195/575] [196/575] [197/575] [198/575] [199/575] [200/575] [201/575] [202/575] [203/575] [204/575] [205/575] [206/575] [207/575] [208/575] [209/575] [210/575] [211/575] [212/575] [213/575] [214/575] [215/575] [216/575] [217/575] [218/575] [219/575] [220/575] [221/575] [222/575] [223/575] [224/575] [225/575] [226/575] [227/575] [228/575] [229/575] [230/575] [231/575] [232/575] [233/575] [234/575] [235/575] [236/575] [237/575] [238/575] [239/575] [240/575] [241/575] [242/575] [243/575] [244/575] [245/575] [246/575] [247/575] [248/575] [249/575] [250/575] [251/575] [252/575] [253/575] [254/575] [255/575] [256/575] [257/575] [258/575] [259/575] [260/575] [261/575] [262/575] [263/575] [264/575] [265/575] [266/575] [267/575] [268/575] [269/575] [270/575] [271/575] [272/575] [273/575] [274/575] [275/575] [276/575] [277/575] [278/575] [279/575] [280/575] [281/575] [282/575] [283/575] [284/575] [285/575] [286/575] [287/575] [288/575] [289/575] [290/575] [291/575] [292/575] [293/575] [294/575] [295/575] [296/575] [297/575] [298/575] [299/575] [300/575] [301/575] [302/575] [303/575] [304/575] [305/575] [306/575] [307/575] [308/575] [309/575] [310/575] [311/575] [312/575] [313/575] [314/575] [315/575] [316/575] [317/575] [318/575] [319/575] [320/575] [321/575] [322/575] [323/575] [324/575] [325/575] [326/575] [327/575] [328/575] [329/575] [330/575] [331/575] [332/575] [333/575] [334/575] [335/575] [336/575] [337/575] [338/575] [339/575] [340/575] [341/575] [342/575] [343/575] [344/575] [345/575] [346/575] [347/575] [348/575] [349/575] [350/575] [351/575] [352/575] [353/575] [354/575] [355/575] [356/575] [357/575] [358/575] [359/575] [360/575] [361/575] [362/575] [363/575] [364/575] [365/575] [366/575] [367/575] [368/575] [369/575] [370/575] [371/575] [372/575] [373/575] [374/575] [375/575] [376/575] [377/575] [378/575] [379/575] [380/575] [381/575] [382/575] [383/575] [384/575] [385/575] [386/575] [387/575] [388/575] [389/575] [390/575] [391/575] [392/575] [393/575] [394/575] [395/575] [396/575] [397/575] [398/575] [399/575] [400/575] [401/575] [402/575] [403/575] [404/575] [405/575] [406/575] [407/575] [408/575] [409/575] [410/575] [411/575] [412/575] [413/575] [414/575] [415/575] [416/575] [417/575] [418/575] [419/575] [420/575] [421/575] [422/575] [423/575] [424/575] [425/575] [426/575] [427/575] [428/575] [429/575] [430/575] [431/575] [432/575] [433/575] [434/575] [435/575] [436/575] [437/575] [438/575] [439/575] [440/575] [441/575] [442/575] [443/575] [444/575] [445/575] [446/575] [447/575] [448/575] [449/575] [450/575] [451/575] [452/575] [453/575] [454/575] [455/575] [456/575] [457/575] [458/575] [459/575] [460/575] [461/575] [462/575] [463/575] [464/575] [465/575] [466/575] [467/575] [468/575] [469/575] [470/575] [471/575] [472/575] [473/575] [474/575] [475/575] [476/575] [477/575] [478/575] [479/575] [480/575] [481/575] [482/575] [483/575] [484/575] [485/575] [486/575] [487/575] [488/575] [489/575] [490/575] [491/575] [492/575] [493/575] [494/575] [495/575] [496/575] [497/575] [498/575] [499/575] [500/575] [501/575] [502/575] [503/575] [504/575] [505/575] [506/575] [507/575] [508/575] [509/575] [510/575] [511/575] [512/575] [513/575] [514/575] [515/575] [516/575] [517/575] [518/575] [519/575] [520/575] [521/575] [522/575] [523/575] [524/575] [525/575] [526/575] [527/575] [528/575] [529/575] [530/575] [531/575] [532/575] [533/575] [534/575] [535/575] [536/575] [537/575] [538/575] [539/575] [540/575] [541/575] [542/575] [543/575] [544/575] [545/575] [546/575] [547/575] [548/575] [549/575] [550/575] [551/575] [552/575] [553/575] [554/575] [555/575] [556/575] [557/575] [558/575] [559/575] [560/575] [561/575] [562/575] [563/575] [564/575] [565/575] [566/575] [567/575] [568/575] [569/575] [570/575] [571/575] [572/575] [573/575] [574/575] [575/575] Done!
```

```
##                                                                                                                          Source
## 1     /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/aadokwei/AdokweiAbraham_Addo.Rmd
## 2          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/aadokwei/AdokweiAbraham.Rmd
## 3    /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/ahernnelson/LastnameFirstname.Rmd
## 4          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/amclever/CleveringaAlex.Rmd
## 5          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/avcoll16/CollinsAbigail.Rmd
## 6    /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/blakekassmeyer/KassmeyerBlake.Rmd
## 7               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/Bufei2022/GuoBufei.Rmd
## 8         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/cerdengithub/ErdenCoskun.Rmd
## 9         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/cgjroe/LastnameFirstname.Rmd
## 10       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/danyangzhang/ZhangDanyang.Rmd
## 11         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/eshitazaman/ZamanEshita.Rmd
## 12    /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/Ghazal2371/LastnameFirstname.Rmd
## 13       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/glcoll16/CollinsGabrielle.Rmd
## 14         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/heike/LastnameFirstname.Rmd
## 15           /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/kieran41/LimingKieran.Rmd
## 16        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/Livy20/LastnameFirstname.Rmd
## 17             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/m-fili/FiliMohammad.Rmd
## 18                       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/PangJinji.Rmd
## 19         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/PariisAk/ParastooAkbari.Rmd
## 20       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/rcast1215/CastanedaRobert.Rmd
## 21        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/Saqlainrocks7/AliSaqlain.Rmd
## 22      /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/willju-wangqian/JuWangqian.Rmd
## 23           /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/xiaolinzi1112/QuanLin.Rmd
## 24       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/xlanwan/LastnameFirstname.Rmd
## 25              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/xlanwan/XiaolanWan.Rmd
## 26              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/xlanwan/XiaolanWan.Rmd
## 27             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/YuhangTom/LinYuhang.Rmd
## 28               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/YunhuiQi/QiYunhui.Rmd
## 29             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/zhiliqiao/QiaoZhili.Rmd
## 30               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #1-01-30-2022-01-24-28/zzhou93/ZhouZirou.Rmd
## 31         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/aadokwei/AdokweiAbraham.Rmd
## 32      /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/aadokwei/LastnameFirstname.Rmd
## 33         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/amclever/CleveringaAlex.Rmd
## 34         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/avcoll16/CollinsAbigail.Rmd
## 35              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/Bufei2022/GuoBufei.Rmd
## 36                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/CastanedaRobert.Rmd
## 37        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/cerdengithub/ErdenCoskun.Rmd
## 38       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/danyangzhang/ZhangDanyang.Rmd
## 39         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/eshitazaman/ZamanEshita.Rmd
## 40    /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/Ghazal2371/LastnameFirstname.Rmd
## 41       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/glcoll16/CollinsGabrielle.Rmd
## 42             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/JinjiPang/PangJinji.Rmd
## 43           /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/kieran41/LimingKieran.Rmd
## 44             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/m-fili/FiliMohammad.Rmd
## 45         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/PariisAk/ParastooAkbari.Rmd
## 46        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/Saqlainrocks7/AliSaqlain.Rmd
## 47      /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/willju-wangqian/JuWangqian.Rmd
## 48           /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/xiaolinzi1112/QuanLin.Rmd
## 49              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/xlanwan/WanXiaolan.Rmd
## 50             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/YuhangTom/LinYuhang.Rmd
## 51               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/YunhuiQi/QiYunhui.Rmd
## 52             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/zhiliqiao/QiaoZhili.Rmd
## 53               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #2-02-05-2022-11-40-19/zzhou93/ZhouZirou.Rmd
## 54         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/aadokwei/AbrahamAdokwei.Rmd
## 55                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/aadokwei/README.Rmd
## 56                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/aadokwei/README.Rmd
## 57         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/amclever/CleveringaAlex.Rmd
## 58         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/amclever/CleveringaAlex.Rmd
## 59         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/amclever/CleveringaAlex.Rmd
## 60         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/amclever/CleveringaAlex.Rmd
## 61                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/amclever/README.Rmd
## 62                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/amclever/README.Rmd
## 63         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/avcoll16/CollinsAbigail.Rmd
## 64         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/avcoll16/CollinsAbigail.Rmd
## 65         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/avcoll16/CollinsAbigail.Rmd
## 66         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/avcoll16/CollinsAbigail.Rmd
## 67         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/avcoll16/CollinsAbigail.Rmd
## 68                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/avcoll16/README.Rmd
## 69                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/avcoll16/README.Rmd
## 70              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Bufei2022/GuoBufei.Rmd
## 71              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Bufei2022/GuoBufei.Rmd
## 72              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Bufei2022/GuoBufei.Rmd
## 73              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Bufei2022/GuoBufei.Rmd
## 74              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Bufei2022/GuoBufei.Rmd
## 75                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Bufei2022/README.Rmd
## 76                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Bufei2022/README.Rmd
## 77        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/cerdengithub/ErdenCoskun.Rmd
## 78        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/cerdengithub/ErdenCoskun.Rmd
## 79        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/cerdengithub/ErdenCoskun.Rmd
## 80        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/cerdengithub/ErdenCoskun.Rmd
## 81  /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/cerdengithub/LastnameFirstname.Rmd
## 82             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/cerdengithub/README.Rmd
## 83             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/cerdengithub/README.Rmd
## 84  /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/danyangzhang/LastnameFirstname.Rmd
## 85             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/danyangzhang/README.Rmd
## 86             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/danyangzhang/README.Rmd
## 87       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/danyangzhang/ZhangDanyang.Rmd
## 88       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/danyangzhang/ZhangDanyang.Rmd
## 89       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/danyangzhang/ZhangDanyang.Rmd
## 90              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/eshitazaman/README.Rmd
## 91              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/eshitazaman/README.Rmd
## 92         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/eshitazaman/ZamanEshita.Rmd
## 93         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/eshitazaman/ZamanEshita.Rmd
## 94         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/eshitazaman/ZamanEshita.Rmd
## 95               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Ghazal2371/README.Rmd
## 96               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Ghazal2371/README.Rmd
## 97      /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Ghazal2371/ShahabadiGhazal.Rmd
## 98       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/glcoll16/CollinsGabrielle.Rmd
## 99       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/glcoll16/CollinsGabrielle.Rmd
## 100                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/glcoll16/README.Rmd
## 101                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/glcoll16/README.Rmd
## 102            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/JinjiPang/PangJinji.Rmd
## 103            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/JinjiPang/PangJinji.Rmd
## 104            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/JinjiPang/PangJinji.Rmd
## 105               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/JinjiPang/README.Rmd
## 106               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/JinjiPang/README.Rmd
## 107          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/kieran41/LimingKieran.Rmd
## 108          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/kieran41/LimingKieran.Rmd
## 109          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/kieran41/LimingKieran.Rmd
## 110          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/kieran41/LimingKieran.Rmd
## 111                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/kieran41/README.Rmd
## 112                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/kieran41/README.Rmd
## 113            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/m-fili/FiliMohammad.Rmd
## 114            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/m-fili/FiliMohammad.Rmd
## 115            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/m-fili/FiliMohammad.Rmd
## 116                  /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/m-fili/README.Rmd
## 117                  /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/m-fili/README.Rmd
## 118        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/PariisAk/AkbariParastoo.Rmd
## 119                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/PariisAk/README.Rmd
## 120                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/PariisAk/README.Rmd
## 121      /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/rcast1215/CastanedaRobert.Rmd
## 122               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/rcast1215/README.Rmd
## 123               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/rcast1215/README.Rmd
## 124       /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Saqlainrocks7/AliSaqlain.Rmd
## 125           /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Saqlainrocks7/README.Rmd
## 126           /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/Saqlainrocks7/README.Rmd
## 127     /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/willju-wangqian/JuWangqian.Rmd
## 128     /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/willju-wangqian/JuWangqian.Rmd
## 129     /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/willju-wangqian/JuWangqian.Rmd
## 130     /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/willju-wangqian/JuWangqian.Rmd
## 131     /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/willju-wangqian/JuWangqian.Rmd
## 132         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/willju-wangqian/README.Rmd
## 133         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/willju-wangqian/README.Rmd
## 134          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/QuanLin.Rmd
## 135          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/QuanLin.Rmd
## 136          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/QuanLin.Rmd
## 137          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/QuanLin.Rmd
## 138          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/QuanLin.Rmd
## 139          /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/QuanLin.Rmd
## 140     /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/R/ply-iterator.r
## 141     /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/R/ply-iterator.r
## 142         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/R/ply-list.r
## 143         /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/R/progress.r
## 144            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/R/rbind.r
## 145 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/R/split-data-frame.r
## 146           /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/README.Rmd
## 147           /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xiaolinzi1112/README.Rmd
## 148                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xlanwan/README.Rmd
## 149                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xlanwan/README.Rmd
## 150             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xlanwan/WanXiaolan.Rmd
## 151             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xlanwan/WanXiaolan.Rmd
## 152             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/xlanwan/WanXiaolan.Rmd
## 153            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YuhangTom/LinYuhang.Rmd
## 154            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YuhangTom/LinYuhang.Rmd
## 155            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YuhangTom/LinYuhang.Rmd
## 156            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YuhangTom/LinYuhang.Rmd
## 157               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YuhangTom/README.Rmd
## 158               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YuhangTom/README.Rmd
## 159              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YunhuiQi/QiYunhui.Rmd
## 160              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YunhuiQi/QiYunhui.Rmd
## 161              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YunhuiQi/QiYunhui.Rmd
## 162                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YunhuiQi/README.Rmd
## 163                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/YunhuiQi/README.Rmd
## 164            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zhiliqiao/QiaoZhili.Rmd
## 165            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zhiliqiao/QiaoZhili.Rmd
## 166            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zhiliqiao/QiaoZhili.Rmd
## 167            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zhiliqiao/QiaoZhili.Rmd
## 168            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zhiliqiao/QiaoZhili.Rmd
## 169            /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zhiliqiao/QiaoZhili.Rmd
## 170               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zhiliqiao/README.Rmd
## 171               /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zhiliqiao/README.Rmd
## 172                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zzhou93/README.Rmd
## 173                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zzhou93/README.Rmd
## 174              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zzhou93/ZhouZirou.Rmd
## 175              /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-16-2022-12-13-44/zzhou93/ZhouZirou.Rmd
## 176        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/aadokwei/AbrahamAdokwei.Rmd
## 177                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/aadokwei/README.Rmd
## 178                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/aadokwei/README.Rmd
## 179        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/amclever/CleveringaAlex.Rmd
## 180        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/amclever/CleveringaAlex.Rmd
## 181        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/amclever/CleveringaAlex.Rmd
## 182        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/amclever/CleveringaAlex.Rmd
## 183                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/amclever/README.Rmd
## 184                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/amclever/README.Rmd
## 185        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/CollinsAbigail.Rmd
## 186        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/CollinsAbigail.Rmd
## 187        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/CollinsAbigail.Rmd
## 188        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/CollinsAbigail.Rmd
## 189        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/CollinsAbigail.Rmd
## 190        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/CollinsAbigail.Rmd
## 191        /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/CollinsAbigail.Rmd
## 192                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/README.Rmd
## 193                /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/README.Rmd
## 194                 /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/avcoll16/renv.lock
## 195             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/Bufei2022/GuoBufei.Rmd
## 196             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/Bufei2022/GuoBufei.Rmd
## 197             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/Bufei2022/GuoBufei.Rmd
## 198             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/Bufei2022/GuoBufei.Rmd
## 199             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/Bufei2022/GuoBufei.Rmd
## 200             /Users/hofmann/Documents/Teaching/Stat 585/Spring 2022/blogs/Blog #3-02-22-2022-10-09-17/Bufei2022/GuoBufei.Rmd
##       Package Require Version   Dev
## 1   rmarkdown                 FALSE
## 2   rmarkdown                 FALSE
## 3   rmarkdown                 FALSE
## 4   rmarkdown                 FALSE
## 5   rmarkdown                 FALSE
## 6   rmarkdown                 FALSE
## 7   rmarkdown                 FALSE
## 8   rmarkdown                 FALSE
## 9   rmarkdown                 FALSE
## 10  rmarkdown                 FALSE
## 11  rmarkdown                 FALSE
## 12  rmarkdown                 FALSE
## 13  rmarkdown                 FALSE
## 14  rmarkdown                 FALSE
## 15  rmarkdown                 FALSE
## 16  rmarkdown                 FALSE
## 17  rmarkdown                 FALSE
## 18  rmarkdown                 FALSE
## 19  rmarkdown                 FALSE
## 20  rmarkdown                 FALSE
## 21  rmarkdown                 FALSE
## 22  rmarkdown                 FALSE
## 23  rmarkdown                 FALSE
## 24  rmarkdown                 FALSE
## 25  rmarkdown                 FALSE
## 26  tidyverse                 FALSE
## 27  rmarkdown                 FALSE
## 28  rmarkdown                 FALSE
## 29  rmarkdown                 FALSE
## 30  rmarkdown                 FALSE
## 31  rmarkdown                 FALSE
## 32  rmarkdown                 FALSE
## 33  rmarkdown                 FALSE
## 34  rmarkdown                 FALSE
## 35  rmarkdown                 FALSE
## 36  rmarkdown                 FALSE
## 37  rmarkdown                 FALSE
## 38  rmarkdown                 FALSE
## 39  rmarkdown                 FALSE
## 40  rmarkdown                 FALSE
## 41  rmarkdown                 FALSE
## 42  rmarkdown                 FALSE
## 43  rmarkdown                 FALSE
## 44  rmarkdown                 FALSE
## 45  rmarkdown                 FALSE
## 46  rmarkdown                 FALSE
## 47  rmarkdown                 FALSE
## 48  rmarkdown                 FALSE
## 49  rmarkdown                 FALSE
## 50  rmarkdown                 FALSE
## 51  rmarkdown                 FALSE
## 52  rmarkdown                 FALSE
## 53  rmarkdown                 FALSE
## 54  rmarkdown                 FALSE
## 55  rmarkdown                 FALSE
## 56      knitr                 FALSE
## 57  rmarkdown                 FALSE
## 58      dplyr                 FALSE
## 59    ggplot2                 FALSE
## 60       plyr                 FALSE
## 61  rmarkdown                 FALSE
## 62      knitr                 FALSE
## 63  rmarkdown                 FALSE
## 64      dplyr                 FALSE
## 65    ggplot2                 FALSE
## 66       plyr                 FALSE
## 67      dplyr                 FALSE
## 68  rmarkdown                 FALSE
## 69      knitr                 FALSE
## 70  rmarkdown                 FALSE
## 71       plyr                 FALSE
## 72       plyr                 FALSE
## 73      dplyr                 FALSE
## 74       plyr                 FALSE
## 75  rmarkdown                 FALSE
## 76      knitr                 FALSE
## 77  rmarkdown                 FALSE
## 78      dplyr                 FALSE
## 79       plyr                 FALSE
## 80       plyr                 FALSE
## 81  rmarkdown                 FALSE
## 82  rmarkdown                 FALSE
## 83      knitr                 FALSE
## 84  rmarkdown                 FALSE
## 85  rmarkdown                 FALSE
## 86      knitr                 FALSE
## 87  rmarkdown                 FALSE
## 88      dplyr                 FALSE
## 89       plyr                 FALSE
## 90  rmarkdown                 FALSE
## 91      knitr                 FALSE
## 92  rmarkdown                 FALSE
## 93      dplyr                 FALSE
## 94       plyr                 FALSE
## 95  rmarkdown                 FALSE
## 96      knitr                 FALSE
## 97  rmarkdown                 FALSE
## 98  rmarkdown                 FALSE
## 99      dplyr                 FALSE
## 100 rmarkdown                 FALSE
## 101     knitr                 FALSE
## 102 rmarkdown                 FALSE
## 103     dplyr                 FALSE
## 104      plyr                 FALSE
## 105 rmarkdown                 FALSE
## 106     knitr                 FALSE
## 107 rmarkdown                 FALSE
## 108     dplyr                 FALSE
## 109      plyr                 FALSE
## 110      plyr                 FALSE
## 111 rmarkdown                 FALSE
## 112     knitr                 FALSE
## 113 rmarkdown                 FALSE
## 114     dplyr                 FALSE
## 115      plyr                 FALSE
## 116 rmarkdown                 FALSE
## 117     knitr                 FALSE
## 118 rmarkdown                 FALSE
## 119 rmarkdown                 FALSE
## 120     knitr                 FALSE
## 121 rmarkdown                 FALSE
## 122 rmarkdown                 FALSE
## 123     knitr                 FALSE
## 124 rmarkdown                 FALSE
## 125 rmarkdown                 FALSE
## 126     knitr                 FALSE
## 127 rmarkdown                 FALSE
## 128     dplyr                 FALSE
## 129      plyr                 FALSE
## 130      plyr                 FALSE
## 131     dplyr                 FALSE
## 132 rmarkdown                 FALSE
## 133     knitr                 FALSE
## 134 rmarkdown                 FALSE
## 135     knitr                 FALSE
## 136     dplyr                 FALSE
## 137      plyr                 FALSE
## 138     dplyr                 FALSE
## 139      plyr                 FALSE
## 140 iterators                 FALSE
## 141 itertools                 FALSE
## 142   foreach                 FALSE
## 143     tcltk                 FALSE
## 144      base                 FALSE
## 145      plyr                 FALSE
## 146 rmarkdown                 FALSE
## 147     knitr                 FALSE
## 148 rmarkdown                 FALSE
## 149     knitr                 FALSE
## 150 rmarkdown                 FALSE
## 151     dplyr                 FALSE
## 152      plyr                 FALSE
## 153 rmarkdown                 FALSE
## 154     dplyr                 FALSE
## 155      plyr                 FALSE
## 156     purrr                 FALSE
## 157 rmarkdown                 FALSE
## 158     knitr                 FALSE
## 159 rmarkdown                 FALSE
## 160      plyr                 FALSE
## 161 tidyverse                 FALSE
## 162 rmarkdown                 FALSE
## 163     knitr                 FALSE
## 164 rmarkdown                 FALSE
## 165     dplyr                 FALSE
## 166      plyr                 FALSE
## 167     dplyr                 FALSE
## 168      plyr                 FALSE
## 169      plyr                 FALSE
## 170 rmarkdown                 FALSE
## 171     knitr                 FALSE
## 172 rmarkdown                 FALSE
## 173     knitr                 FALSE
## 174 rmarkdown                 FALSE
## 175     dplyr                 FALSE
## 176 rmarkdown                 FALSE
## 177 rmarkdown                 FALSE
## 178     knitr                 FALSE
## 179 rmarkdown                 FALSE
## 180     dplyr                 FALSE
## 181   ggplot2                 FALSE
## 182      plyr                 FALSE
## 183 rmarkdown                 FALSE
## 184     knitr                 FALSE
## 185 rmarkdown                 FALSE
## 186     dplyr                 FALSE
## 187   ggplot2                 FALSE
## 188      plyr                 FALSE
## 189      renv                 FALSE
## 190      renv                 FALSE
## 191     dplyr                 FALSE
## 192 rmarkdown                 FALSE
## 193     knitr                 FALSE
## 194      renv                 FALSE
## 195 rmarkdown                 FALSE
## 196      plyr                 FALSE
## 197      plyr                 FALSE
## 198     dplyr                 FALSE
## 199      renv                 FALSE
## 200      plyr                 FALSE
##  [ reached 'max' / getOption("max.print") -- omitted 468 rows ]
```


4. **Add the `renv` folder to your blog 3 repository, and push the changes.**

5. **Is the github action working? Read any potential error messages in the workflow and try to fix things. Make sure to check stackoverflow for help, don't forget our forum!**


Write a blog post addressing the following questions: 

1. **What is the idea of the renv package?**

It looks like renv tries to document the dependencies of the packages used and installed on an R project. It helps manage your packages' dependencies, which can help save us from issues like the ones we saw on Blog 3.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
 

Most of the trouble I had with Renv was dealing with updating Blog 3. It appears to almost be working, however I am having trouble with some individual packages.

Submit this blog post to the blog-5 repo. 
