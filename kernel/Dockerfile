FROM ubuntu:14.04

WORKDIR /root/marshmallow-x86-kernel

ENV DEBIAN_FRONTEND noninteractive

RUN dpkg --add-architecture i386

# common x86 build requirements
RUN apt-get update && \
    apt-get install -y \
    build-essential \
    curl \
    git \
    g++-multilib \
    zlib1g:i386 \ 
    libxml2-utils \
    squashfs-tools \
    dosfstools \
    mtools \
    python \
    python-libxml2 \
    python-mako \
    bison \
    zip \
    unzip \ 
    bc \
    gperf \
    gettext \
    genisoimage \
    syslinux \
    libncurses5-dev \
    libncursesw5-dev


COPY marshmallow-x86-kernel /root/marshmallow-x86-kernel
COPY config/android-x86_64_defconfig  /root/marshmallow-x86-kernel/.config


