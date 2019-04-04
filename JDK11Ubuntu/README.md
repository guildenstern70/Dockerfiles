### Ubuntu-JDK Docker image

Docker image based on Ubuntu 18.04 with Oracle JDK 1.8.171

Create Docker image

    docker build . -t ubuntu18jdk8

-t is "tag" to tag image

Run image with shell

    docker run -it ubuntu18jdk8 /bin/bash

Modify as needed. To persist changes, OPEN ANOTHER TERMINAL WITHOUT EXITING:

    docker ps 

Get your image id

    docker commit [image id]  guildenstern/ubuntu18jdk8:version

If you want to push image onto Docker Hub:

    export DOCKER_ID_USER="guildenstern70"
    docker login
    docker tag ubuntu18jdk8 $DOCKER_ID_USER/ubuntu18jdk8
    docker push $DOCKER_ID_USER/ubuntu18jdk8

