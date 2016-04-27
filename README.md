# docker-debian

[![Build Status](https://travis-ci.org/joeygibson/docker-debian.svg?branch=master)](https://travis-ci.org/joeygibson/docker-debian)

Customized Debian Jessie Docker image.

## Contents
* curl
* wget
* tree
* Docker client 1.8.3
* Docker-Compose 1.5.2

## Running
    docker run -it joeygibson/debian:jessie 
will drop you into bash.


    docker run -it -v /var/run/docker.sock:/var/run/docker.sock -v $(pwd):/opt/project -w /opt/project joeygibson/debian:jessie 
will do the same thing, but will map the current directory to `/opt/project`, map the Docker socket into
the container for Docker-in-Docker, and will `cd /opt/project` so you're ready to go.

