---
author: "Alex Cleveringa"
title: "Blog 5: Revenge of Blog 3"
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
The idea of the renv package is to create an R environment inside the project that contains all of the packages and dependencies required for the code. This should allow shared code to be executed easier on different local computers. It also has a file that lists the versions of RStudio and all the packages used for documentation and to fulfill rule 3 of the rules for reproducible computational research we read about for Blog 4.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
 The two errors I got in GitHub the first time were "there is no package called 'ggplot2'" and "Process completed with exit code 1" in the render-rmarkdown.yaml. I entered the packages I was using in row 27 so that it said:

run: Rscript -e 'install.packages(c("rmarkdown", "ggplot2", "dplyr"))'

In the same attempt, I also activated the packages in the console before taking a snapshot with renv. I am not sure which of these two changes made the difference. If I wanted to, I could delete them from the .yaml file and see if I get the same warning message.

 

Submit this blog post to the blog-5 repo. 

