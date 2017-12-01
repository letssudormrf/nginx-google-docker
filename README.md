# nginx-google-docker
a simple alpine-base docker image for google reverse proxy

Quick Start
-----------

This image is Nginx reverse proxy for Google, binding the multi-port for the following language.

    8001 EN
    8081 JA
    8086 ZH
    8886 ZF

For Docker run command:

    docker run --restart always -d -p 8001:8001/tcp -p 8081:8081/tcp -p 8086:8086/tcp -p 8886:8886/tcp --name nginx-google-docker letssudormrf/nginx-google-docker

Or

    docker run --restart always -d -P --name nginx-google-docker letssudormrf/nginx-google-docker

