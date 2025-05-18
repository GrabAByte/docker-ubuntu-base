FROM docker.io/ubuntu:25.10

LABEL devops.grababyte.image.authors="GrabAByte"

ARG USER=ubuntu24
ENV ID=1001

RUN \
  apt-get update -y && \
  apt-get install --no-install-recommends -y \
    curl=8.12.1-3ubuntu1 \
    gcc=4:14.2.0-1ubuntu1 \
    git=1:2.48.1-0ubuntu1 \
    gnupg=2.4.4-2ubuntu23 \
    jq=1.7.1-3ubuntu1 \
    lsb-release=12.1-1 \
    nodejs=20.18.1+dfsg-1ubuntu2 \
    npm=9.2.0~ds1-3 \
    openssh-server=1:9.9p1-3ubuntu3 \
    pipx=1.7.1-1 \
    python3-full=3.13.3-1 \
    python3-setuptools=75.8.0-1 \
    python3-pip=25.0+dfsg-1 \
    python3-yaml=6.0.2-1build2 \
    ruby=1:3.3~ubuntu3 \
    software-properties-common=0.111 \
    sshpass=1.10-0.1 \
    sudo=1.9.16p2-1ubuntu1 \
    tar=1.35+dfsg-3.1 \
    unzip=6.0-28ubuntu6 \
    zip=3.0-14ubuntu2 && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* && \
  groupadd -g "${ID}" "${USER}" && \
  useradd -l -m -u "${ID}" -g "${USER}" "${USER}" && \
  echo "${USER} ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER "${USER}"
