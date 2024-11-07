---
layout: page
title: Docker
permalink: /docker/
---

# Docker Notes

* [Cheatsheet](https://docs.docker.com/get-started/docker_cheatsheet.pdf)
  * this seems to be outdated now with `buildx` being a thing
* [Ultimate Cheatsheet](https://dockerlabs.collabnix.com/docker/cheatsheet/)

## Images

* Build an image
  * `docker buildx build -t {container name}`
  * Can specify the directory to build from: `docker buildx build -t {container name} {directory}`
  * `-f {Dockerfile}` to specify the Dockerfile to use
  * `-no-cache` skips the cache
* List local Images
  * `docker images`
* Delete an image
  * `docker rmi {image name}`
* Remove unused images
  * `docker image prune`

## Containers

* Create and run a container from an image
  * `docker run {image name}`
  * `-d` to run in the background
  * Can give the container a customer name with `--name {container name}`
* List containers
  * `docker ps` to show running containers
  * `--all` to show running and stopped containers
* Start / stop existing containers
  * `docker {start | stop} {container name | container id}`
* Remove a stopped container
  * `docker rm {container name}`
* Open a shell in a container
  * `docker exec -it {container name} sh`
