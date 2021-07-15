- 构建镜像
```
sudo docker build --rm --no-cache -t my/debian8 .
```
- 运行镜像
```
sudo docker run --rm -it --name debian8 my/debian8
```
