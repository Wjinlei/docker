FROM centos:8

RUN cp -a /etc/yum.repos.d/CentOS-Linux-BaseOS.repo /etc/yum.repos.d/CentOS-Linux-BaseOS.repo.bak 
RUN sed -i "s/#baseurl/baseurl/g" /etc/yum.repos.d/CentOS-Linux-BaseOS.repo
RUN sed -i "s/mirrorlist=http/#mirrorlist=http/g" /etc/yum.repos.d/CentOS-Linux-BaseOS.repo
RUN sed -i "s@http://mirror.centos.org@https://repo.huaweicloud.com@g" /etc/yum.repos.d/CentOS-Linux-BaseOS.repo
RUN yum clean all; yum makecache
RUN yum install -y iproute net-tools wget curl vim gcc gcc-c++ make cmake;
RUN yum install -y --nobest rpm-build
RUN yum clean all;
