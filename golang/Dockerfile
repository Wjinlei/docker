FROM centos:7

RUN cp -a /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.bak
RUN sed -i "s/#baseurl/baseurl/g" /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i "s/mirrorlist=http/#mirrorlist=http/g" /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i "s@http://mirror.centos.org@https://repo.huaweicloud.com@g" /etc/yum.repos.d/CentOS-Base.repo
RUN yum makecache
RUN yum install -y iproute wget curl vim gcc gcc-c++ make cmake
RUN yum clean all

RUN wget http://test.hws.com/wangjinlei/go1.16.5.linux-amd64.tar.gz && tar -zxf go1.16.5.linux-amd64.tar.gz -C /usr/local
RUN rm -f go1.16.5.linux-amd64.tar.gz

ENV GO111MODULE=on
ENV GOPROXY="https://goproxy.io,direct"
ENV GOROOT="/usr/local/go"
ENV GOPATH="$HOME/go"
ENV PATH="$GOPATH/bin:$GOROOT/bin:$PATH"

RUN go get -u github.com/gobuffalo/packr/packr
RUN go get -u github.com/gobuffalo/packr

