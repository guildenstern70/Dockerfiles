FROM gradle:5.3.1-jdk11-slim
MAINTAINER Alessio Saltarin <alessiosaltarin@gmail.com>
USER root

# Replace shell with bash so we can source files
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

# Install cURL
RUN apt-get update \
    && apt-get install -y curl \
    && apt-get install -y apt-utils \
    && apt-get -y autoclean

# Gradle Home
ENV GRADLE_USER_HOME=~/.gradle

# Node version
RUN mkdir -p /usr/local/nvm
ENV NVM_DIR /usr/local/nvm
ENV NODE_VERSION 10.13.0

# Download Node
RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash

# Install Node
RUN source $NVM_DIR/nvm.sh \
    && nvm install $NODE_VERSION \
    && nvm alias default $NODE_VERSION \
    && nvm use default

# add Node and npm to path 
ENV NODE_PATH $NVM_DIR/v$NODE_VERSION/lib/node_modules
ENV PATH $NVM_DIR/versions/node/v$NODE_VERSION/bin:$PATH

# Set Working Directory
ADD --chown=gradle . /src
WORKDIR /src

# Confirm installation
RUN java -version
RUN node -v
RUN npm -v


