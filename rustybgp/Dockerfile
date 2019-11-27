FROM rust

ENV HOME /root
WORKDIR /root

RUN apt-get update
RUN apt-get install -qy --no-install-recommends supervisor cmake gcc

# go is necessary for build
RUN wget https://dl.google.com/go/go1.13.4.linux-amd64.tar.gz && tar -C /usr/local -xzf go1.13.4.linux-amd64.tar.gz && rm go1.13.4.linux-amd64.tar.gz
ENV PATH=$PATH:/usr/local/go/bin

RUN git clone https://github.com/osrg/rustybgp.git
RUN cd rustybgp && cargo build

