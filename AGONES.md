---
layout: page
title: Agones
permalink: /agones/
---

# Agones Notes

## Minikube

* [Minikube notes](/kube)
* If using the `minikube` `kubectl`, make sure the alias includes the `agones` profile
  * `alias kubectl="minikube kubectl -p agones --`
* Startup with the supported Kubernetes version and the Agones profile
  *  `minikube start --kubernetes-version v1.29.7 -p agones`
  *  Starting with a (narrow) range of ports exposed (through Docker) for connections
      * `minikube start --kubernetes-version v1.29.7 -p agones --ports 7000-7010:7000-7010/udp`
* Get local IP
  * `minikube ip -p agones`
  * Use instead of the published `GameServer` IP
* "Uninstalling" the cluster
  * `minikube delete -p agones`

## General Usage

* Verify Agones is running
  * `kubectl describe --namespace agones-system pods`
      * Verify all 6 Pods exist and have no errors
  * `kubectl get pods --namespace agones-system`
      * All Pods should be Running
* Delete Fleets
  * `kubectl delete fleets --all --all-namespaces`
* Delete Game Servers
  * `kubectl delete gameservers --all --all-namespaces`
* Uninstalling
  * `kubectl delete -f https://raw.githubusercontent.com/googleforgames/agones/release-1.44.0/install/yaml/install.yaml`
  * `kubectl delete namespace agones-system`
