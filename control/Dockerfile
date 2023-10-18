FROM ubuntu:22.04
ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && \
  apt install -y gcc python3-dev libkrb5-dev apt-utils build-essential software-properties-common openssh-server sudo && \
  apt install python3-pip -y && \
  pip3 install --upgrade pip && \
  pip3 install --upgrade virtualenv && \
  pip3 install pywinrm[kerberos] && \
  apt install krb5-user -y && \ 
  pip3 install pywinrm && \
  pip3 install ansible && \
  apt clean     && \
  rm -Rf /var/lib/apt/lists/* && \
  rm -Rf /usr/share/doc && \
  rm -Rf /usr/share/man