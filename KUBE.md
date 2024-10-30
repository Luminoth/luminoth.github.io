---
layout: page
title: Kube
permalink: /kube/
---

# Kubernetes Notes

## General Usage

* [Cheatsheet](https://www.bluematador.com/learn/kubectl-cheatsheet)
* Get cluster info
  * `kubectl cluster-info`
* Get cluster config
  * `kubectl config view`
* Get API info
  * `kubectl api-resources`
  * `kubectl api-versions`
* List everything
  * `kubectl get all --all-namespaces`
* ... 

## Minikube

* [Install](https://minikube.sigs.k8s.io/docs/start/)
* [Handbook](https://minikube.sigs.k8s.io/docs/handbook/)
* [Command Reference](https://minikube.sigs.k8s.io/docs/commands/)
* Installing `kubtectl`
  * `minikube kubectl -- get po -A`
  * Add `alias kubectl="minikube kubectl --"` to profile
      * Using this with `agones` will need `-p agones` before the `--`
* Check for updates
  * `minikube update-check`
* Start the cluster
  * `minikube start`
  * [Agones](/agones) requires some additional parameters
* Get cluster status
  * `minikube status`
* Pause / Unpause the cluster
  * `minikube pause`
  * `minikube unpause`
* Halt the cluster
  * `minikube stop`
* List installed addons
  * `minikube addons list`
* Delete clusters
  * `minikube delete -p {profile}`
  * `minikube delete --all`
* Open dashboard
  * `minikube dashboard`
* Get logs
  * `minikube logs`
