FROM gradle:6.6.1-jdk14
MAINTAINER Alessio Saltarin <alessiosaltarin@gmail.com>
USER root
RUN apt-get update; apt-get -y install curl
ENV GRADLE_USER_HOME=~/.gradle
ADD --chown=gradle . /src
WORKDIR /src