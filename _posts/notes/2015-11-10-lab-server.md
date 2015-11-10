---
layout: post
title:  Troy University Lab Server Config
catgories: 
---

Ip Address

-  10.33.0.31

Docker Command:

- docker images: List all the images
- docker ps：List all the containers which are running now
- docker ps -a: List all the containters include not running
- docker run -i -t ubuntu /bin/bash: run ubuntu image
- docker restart master: restart container with default command
- docker commit 3a09b2588478 ubuntu:mynewimage：git commit
- docker run -ti -h master ubuntu
- docker run -d --name master -h master ubuntu /etc/init.d/ssh start -D
- docker inspect master grep IP
- docker pull ubuntu: download all the Linux server
