FROM ubuntu:22.04
RUN apt update && \
  apt install -y gcc python3-dev libkrb5-dev apt-utils build-essential software-properties-common openssh-server sudo python3-pip && \
  pip3 install --upgrade pip && \
  apt clean     && \
  rm -Rf /var/lib/apt/lists/* && \
  rm -Rf /usr/share/doc && \
  rm -Rf /usr/share/man
RUN useradd -rm -d /home/sshuser -s /bin/bash -g root -G sudo -u 1000 sshuser
RUN echo 'sshuser:password' | chpasswd
RUN service ssh start
EXPOSE 22