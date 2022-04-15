---
author: "Abraham Adokwei"
title: "Experience with renv"
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
  - To my understanding, *renv* gives users the opportunity to keep track of every package (and its version) used in a scientific project. This is particularly because otherwise it'll be almost impossible to keep track of such smaller details. Additionally, *renv* attempts to make reproducibility achievable. This fulfills **Rule #3** of *Sandve et al.* reproducibility rules. 

2. **In 50 to 100 words describe your experience working with `renv`. What went well? What did not go so well?**
 
  - I would say my experience with *renv* as a first time user was a smooth one. The feedback given after running *init()* was very helpful and made things super straightforward. One thing that didn't make a lot of sense initially was the idea of "installing packages" that I had already installed. 

Submit this blog post to the blog-5 repo. 

