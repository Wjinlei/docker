### 构建支持systemd的镜像Centos镜像
- Dockerfile
``` docker
FROM centos:7

ENV container docker
MAINTAINER The CentOS Project <cloud-ops@centos.org>

RUN (cd /lib/systemd/system/sysinit.target.wants/; for i in *; do [ $i == systemd-tmpfiles-setup.service ] || rm -f $i; done); \
rm -f /lib/systemd/system/multi-user.target.wants/*;\
rm -f /etc/systemd/system/*.wants/*;\
rm -f /lib/systemd/system/local-fs.target.wants/*; \
rm -f /lib/systemd/system/sockets.target.wants/*udev*; \
rm -f /lib/systemd/system/sockets.target.wants/*initctl*; \
rm -f /lib/systemd/system/basic.target.wants/*;\
rm -f /lib/systemd/system/anaconda.target.wants/*;

VOLUME [ "/sys/fs/cgroup" ]

CMD ["/usr/sbin/init"]
```
- 构建镜像
```
sudo docker build --rm --no-cache -t centos7/systemd .
```
- 运行镜像
```
sudo docker run --privileged  --rm -it --name centos7 -v /sys/fs/cgroup:/sys/fs/cgroup:ro centos7/systemd
```
