# aws-eksctl-with-helm-prometheus
A demostration of how I provisioned kubernetes cluster with eksctl, manage the microservices by helm, monitor both the infrastructure and application with prometheus and visualize the result with grafana for an online-shopping webapp.

# Contents
* [Architecture](#architecture)
* [Project Objective](#project-Objective)
* [Pre-requisites](#pre-requisities)
  * [Knowledge](#knowledge)
  * [Tools](#tools)
* [Demo](#demo)
  * [Provision cluster with eskctl](#provision-cluster-with-eskctl)
    * [Master node](#master-node)
    * [Connect kubernetes with cluster](#connect-kubernetes-with-cluster)
    * [Configure auto-scaling](#configure-auto-scaling)
  * [Deploy Microservices with helmfile](#deploy-microservices-with-helmfile)
    * [Create helm chart](#create-helm-chart)
    * [Deploy apps to cluster](#deploy-apps-to-cluster)
  * [Deploy Prometheus Monitoring Stack](#deploy-prometheus-monitoring-stack)
    * [Monitoring at Infra](#monitoring-at-infra)
    * [Monitoring at Platform](#monitoring-at-platform)
    * [Monitoring at Application](#monitoring-at-application)
* [Resources](#resources)
* [Lesson learnt](#lesson-learnt)

## Architecture
![design](docs/assets/designs.svg)

## Project Objective
- By the end of the first part of this project, we will know how to provision kubernetes cluster resources in AWS with help of eksctl.
- Through the end of second part of the project, we will have master how to deploy highly scalable microservices application with helmfile.
- And in the final part, we will know how to monitor at infrastructure and application level with prometheus and grafana for visualization.

## Pre-requisities
- So that we all be on the same page, it will be nice to have following in our tool belt;
### Knowledge
- Basic knowledge of how AWS, kubernetes, helm, yaml, prometheus and grafana works.
### Tools
- [aws](https://aws.amazon.com/) - cloud platform, offers reliable, scalable, and inexpensive cloud computing services.
- [aws cli](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)  - a unified tool to manage your AWS services.
- [VSCode](https://code.visualstudio.com/) - a source-code editor made by Microsoft with the Electron Framework, for Windows, Linux and macOS.
- [helm](https://helm.sh/) - Helm helps you manage Kubernetes applications — Helm Charts help you define, install, and upgrade even the most complex Kubernetes application.
- [eksctl](https://eksctl.io/) - a simple CLI tool for creating and managing clusters on EKS - Amazon's managed Kubernetes service for EC2.
- [prometheus](https://prometheus.io/) - An open-source monitoring system with a dimensional data model, flexible query language, efficient time series database and modern alerting approach.
- [grafana](https://grafana.com/) - Grafana is the open source analytics & monitoring solution for every database.

## Demo
From the architecture flow shown;
Git --> GitHub --> eskctl --> helmfile --> kubernetes cluster --> prometheus --> Grafana
![design](docs/assets/designs.svg)

### Provision cluster with eskctl
- Step 1: Programmatic access; 

- Step 2: Install and configure kubectl, AWS CLI and eksctl. [Link to How](https://docs.aws.amazon.com/eks/latest/userguide/getting-started.html). Be careful to set and utilise profile name when working with multiple accounts in your machine.

- Step 3: Creating cluster with a name in a specify region and without config file, run; ``eksctl create cluster``


#### Master node

### Deploy Microservices with helmfile
Let’s quickly remind ourselves that;
- The microservices source code repository for this project is from this link; [google-microservices-demo](https://github.com/GoogleCloudPlatform/microservices-demo), containing 11 services I will be deploying with this demo. Among the services, Frontend serve as entrypoint for all the service receiving externally request from the browser. The load generator deployment is optional.
- Also, image names for each microservice, expected environment variables including which port each starts and decision on namespace depending on developer's access must be a collaborative effort between Dev and Ops team.
Before moving on with the following steps, get helm installed [helm](https://helm.sh/docs/intro/install/)

#### Create helm chart
- Step 1: Create shared helm chart for the 10 microservices, run the command
```
helm create common
```
It should auto generate a folder named after what we call our chart, containing; charts folder, template folder, Chart.yaml, values.yaml, .helmignore file
- Step 2: Inside template folder create deployment and service blueprint by configuring the ``deployment.yaml`` and ``service.yaml``
- Step 3: Define the actual values for the template files inside ``values.yaml``


## Lesson learnt

## Resources
The following are useful resources that really contribute to actualise this project;
- Docs; aws doc, helm doc, eksctl doc, prometheus doc, grafana doc
- YouTube Channels; TechWorldWithNana, Cloud With Raj, Be A Better Dev, DevOps Made Easy
- Repo; 
