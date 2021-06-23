- 构建镜像
```
sudo docker build --rm --no-cache -t my/ubuntu18.04 .
```
- 运行镜像
```
sudo docker run --rm -it --name ubuntu18.04 my/ubuntu18.04
```
