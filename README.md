# 我的一些Dockerfile
- 它们可能不适用于你

# Docker 简单使用命令
- 拉取镜像
```shell
sudo docker pull centos:7
```

- 查看镜像
```shell
sudo docker images
```

- 删除镜像
```shell
#sudo docker rmi 镜像id或名字
sudo docker rmi 442fd76b9077
```

- 查看容器
```shell
sudo docker ps    # 查看运行中的容器
sudo docker ps -a # 查看所有容器
```

- 删除容器
```shell
#sudo docker rm 容器id或名字
sudo docker rm centos7
```

- 运行容器
```shell
# sudo docker run --rm -it --name 容器名字 -v /home/w/my.codes:/root/my.codes 镜像名字
# --rm 退出容器后删除该容器
# --it 附加到容器(这个不用管,反正你要进入容器加上-it即可)
# --name 容器名字
# -v 映射本地目录到容器
sudo docker run --rm -it --name centos7 -v /home/w/my.codes:/root/my.codes my/centos7
```
