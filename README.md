## Myhelm-app

It is a simple containerized microservice webapp that uses nginx webserver to deploy code on Kubernetes Cluster using Helm 3.0. Helm helps to deploy all the manifest required to run this application that includes services, deployments, configmap, serviceaccount etc.

# Introduction

This chart bootstraps a webapp deployment on a Kubernetes cluster using the Helm package manager. Configuration values are provided in separate file to make this chart reusable as well as to support easy upgrade and rollback.

Files:-
1. Chart.yaml - Information about chart.
2. values.yaml - The default values for templates.
3. NOTES.txt - The "help text" for chart. This will be displayed to your users when they run helm install.
4. _helpers.tpl - A place to put template helpers that can be re-use throughout the chart.
5. deployment.yaml - A basic manifest for creating a Kubernetes deployment
6. service.yaml - creating service to expose the deployment.
7. auto-scaling.yaml - HPA helps scaling the pod replicas if cluster supported.
8. config-map.yaml - helps to inject html file to pod as volume.
9. srviceaccount.yaml - serviceaccount asociated with pod.

# Key Takeoffs

* Replicas help to keep application highly avialible and fault tolerant.
* Service expose endpoint for application discovery as well as help as loadbalancer between replicas.
* HPA helps to scale up and down automatically based on CPU and memory metrics.
* Helm functions, objects keep all the manifest in sync using defined values and maintain uniformity.

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

# Author

managed by Amardeep Gupta
