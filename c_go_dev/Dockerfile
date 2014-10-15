# This dockerfile uses the ubuntu 14.04 image
# VERSION 1 - EDITION 2
# Author: philomuzzi
# 一个最简单的基于ubuntu 的C系语言和Go语言的开发和调试环境。包含Git和Vim

FROM ubuntu:14.04

MAINTAINER philomuzzi gxlee1986@gmail.com

RUN apt-get -qq update
RUN apt-get install -qqy build-essential gdb git golang vim
RUN mkdir /usr/gopath
ENV GOPATH /usr/gopath

ADD ~/.vimrc ~/.vimrc