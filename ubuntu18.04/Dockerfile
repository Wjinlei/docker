FROM ubuntu:18.04

ENV DEBIAN_FRONTEND noninteractive
RUN cp -a /etc/apt/sources.list /etc/apt/sources.list.bak
RUN sed -i "s@http://.*archive.ubuntu.com@http://repo.huaweicloud.com@g" /etc/apt/sources.list
RUN sed -i "s@http://.*security.ubuntu.com@http://repo.huaweicloud.com@g" /etc/apt/sources.list
RUN apt-get update
RUN apt-get --assume-yes install apt-utils dialog
Run apt-get --assume-yes install gcc g++ make cmake
RUN apt-get --assume-yes install iproute2 net-tools
Run apt-get --assume-yes install wget curl vim
RUN apt-get clean
