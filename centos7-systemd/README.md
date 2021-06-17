- 构建镜像
```
sudo docker build --rm --no-cache -t my/centos7 .
```
- 运行镜像
```
sudo docker run --privileged --rm -it --name centos7 -v /sys/fs/cgroup:/sys/fs/cgroup:ro my/centos7
```
