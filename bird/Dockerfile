FROM ubuntu:18.04
LABEL maintainer "FUJITA Tomonori <fujita.tomonori@gmail.com>"

ENV HOME /root
WORKDIR /root

RUN apt-get update && apt-get install -qy --no-install-recommends git build-essential automake autoconf libncurses-dev libreadline-dev flex bison ca-certificates

RUN git clone https://github.com/CZ-NIC/bird.git
RUN cd bird && autoreconf && ./configure && make && make install
