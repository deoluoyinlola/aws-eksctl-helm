# eksctl-kubernetes-cluster-helm-prometheus
Kubernetes cluster provisioned with eksctl, manage by helm and monitor with prometheus and grafana. 

# Contents
* [Architecture](#architecture)
* [Project Requirement](#project-requirement)
* [Main Tools Used](#main-tools-used)
* [Project Deliverables](#project-deliverables)
* [Documentation](#documentation)
  * [Provision cluster with eskctl](#provision-cluster-with-eskctl)
    * [Master node](#master-node)
    * [Connect kubernetes with cluster](#connect-kubernetes-with-cluster)
    * [Configure auto-scaling](#configure-auto-scaling)
  * [Deploy Microservices with helm](#deploy-microservices-with-helm)
    * [Deploy apps to cluster](#deploy-apps-to-cluster)
  * [Deploy Prometheus Monitoring Stack](#deploy-prometheus-monitoring-stack)
    * [Monitoring at Infra](#monitoring-at-infra)
    * [Monitoring at Platform](#monitoring-at-platform)
    * [Monitoring at Application](#monitoring-at-application)
* [Lesson learnt](#lesson-learnt)

## Architecture
![design](docs/assets/designs.svg)

## Project Requirement
- 
- 
- 
- 

## Main Tools Used
- [aws](https://aws.amazon.com/) - cloud platform, offers reliable, scalable, and inexpensive cloud computing services.
- [VSCode](https://code.visualstudio.com/) - a source-code editor made by Microsoft with the Electron Framework, for Windows, Linux and macOS.
- [helm](https://helm.sh/) - Helm helps you manage Kubernetes applications — Helm Charts help you define, install, and upgrade even the most complex Kubernetes application.
- [eksctl](https://eksctl.io/) - a simple CLI tool for creating and managing clusters on EKS - Amazon's managed Kubernetes service for EC2.
- [prometheus](https://prometheus.io/) - An open-source monitoring system with a dimensional data model, flexible query language, efficient time series database and modern alerting approach.
- [grafana](https://grafana.com/) - Grafana is the open source analytics & monitoring solution for every database.


## Project Deliverables
![d-app](docs/assets/d-app.png)


## Documentation
From the architecture flow shown;
Git --> GitHub --> eskctl --> helm --> kubernetes cluster --> prometheus --> Grafana
![design](docs/assets/designs.svg)

### Provision cluster with eskctl
- 
#### Master node

## Lesson learnt