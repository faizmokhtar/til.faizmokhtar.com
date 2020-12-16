---
title: "#9 List all commits history for specific file with git"
date: 2020-12-16T02:24:09.782Z
categories:
  - git
tags:
  - git
comments: true
---
Assuming the given situation:

- You work on a large project that has an extensive git commits history and a lot of files
- You need to debug a certain issue that was caused by a certain file
- You need to know the commit history for that certain code in a certain file

Well, you're in luck. You can use the following `git log` command

````
$~ git log --follow -- path/to/file.txt
````

This will list down all the commits history for that specific file. It will work even if the file was deleted or renamed. However please be aware that it will only work for a single file at a time.
