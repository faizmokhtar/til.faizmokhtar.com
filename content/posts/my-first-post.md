---
title: "#1: How to clone git repository with submodules"
date: 2020-08-13T22:39:49+08:00
draft: true
tags:
  - git
comments: true
---
Today I learned how to git clone a repository that has [git submodules][1] inside of it. I realized that when I cloned a project it will clone the parent repo but the submodules will be empty. Here are the steps on how to clone it properly.

If I haven't cloned the project yet, I can use `--recurse-submodules` option:

````
$ git clone --recurse-submodules https://github.com/sample/sample-repo.git
````

Otherwise, If I already cloned the project I can use the following options:

````
git submodule update --init --recursive
````

This will initialize, fetch and checkout any nested submodules. That's it.

\[1]: <https://git-scm.com/book/en/v2/Git-Tools-Submodules>