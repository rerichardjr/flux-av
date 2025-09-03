# WIP: Flux-AV: Autonomous Vehicle Lab - In-a-Box

Flux-AV is an end-to-end autonomous vehicle lab designed to be deployed with minimal effort using GitOps principles.

Base RKE2 will be from this [Vagrant build](https://github.com/rerichardjr/vagrant-rke2)

---

## Project Overview

This repository provides a GitOps-driven deployment for an RKE2 Kubernetes cluster using Vagrant. It bootstraps core infrastructure components and application sets automatically, enabling rapid experimentation and development.

### 🔧 Key Features (so far)

- **GitOps-first**: Declarative infrastructure and app management via Argo CD
- **RKE2 + Vagrant**: Local Kubernetes cluster provisioned with Vagrant
- **Automated Bootstrap**: Argo CD syncs manifests from this repo
- **Modular Infra Stack**:
  - `cert-manager` for certificate management
  - `Traefik` as the ingress controller
  - `MetalLB` for bare-metal load balancing

---

## About My Lab

This repository is supported by a home lab designed for hands-on network and server experimentation.  Below are the details of the infrastructure:

### Server Configuration
- **Motherboard**: ASRock 990FX Extreme9
- **Processor**: AMD FX™-8150 Eight-Core, 3.6 GHz
- **Memory**: 32 GiB
- **Storage**: 480 GB Kingston SSD
- **GPU**: EVGA GeForce RTX 3060
- **Operating System**: Ubuntu 24.04, deployed via Canonical MAAS (PXE boot)

### Networking Setup
- **NICs**:  
  - Intel Corporation 82571EB/82571GB Gigabit Ethernet Controller (copper applications)  
    - Interfaces: `enp6s0f0`, `enp6s0f1`  
  - Intel Corporation 82583V Gigabit Network Connection  
    - Interface: `enp9s0`  
- **Traffic Management**:  
  - Open vSwitch (OVS) bridge configured with `enp6s0f0` and `enp6s0f1` for lab traffic  
- **Network Integration**:  
  - VLANs for lab traffic are trunked to a MikroTik router for network segmentation and control

