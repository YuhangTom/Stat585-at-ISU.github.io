---
author: "Yunhui Qi"
title: "Use renv to fix github actions"
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

3. **Add all dependencies to the environment (implicitly by installing all the depepndencies or explicilty by listing dependencies in a DESCRIPTION file).**

4. **Add the `renv` folder to your blog 3 repository, and push the changes.**

5. **Is the github action working? Read any potential error messages in the workflow and try to fix things. Make sure to check stackoverflow for help, don't forget our forum!**


Write a blog post addressing the following questions: 

1. **What is the idea of the renv package?**

I think renv is used to get some snapshot of the R environment including the packages and dependencies used in one project and save this snapshot as a separate file renv.lock. Once we run the project on github or other platforms, the renv.lock file will help recover the original R environment to avoid some package errors. 

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
 
I firstly opened blog3 project and remove the plyr and tidyverse packages, libraried renv, and it just gave some welcome message which is very user friendly, I then ran renv::init() to initialize the renv.lock file. I then installed the packages plyr and tidyverse, renv gave me the OK message for each installation. And I ran renv::snapshot() to record the environment. At last, I pushed all the files to the github.

I got the first error: installing curl wrong for some odd reason. So I opened the renv.lock file, there were tidyverse, curl packages. Dr. Hofmann said no need for curl and tidyverse, just dplyr. So I deleted curl and tidyverse chunk in the renv.lock file. And pushed the change to the github. Then it works.

In summary, renv is really easy to use and reliable. Github action is difficult to deal with. I would say if I need to run the rmd on github, I would like to use renv to avoid unnecessary difficulty. 



