FROM gradle:5.3.1-jdk11-slim
MAINTAINER Alessio Saltarin <alessiosaltarin@gmail.com>
USER root
ENV GRADLE_USER_HOME=~/.gradle
ADD --chown=gradle . /src
WORKDIR /src
CMD ["gradle", "--version"]
