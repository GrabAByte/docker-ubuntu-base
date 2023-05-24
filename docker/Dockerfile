FROM docker.io/ubuntu:23.10

LABEL devops.grababyte.image.authors="GrabAByte"

ARG USER=ubuntu23
ENV ID=1001

RUN \
  apt-get update -y && \
  apt-get install --no-install-recommends -y \
    curl=7.88.1-9ubuntu1 \
    gcc=13.1.0-2ubuntu2 \
    git=1:2.39.2-1ubuntu1.1 \
    gnupg=2.2.40-1.1ubuntu1 \
    jq=1.6-2.1ubuntu3 \
    lsb-release=12.0-1ubuntu1 \
    nodejs=18.13.0+dfsg1-1ubuntu2 \
    npm=9.2.0~ds1-1 \
    openssh-server=1:9.0p1-1ubuntu8.1 \
    python3-full=3.11.2-1 \
    python3-setuptools=66.1.1-1 \
    python3-pip=23.1.2+dfsg-1 \
    python3-yaml=6.0-3build1 \
    pipx=1.2.0-1 \
    ruby=1:3.1 \
    sshpass=1.09-1 \
    sudo=1.9.13p1-1ubuntu2 \
    tar=6.1.13+~cs7.0.5-1 \
    unzip=6.0-27ubuntu1 \
    zip=3.0-13 && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* && \
  groupadd -g "${ID}" "${USER}" && \
  useradd -l -m -u "${ID}" -g "${USER}" "${USER}" && \
  echo "${USER} ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER "${USER}"
