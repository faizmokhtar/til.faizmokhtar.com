---
title: "#3: What is the difference between Docker container and Docker image?"
date: 2020-08-25T07:54:01.914Z
categories:
  - ""
tags:
  - docker
comments: true
---
Today I learned the difference between **image** and **container** in Docker. An **image** is a template that can be used to create a container while **container** is the instances of said Docker images. The container is the one that runs your application.

To explain it in *cake* term, **image** is the recipe of the cake and **container** is the cake itself. You can create multiple cakes based on the same recipe.

To see all the images available, you can run the following:
```
$~ docker images
```

and to see the container that's currently running, you can run:
```
$~ docker ps
```

or if you want to see the list of available containers
```
$~ docker ps -a
```

That's it. 🎂