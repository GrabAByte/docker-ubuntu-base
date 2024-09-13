FROM docker.io/ubuntu:24.04

LABEL devops.grababyte.image.authors="GrabAByte"

ARG USER=ubuntu24
ENV ID=1001

RUN \
  apt-get update -y && \
  apt-get install --no-install-recommends -y \
    curl=8.5.0-2ubuntu10.3 \
    gcc=4:13.2.0-7ubuntu1 \
    git=1:2.43.0-1ubuntu7.1 \
    gnupg=2.4.4-2ubuntu17 \
    jq=1.7.1-3build1 \
    lsb-release=12.0-2 \
    nodejs=18.19.1+dfsg-6ubuntu5 \
    npm=9.2.0~ds1-2 \
    openssh-server=1:9.6p1-3ubuntu13.5 \
    python3-full=3.12.3-0ubuntu2 \
    python3-setuptools=68.1.2-2ubuntu1.1 \
    python3-pip=24.0+dfsg-1ubuntu1 \
    python3-yaml=6.0.1-2build2 \
    pipx=1.4.3-1 \
    ruby=1:3.2~ubuntu1 \
    software-properties-common=0.99.48 \
    sshpass=1.09-1 \
    sudo=1.9.15p5-3ubuntu5 \
    tar=1.35+dfsg-3build1 \
    unzip=6.0-28ubuntu4 \
    zip=3.0-13build1 && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* && \
  groupadd -g "${ID}" "${USER}" && \
  useradd -l -m -u "${ID}" -g "${USER}" "${USER}" && \
  echo "${USER} ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER "${USER}"
