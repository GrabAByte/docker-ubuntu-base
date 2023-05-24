FROM docker.io/ubuntu:23.10

LABEL devops.grababyte.image.authors="GrabAByte"

ARG USER=ubuntu23
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
    python3-dev \
    python3-setuptools \
    python3-pip \
    python3-yaml \
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

RUN \
    pip3 install --no-cache-dir --upgrade \
      pip==23.1.2 \
      setuptools==67.8.0
