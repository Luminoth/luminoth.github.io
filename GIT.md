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
