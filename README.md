# nginx-google-docker
a simple alpine-base dockerfile of google reverse proxy for deploying by oc

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

For oc command:

    oc new-app --docker-image=registry-1.docker.io/letssudormrf/nginx-google-docker:latest --name='nginx-google-docker' --labels='app=nginx-google-docker'

To create the route:

    oc expose service <ServiceName>


