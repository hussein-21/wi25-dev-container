FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Install required packages
RUN apt-get update && apt-get install -y \
    xz-utils \
    curl \
    gnupg \
    ca-certificates \
    software-properties-common

# Install Node.js (LTS version)
RUN curl -fsSL https://deb.nodesource.com/setup_lts.x | bash - && \
    apt-get install -y nodejs

# Install Go (latest stable)
RUN curl -OL https://golang.org/dl/go1.21.6.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go1.21.6.linux-amd64.tar.gz && \
    echo 'export PATH=$PATH:/usr/local/go/bin' >> /etc/bash.bashrc
