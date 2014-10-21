# This dockerfile uses the ubuntu 14.04 image
# VERSION 1 - EDITION 1
# Author: philomuzzi

FROM ubuntu:14.04
MAINTAINER philomuzzi

RUN echo "deb http://shadowsocks.org/debian wheezy main" >> /etc/apt/sources.list
RUN apt-get -qq update
RUN apt-get -qqy --force-yes install shadowsocks

ADD local.conf /etc/sysctl.d/local.conf
#no allowed, but will load at system start time
#RUN sysctl --system
RUN echo "ulimit -n 51200" >> ~/.bashrc
RUN ["/bin/bash", "-c", "source ~/.bashrc"]

ENTRYPOINT ["usr/bin/ss-server"]
