FROM golang
LABEL maintainer "FUJITA Tomonori <fujita.tomonori@gmail.com>"

ENV HOME /root
WORKDIR /root
ENV GO111MODULE on

RUN git clone git://github.com/osrg/gobgp
RUN cd gobgp && go install ./cmd/gobgpd ./cmd/gobgp
