# This dockerfile uses the ubuntu 14.04 image
# VERSION 1 - EDITION 1
# Author: philomuzzi

FROM ubuntu:14.04
MAINTAINER philomuzzi

RUN echo "deb http://shadowsocks.org/debian wheezy main" >> /etc/apt/sources.list
RUN apt-get -qq update
RUN apt-get -qqy --force-yes install shadowsocks

ADD local.conf /etc/sysctl.d/local.conf
#docker system restrict, need add at readme
#RUN sysctl --system

ENTRYPOINT ["ulimit -n 51200 && /usr/bin/ss-server"]