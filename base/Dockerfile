FROM phusion/baseimage:0.9.16
MAINTAINER Binh Nguyen "binhnguyen@anduintransact.com"

# avoid interactive dialoges from apt:
ENV DEBIAN_FRONTEND noninteractive

RUN groupadd -r anduin && useradd -g anduin anduin

# install essential tools
RUN apt-get update && apt-get install -yq \
    ca-certificates \
    software-properties-common \
    python-software-properties \
    python-pip \
    curl \
    supervisor \
    git \
    libfontconfig \
    --no-install-recommends

# Clean up APT when done.
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
