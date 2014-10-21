# This dockerfile uses the ubuntu 14.04 image
# VERSION 1 - EDITION 1
# Author: philomuzzi

FROM ubuntu:14.04
MAINTAINER philomuzzi

RUN echo "deb http://shadowsocks.org/debian wheezy main" >> /etc/apt/sources.list
RUN apt-get -qq update
RUN apt-get -qqy --force-yes install shadowsocks

ADD local.conf /etc/sysctl.d/local.conf
RUN sysctl --system
RUN ulimit -n 51200

ENTRYPOINT ["/usr/bin/ss-server"]