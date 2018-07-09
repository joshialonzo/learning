---
layout: default
title: Some Docker commands
email: joshi.alonzo@gmail.com
category: docker
---

<div class="alert alert-warning" role="alert">
  Note: Code beginning with $ (dollar sign) implies a terminal command.
</div>

##### 1. Download and install Docker for Mac or Linux. It is very easy. Look for tutorials on YouTube.

##### 2. How to see Docker version.

<kbd>
  $ docker version
</kbd>

##### 3. How to retrieve an ubuntu image from a web repository.

The default tag is the latest version.

<kbd>
  $ docker pull ubuntu
</kbd>

This is the same as:

<kbd>
  $ docker pull ubuntu:latest
</kbd>

Other options are:

<kbd>
  $ docker pull ubuntu:17.10
</kbd>

<kbd>
  $ docker pull ubuntu:latest-1
</kbd>

<kbd>
  $ docker pull ubuntu:nginx
</kbd>

##### 4. In order to create a container out of an image.

-i: interactive
-t: terminal

<kbd>
  $ docker run -it ubuntu:latest /bin/bash
</kbd>

##### 5. We can see the information about the SO release.

<kbd>
  $ cat /etc/os-release
</kbd>

##### 6. We can see the processes that are running on the OS.

<kbd>
  $ ps -ef
</kbd>

##### 7. If we want to get out of the docker container without killing it:

<kbd>
  CTRL + P + Q
</kbd>

##### 8. If we want to see the container status:

<kbd>
  $ docker container ls
</kbd>

##### 9. If we want to return to the alive container:

-i: interactive
-t: terminal

<kbd>
  $ docker container exec -it <container_id> /bin/bash
</kbd>

##### 10. If we need to stop a container:

<kbd>
  $ docker stop <container_id>
</kbd>

<container_id> can be founded by running:

<kbd> $ ps -ef </kbd>

##### 10. If we need to start a container:

<kbd>
  $ docker start <container_id>
</kbd>

<container_id> can be founded by running:

<kbd>
  $ ps -ef
</kbd>

##### 11. How to delete a container:

<kbd>
  $ docker container rm <container_id>
</kbd>

<container_id> can be founded by running:

<kbd>
  $ ps -ef
</kbd>

##### 11. If we want to see the available images:

<kbd>
  $ docker image ls
</kbd>

##### 11. If we want to remove an image:

<kbd>
  $ docker image rm <image>
</kbd>

#### References
* [Docker community documentation](https://www.docker.com/docker-community)
* [Here we can find more Docker images maintained by Docker](https://hub.docker.com/explore/)
