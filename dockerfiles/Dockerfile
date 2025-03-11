FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl git gcc g++ make 

RUN apt-get update && apt-get install -y libisal-dev libdeflate-dev

RUN curl -LO https://github.com/OpenGene/fastp/archive/refs/tags/v0.24.0.tar.gz && \
    tar -zxvf v0.24.0.tar.gz && cd /root/fastp-0.24.0/ && \
    make && make install

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=fastp
