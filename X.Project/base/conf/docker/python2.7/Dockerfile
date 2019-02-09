FROM ubuntu:16.04

# Install common package
RUN \
  apt-get update -y && \
  apt-get install -y \
    apt-transport-https \
    ca-certificates \
    software-properties-common \
    curl \
    wget

# Python
RUN \
  apt-get upgrade -y && \
  apt-get install -y \
    # Python 2.7
    python \
    python-pip

# upgrade pip
RUN \
  curl https://bootstrap.pypa.io/get-pip.py | python
