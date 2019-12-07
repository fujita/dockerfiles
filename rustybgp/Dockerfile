FROM rust

ENV HOME /root
WORKDIR /root

RUN curl -OL https://github.com/osrg/gobgp/releases/download/v2.11.0/gobgp_2.11.0_linux_amd64.tar.gz && tar xzf gobgp_2.11.0_linux_amd64.tar.gz && cp gobgp gobgpd /usr/sbin && rm gobgp_2.11.0_linux_amd64.tar.gz

RUN rustup component add rustfmt
RUN git clone https://github.com/osrg/rustybgp.git && cd rustybgp && cargo build --release


