FROM docker.io/ubuntu:24.04

LABEL devops.grababyte.image.authors="GrabAByte"

ARG USER=ubuntu24
ENV ID=1001

RUN \
  apt-get update -y && \
  apt-get install --no-install-recommends -y \
    curl \
    gcc \
    git \
    gnupg \
    jq \
    lsb-release \
    nodejs \
    npm \
    openssh-server \
    python3-full \
    python3-setuptools \
    python3-pip \
    python3-yaml \
    pipx \
    ruby \
    sshpass \
    sudo \
    tar \
    unzip \
    zip && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* && \
  groupadd -g "${ID}" "${USER}" && \
  useradd -l -m -u "${ID}" -g "${USER}" "${USER}" && \
  echo "${USER} ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER "${USER}"
