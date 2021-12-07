FROM gradle:7.3.1-jdk17
MAINTAINER Alessio Saltarin <alessiosaltarin@gmail.com>
USER root
RUN apt-get update; apt-get -y install curl
ENV GRADLE_USER_HOME=~/.gradle
ADD --chown=gradle . /src
WORKDIR /src
