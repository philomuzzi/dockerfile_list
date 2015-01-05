# This dockerfile uses the ubuntu 14.04 image
# VERSION 1 - EDITION 1
# Author: philomuzzi
# 一个Rails开发环境，包含Git, Vim

FROM ubuntu:14.04

MAINTAINER philomuzzi

RUN apt-get -qq update
RUN apt-get install -qqy build-essential bison openssl libreadline6 libreadline6-dev curl gdb git vim ctags cscope openssh-server zlib1g zlib1g-dev libssl-dev libyaml-dev libsqlite3-0 libsqlite3-dev sqlite3 libxml2-dev libxslt-dev autoconf libc6-dev

COPY .vimrc /root/

RUN mkdir ~/.vim && mkdir ~/.vim/bundle
RUN git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
RUN vim +PluginInstall +qall

RUN wget http://cache.ruby-lang.org/pub/ruby/2.1/ruby-2.1.5.tar.gz && tar xvfz ruby-2.1.5.tar.gz
RUN cd ruby-2.1.5/ && ./configure && make && make install

RUN gem install rails