---
layout: page
title: Kube
permalink: /kube/
---

# Kubernetes Notes

## Minikube

* [Install](https://minikube.sigs.k8s.io/docs/start/)
* Start `minikube`
  * `minikube start`
  * [Agones](/agones) requires some additional parameters
* Install `kubtectl`
  * `minikube kubectl -- get po -A`
  * Add `alias kubectl="minikube kubectl --"` to profile
* Open dashboard
 * `minikube dashboard`
