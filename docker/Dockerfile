FROM docker.io/ubuntu:23.04

LABEL devops.grababyte.image.authors="GrabAByte"

RUN \
  apt-get update -y && \
  apt-get install --no-install-recommends -y \
    gcc \
    curl \
    git \
    jq \
    openssh-server \
    python3-dev \
    python3-setuptools \
    python3-pip \
    python3-yaml \
    sshpass \
    sudo \
    tar \
    unzip \
    zip && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*
