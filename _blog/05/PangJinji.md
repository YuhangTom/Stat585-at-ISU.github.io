---
author: "Jinji Pang"
title: "Fixing GitHub action errors using  package(renv)"
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

- In real life, we have multiple projects, each project uses some packages, those packages usually will have more new versions as time goes by, then it sometimes causes issues because some codes only work under specific package versions. We can use `renv`  to make our projects more isolated, which means each project gets its own *library* of **R**, and it also enables us to upgrade, download and change package versions in one project without worrying about breaking other projects. 


2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**

- The workflow of `renv` is really easy to follow, basically I just downloaded and loaded the package, and run `renv::init()` and `renv::snapshot`, then I was able to see renv folder and renv.lock in my project folder. 

- When I first pushed the modified project into GitHub, I still got error messages said "There is no package 'plyr'...". Then, I unloaded `tidverse` in my Rmd file and used `dplyr` instead, I also run `renv::snapshot` again, and pushed the modified project to GitHub in the end. This time it worked, no error messages. Therefore, I feel `renv` can help us solve the packages' version conflicts, but it may not be able to solve the conflicts between different packages automatically. We still need to debug by ourselves in some cases.





