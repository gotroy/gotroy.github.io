---
layout: post
title:  Troy University Lab Server Config
catgories: 
---

Ip: 10.33.0.31

Docker Command:

- docker images：列出所有镜像(images)
- docker ps：列出正在运行的(容器)containers
- docker ps -a: 列出所有的容器，包括不运行的容器。
- docker pull ubuntu：下载镜像
- docker run -i -t ubuntu /bin/bash：运行ubuntu镜像
- docker restart master: 重启已经停止的container，但start不能够再指定容器启动时运行的指令，因为docker只能有一个前台进程。
- docker commit 3a09b2588478 ubuntu:mynewimage：提交你的变更，并且把容器保存成Tag为mynewimage的新的ubuntu镜像.(注意，这里提交只是提交到本地仓库，类似git)
- docker run -ti -h master ubuntu
- docker run -d --name master -h master ubuntu /etc/init.d/ssh start -D
- docker inspect master grep IP
