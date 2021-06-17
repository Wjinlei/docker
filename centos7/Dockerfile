FROM centos:7

RUN cp -a /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.bak 
RUN sed -i "s/#baseurl/baseurl/g" /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i "s/mirrorlist=http/#mirrorlist=http/g" /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i "s@http://mirror.centos.org@https://repo.huaweicloud.com@g" /etc/yum.repos.d/CentOS-Base.repo
RUN yum clean all; yum makecache
RUN yum install -y iproute net-tools wget curl vim rpm-build gcc g++ make cmake;
RUN yum clean all;
