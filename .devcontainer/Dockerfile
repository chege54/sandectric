FROM ubuntu:latest

# Install dependencies
RUN apt-get update && apt-get install -y \
    git-all \
    curl \
    vim \
    wget \
    nodejs npm

#get 'latest' go version
RUN wget https://go.dev/dl/go1.23.3.linux-amd64.tar.gz -O /tmp/go.tar.gz && \
    tar -xzf /tmp/go.tar.gz -C /usr/local
ENV PATH="$PATH:/usr/local/go/bin"

# get 'latest' version of hugo
RUN wget https://github.com/gohugoio/hugo/releases/download/v0.138.0/hugo_extended_withdeploy_0.138.0_linux-amd64.tar.gz -O /tmp/hugo.tar.gz && \
    tar -xzf /tmp/hugo.tar.gz -C /usr/local/bin

# ubuntu user is available in the base image
# RUN apt-get install sudo
# RUN usermod -aG sudo ubuntu
USER ubuntu

EXPOSE 1313

# interactive shell
# CMD ["/bin/bash", "-il"]
