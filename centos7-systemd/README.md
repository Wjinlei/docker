### 构建支持systemd的镜像Centos镜像
- 先构建base目录中支持systemd的centos镜像
- 再基于其构建镜像
```
sudo docker build --rm --no-cache -t my/centos7 .
```
- 运行镜像
```
sudo docker run --privileged  --rm -it --name centos7 -v /sys/fs/cgroup:/sys/fs/cgroup:ro my/centos7 
```
