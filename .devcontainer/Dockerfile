# syntax=docker/dockerfile:1
FROM ubuntu:22.04

LABEL maintainer="stefan_dan.ciocirlan@upb.ro"
LABEL version="0.1"
LABEL description="The open source toolchain qkd net simulator"

# for apt-get
# https://serverfault.com/questions/949991/how-to-install-tzdata-on-a-ubuntu-docker-image
ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Europe/Bucharest

# Update Ubuntu Software repository
# https://stackoverflow.com/questions/39760663/docker-ubuntu-bin-sh-1-locale-gen-not-found
# https://askubuntu.com/questions/162391/how-do-i-fix-my-locale-issue/229512#229512
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y locales && \
    locale-gen "en_US.UTF-8" && \
    dpkg-reconfigure locales

# install basic tools
RUN apt-get install -y curl sudo zip unzip wget git make gcc g++ nano

# install python3 and pip3
RUN apt-get install -y python3 python3-pip

RUN apt-get install -y g++ python3 cmake ninja-build git

RUN apt-get install -y ccache

RUN apt-get install -y gir1.2-goocanvas-2.0 python3-gi python3-gi-cairo python3-pygraphviz gir1.2-gtk-3.0 ipython3  

RUN apt-get install -y python3-setuptools git

RUN apt-get install -y qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools

RUN apt-get install -y openmpi-bin openmpi-common openmpi-doc libopenmpi-dev

RUN apt-get install -y mercurial unzip

RUN apt-get install -y gdb valgrind 

RUN apt-get install -y clang-format

RUN apt-get install -y tcpdump

RUN apt-get install -y sqlite sqlite3 libsqlite3-dev

RUN apt-get install -y libxml2 libxml2-dev

RUN apt-get install -y cmake libc6-dev libc6-dev-i386 libclang-dev llvm-dev automake python3-pip

RUN apt-get install -y libgtk-3-dev

RUN apt-get install -y vtun lxc uml-utilities

RUN apt-get install -y libxml2 libxml2-dev libboost-all-dev

RUN apt-get install -y libcrypto++-dev libcrypto++-doc libcrypto++-utils gnuplot uuid-dev

RUN python3 -m pip install --user cppyy
RUN python3 -m pip install --user cxxfilt

