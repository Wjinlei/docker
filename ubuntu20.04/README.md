- 构建镜像
```
sudo docker build --rm --no-cache -t my/ubuntu20.04 .
```
- 运行镜像
```
sudo docker run --rm -it --name ubuntu20.04 my/ubuntu20.04
```
