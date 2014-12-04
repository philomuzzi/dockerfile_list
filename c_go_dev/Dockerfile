# This dockerfile uses the ubuntu 14.04 image
# VERSION 1 - EDITION 4
# Author: philomuzzi
# 一个最简单的基于ubuntu 的C系语言和Go语言的开发和调试环境。包含Git和Vim

FROM ubuntu:14.04

MAINTAINER philomuzzi

RUN apt-get -qq update
RUN apt-get install -qqy build-essential gdb git golang vim ctags cscope
RUN mkdir /usr/gopath
ENV GOPATH /usr/gopath

COPY .vimrc /root/

RUN mkdir ~/.vim && mkdir ~/.vim/bundle
RUN git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
RUN vim +PluginInstall +qall
