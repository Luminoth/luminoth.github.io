---
layout: page
title: Git
permalink: /git/
---

# Git Cheatsheet

## Branches

* List all branches (remote and local)
  * `git branch -a`
* Create a branch
  * `git branch {branch name}`
  * `git checkout -b {branch name}`
    * Creates a branch and immediately checks it out
* Switch branches
  * `git checkout {branch name}`
* Destroy a remote branch
  * `git push -d {remote name} {branch name}`
* Destroy a local branch
  * `git branch -d {branch name}`
* Merge main branch into local branch
  * `git merge main`
* Rebase the local branch onto the main branch
  * `git rebase main`
  * Do *not* do this if other people are committing to the branch

## Submodules

* Add a submodule
  * `git submodule add {path to submodule repository}`
* Cloning with submodules
  * Clone the repository as normal
  * `git submodule init`
    * This only needs to be run once to initialize the submodule
  * `git submodule update`
    * This should be run any time a submodule needs updated
