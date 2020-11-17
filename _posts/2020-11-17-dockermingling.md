---
title: Docker常用命令
excerpt_separator: <!--more-->
category: docker
layout: article1
---



```
#0.搜索收藏数不⼩于10的镜像
docker search -s 10 名称
#1.下载镜像
docker pull 名称:tag
#2.查看下载的镜像
docker images;
123456
#3.查看正在运⾏的容器
docker ps
#4.查看所有容器
docker ps -a
#5.运⾏容器<!--more-->
docker start/restart 容器名称/id
#6.停⽌容器
docker stop 容器名称/id
#7.在使⽤ -d 参数时，容器启动后会进⼊后台。此时想要进⼊容器，可以通过以下指令进⼊
docker attach 容器名称/id #不推荐使⽤，因为退出时会导致容器的停⽌
docker exec -it 容器名称/id /bin/bash #在进⼊容器后可使⽤linux命令，退出使⽤exit
#8.导出
docker export 容器名称/id > 名称.tar
#9.导⼊，可以使⽤ docker import 从容器快照⽂件中再导⼊为镜像，以下实例将快照⽂件指定
路径的tar 导⼊到镜像 test/test:v1:
cat tar路径 | docker import - test/test:v1
#也可以通过指定 URL 或者某个⽬录来导⼊
docker import http://example.com/exampleimage.tgz example/imagerepo
#10.删除容器
docker rm -f 容器名称/id
```

