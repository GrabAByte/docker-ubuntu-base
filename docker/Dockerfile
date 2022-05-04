FROM docker.io/ubuntu:22.04

LABEL devops.grababyte.image.authors="GrabAByte"

RUN \
  apt-get update -y && \
  apt-get install --no-install-recommends -y \
    gcc \
    curl \
    git \
    jq \
    openssh-server \
    sshpass \
    sudo \
    tar \
    unzip \
    zip
