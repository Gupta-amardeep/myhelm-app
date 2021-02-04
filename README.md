## MYHELM-APP

It is a simple containerized microservice webapp that uses nginx webserver to deploy code on Kubernetes Cluster using Helm 3.0. Helm helps to deploy all the manifest required to run this application that includes services, deployments, configmap, serviceaccount etc.

# Introduction

This chart bootstraps a webapp deployment on a Kubernetes cluster using the Helm package manager. Configuration values are provided in separate file to make this chart reusable as well as to support easy upgrade and rollback.

# Prerequisites

* Kuberntes cluster
* Helm 3.0

# Installing the chart

To install the chart with the release name _my-release_:

> $ helm install my-release myhelm-app/

Tip: List all releases using helm list

# Configuration

Service type can be set using --set argument during install to show the URL at the output of helm install. For Example

> $ helm install my-release myhelm-app/ --set service.type=NodePort/LoadBalancer

