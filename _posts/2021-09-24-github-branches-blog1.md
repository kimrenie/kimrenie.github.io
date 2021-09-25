---
layout: post
title:  "1. Github Branches"
date:   2021-09-24 01:00:00 -0700
categories: jekyll update
---
<html><head><link rel="stylesheet" type="text/css" href="./style2.css"></head></html>

#  Github Branches

Git and Github have features that allow the user to control which version of their code is used when publishing your work. This version control is managed through the usage of different `branches`. Repositories are able to host multiple branches in order to save different versions of code such as updates or features that can be deployed in the future. The code in these branches are essentially held in limbo until a `git push` is performed to integrate it with the main code. 

This main version of code is the Git's *default branch* which referred to as the `main branch` or the `master branch`. This branch is not meant to be directly altered because it needs to be stable enough to deploy your projects without issues. Creating additional branches allows edits to be safely added to the main branch and its code. 

# New Branches

A `branch` can be seen as a develper's specific workflow, this allows Git to point to new commits. (A secondary concept to branches would be `forking` and `Git remotes`. I will have to research that later on tbh.) This pointer system does not change the repository's history but rather allows the main branch to keep track of changes. 
> **Note:** Viewing a branch as a pointer is a fundamental concept when using Git.

Once added as collaborators to a repository, different developers use branches in order to keep all of the project's work/progress accessible and allows all of the collaborators to push to the same place.The image below shows different branches are able to hold upcoming features and updates that are able to be easily pushed and deployed to the main branch.

![a Github branch workflow](/images/branch-workflow.png)

>**Note:** Creating new branches can only happen in your local repository. Doing this in a remote repository requires a more in depth understanding of branches. 

# How to Create a Branch

Below is a list of commands that a developer often uses in order to create, modify, and switch to different branch workflows.

| Code Snippet | What it Does | 
| --- | --- |
| $ git branch | Displays the branches associated with the current repository |
| $ git branch -a | Displayes the remote branches |
| $ git branch <-new-branch-name-> | Creates a new branch, without checking out|
| $ git branch -m <-branch-name-> | Renames the current branch |
| $ git branch -d <-new-branch-name-> | Deletes your branch (safely*) |
| $ git branch -D < branch-name > | Force delete a branch and its commits |

Some of this code can be visually seen as follows:

![terminal view of above commands](/images/branch-checkout.png)

# Git Checkout

The `$ git checkout` command enables the user to switch between and navigate around branches that were created with `$ git branch`. In other words, using this command allows the user to switch between different versions of the code thats available on their local system's repository.

> **Note:** In order for the `$ git checkout` command to work, the following entities must be used properly: `files`, `commits`, and `branches`.

After performing a `git checkout`, Git updates the files in the working directory to match the associated version and record the branch's new commits.