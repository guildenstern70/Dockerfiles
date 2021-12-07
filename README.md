### Dockerfiles

How to build images:

    cd JDK17Gradle7
    docker build -t guildenstern70/jdk17gradle7 .
    [opt] docker push guildenstern70/jdk17gradle7

Test container:

    docker run -it guildenstern70/jdk17gradle7:1.0 /bin/bash

    
