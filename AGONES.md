---
layout: page
title: Agones
permalink: /agones/
---

# Agones Notes

## Minikube

* [Minikube notes](/kube)
* Startup with the supported Kubernetes version and the Agones profile
  *  `minikube start --kubernetes-version v1.29.7 -p agones`
  *  Starting with a (narrow) range of ports exposed (through Docker) for connections
      * `minikube start --kubernetes-version v1.29.7 -p agones --ports 7000-7010:7000-7010/udp`
* Get local IP
  * `minikube ip -p agones`
  * Use instead of the published `GameServer` IP
* "Uninstalling"
  * `minikube delete -p agones`
