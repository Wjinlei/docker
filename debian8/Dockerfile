FROM debian:8

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get --assume-yes install apt-transport-https ca-certificates
RUN cp -a /etc/apt/sources.list /etc/apt/sources.list.bak
RUN sed -i "s@http://deb.debian.org@https://repo.huaweicloud.com@g" /etc/apt/sources.list
RUN sed -i "s@http://security.debian.org@https://repo.huaweicloud.com@g" /etc/apt/sources.list
RUN apt-get update
RUN apt-get --assume-yes install apt-utils dialog
Run apt-get --assume-yes install gcc g++ make cmake
RUN apt-get --assume-yes install iproute2 net-tools
Run apt-get --assume-yes install wget curl vim
RUN apt-get clean
