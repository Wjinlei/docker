- 构建镜像
```
sudo docker build --rm --no-cache -t my/centos7 .
```
- 运行镜像
```
sudo docker run --rm -it --name centos7 my/centos7 
```
