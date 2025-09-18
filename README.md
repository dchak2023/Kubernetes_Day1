# Kubernetes_Day1

> Learning repository for Kubernetes — tracking daily exercises and explorations.

---

## Table of Contents

- [Overview](#overview)  
- [Objectives](#objectives)  
- [Repository Structure](#repository-structure)  
- [Prerequisites](#prerequisites)  
- [Usage](#usage)  
- [Examples](#examples)  
- [What I Learned](#what-i-learned)  
- [Next Steps](#next-steps)  
- [Author](#author)

---

## Overview

This repository is part of my learning journey in Kubernetes.  
It contains basic resource definitions used on **Day 1** of studying Kubernetes — covering Pods, Namespaces, Deployments, etc., to understand how Kubernetes workloads are defined and run.

---

## Objectives

- Understand the basic Kubernetes resource types: **Pod**, **Namespace**, **Deployment**.  
- Practice writing YAML manifests for these resources.  
- Deploy simple applications in Kubernetes and observe how they work.  
- Learn how Kubernetes schedules workloads inside namespaces and how to define deployments.

---

## Repository Structure

| File | Purpose |
|------|---------|
| `namespace.yml` | Defines a Kubernetes Namespace for isolating resources. |
| `pod.yml` | Defines a Pod resource (single container). |
| `deployment.yml` | Defines a Deployment resource (manages replicas, rollouts). |

---

## Prerequisites

To use these manifests, you will need:

- **A Kubernetes cluster** (kind / minikube / k3s / GKE / EKS / AKS / etc.)  
- `kubectl` configured to talk to your cluster  
- Basic knowledge of `kubectl` commands  

---

## Usage

Here’s how you can apply the configurations in this repository:

### Create the namespace
```
kubectl apply -f namespace.yml
```
### Verify namespace was created
```
kubectl get namespaces
```
### Deploy a Pod (inside the namespace)
```
kubectl apply -f pod.yml -n nginx-test
```
### Check pods
```
kubectl get pods -n nginx-test
```
### Deploy a Deployment
```
kubectl apply -f deployment.yml -n nginx-test
```
### Check deployment status, replicas, etc.
```
kubectl get deployments -n nginx-test
kubectl get pods -n nginx-test
```


## Author:
[Devjoy Chakraborty 🧑‍💻](https://github.com/dchak2023)