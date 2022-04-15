---
author: "Bufei Guo"
title: "Blog 5: Fixing github actions"
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

renv package helps manage library paths to help isolate project's R dependencies from other R library on one's system. It allows to initialize a new project-local environment (`renv::init`) or save the state of the project library to the lockfile (`renv::snapshot`) and revert to the previous state (`renv::restore`). Thus it helps to make sure that the working environment is consistent, especially when working with collaborators, i.e. one user initialize renv in the project and share project resources, when collaborator first launches the project, the can use `renv::restore` to restore the project library locally.

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
 
When I was doing my blog 3, I need to install both `plyr` and `dplyr` packages and specify the repo to install from in Rmd file, i.e. using command `install.packages("plyr",repos = "http://cran.us.r-project.org")`, before use the `library` command. Otherwise, github will give me an error message saying `there is no package called 'dplyr'`.

When use renv, I first initialize the workflow using `renv::init` on my local computer then call `plyr` and `dplyr` libraries as I need. After that push the changes as well as the renv folder the my blog 3 repository. Then I found out that I do not need to manually install the `plyr` or `dplyr` package to make my github actions pass. (I can remove the command line `install.packages("plyr",repos = "http://cran.us.r-project.org")` and still get my final result compiled, which can be seen in my Actions history. I added back this line of code at last to make my blog3 Rmd file unchanged)

I have one issue that I am able to solve when using renv files. When I clone my repo to my local machine and then push the changes I made back to my repo. This works fine the first time I push my changes. At the second time I want to push my changes, it will give me an error message saying *error: failed to push some refs to 'https://github.com/Stat585-at-ISU/blog-3-Bufei2022.git'* and give some hint like *Integrate the remote changes before pushing again.* The problem is that I can not pull from my repo either, it will give me a warning like **Pulling without specifying how to reconcile divergent branches is discouraged*. Stack overflow gives suggestions like configure git client to always `--ff-only` by typing `git config --global pull.ff only` in the terminal. This action can not solve the problem either, only the error message changes to *fatal: Not possible to fast-forward, aborting.*

Submit this blog post to the blog-5 repo. 

