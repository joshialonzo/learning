---
layout: default
title: Create a Docker image
email: joshi.alonzo@gmail.com
category: docker
---

<div class="alert alert-warning" role="alert">
  Note: Code beginning with $ (dollar sign) implies a terminal command.
</div>

##### 1. We first pull a minimal version of linux:

<kbd>
  $ docker pull alpine
</kbd>

##### 2. We see the list of images:

<kbd>
  $ docker image ls
</kbd>

##### 2. Create a container from the downloaded image:

<kbd>
  $ docker run -it --name minimal alpine /bin/sh
</kbd>



#### References
* [Docker community documentation](https://www.docker.com/docker-community)
* [Here we can find more Docker images maintained by Docker](https://hub.docker.com/explore/)
