# [Tasks](tasks.md)

+ Install Tools
    + [Install and Set Up kubectl](install-and-set-up-kubectl.md)
    + [Install Minikube](install-minikube.md)
+ [Configure Pods and Containers](#)
    + [Assign Memory Resources to Containers and Pods](#)
    + [Assign CPU Resources to Containers and Pods](#)
    + [Configure GMSA for Windows pods and containers](#)
    + [Configure Quality of Service for Pods](#)
    + [Assign Extended Resources to a Container](#)
    + [Configure a Pod to Use a Volume for Storage](#)
    + [Configure a Pod to Use a PersistentVolume for Storage](#)
    + [Configure a Pod to Use a Projected Volume for Storage](#)
    + [Configure a Security Context for a Pod or Container](#)
    + [Configure Service Accounts for Pods](#)
    + [Pull an Image from a Private Registry](#)
    + [Configure Liveness and Readiness Probes](#)
    + [Assign Pods to Nodes](#)
    + [Configure Pod Initialization](#)
    + [Attach Handlers to Container Lifecycle Events](#)
    + [Configure a Pod to Use a ConfigMap](#)
    + [Share Process Namespace between Containers in a Pod](#)
    + [Translate a Docker Compose File to Kubernetes Resources](#)
+ [Administer a Cluster](#)
    + [Administration with kubeadm](#)
        + [Certificate Management with kubeadm](#)
        + [Upgrading kubeadm HA clusters from v1.12 to v1.13](#)
        + [Upgrading kubeadm clusters from v1.12 to v1.13](#)
        + [Upgrading kubeadm clusters from v1.13 to v1.14](#)
        + [Upgrading kubeadm clusters from v1.14 to v1.15](#)
    + [Manage Memory, CPU, and API Resources](#)
        + [Configure Default Memory Requests and Limits for a Namespace](#)
        + [Configure Default CPU Requests and Limits for a Namespace](#)
        + [Configure Minimum and Maximum Memory Constraints for a Namespace](#)
        + [Configure Minimum and Maximum CPU Constraints for a Namespace](#)
        + [Configure Memory and CPU Quotas for a Namespace](#)
        + [Configure a Pod Quota for a Namespace](#)
    + [Install a Network Policy Provider](#)
        + [Use Calico for NetworkPolicy](#)
        + [Use Cilium for NetworkPolicy](#)
        + [Use Kube-router for NetworkPolicy](#)
        + [Romana for NetworkPolicy](#)
        + [Weave Net for NetworkPolicy](#)
    + [Access Clusters Using the Kubernetes API](#)
    + [Access Services Running on Clusters](#)
    + [Advertise Extended Resources for a Node](#)
    + [Autoscale the DNS Service in a Cluster](#)
    + [Change the Reclaim Policy of a PersistentVolume](#)
    + [Change the default StorageClass](#)
    + [Cluster Management](#)
    + [Configure Multiple Schedulers](#)
    + [Configure Out Of Resource Handling](#)
    + [Configure Quotas for API Objects](#)
    + [Control CPU Management Policies on the Node](#)
    + [Customizing DNS Service](#)
    + [Debugging DNS Resolution](#)
    + [Declare Network Policy](#)
    + [Developing Cloud Controller Manager](#)
    + [Encrypting Secret Data at Rest](#)
    + [Guaranteed Scheduling For Critical Add-On Pods](#)
    + [IP Masquerade Agent User Guide](#)
    + [Kubernetes Cloud Controller Manager](#)
    + [Limit Storage Consumption](#)
    + [Namespaces Walkthrough](#)
    + [Operating etcd clusters for Kubernetes](#)
    + [Reconfigure a Node's Kubelet in a Live Cluster](#)
    + [Reserve Compute Resources for System Daemons](#)
    + [Safely Drain a Node while Respecting the PodDisruptionBudget](#)
    + [Securing a Cluster](#)
    + [Set Kubelet parameters via a config file](#)
    + [Set up High-Availability Kubernetes Masters](#)
    + [Share a Cluster with Namespaces](#)
    + [Static Pods](#)
    + [Using CoreDNS for Service Discovery](#)
    + [Using NodeLocal DNSCache in Kubernetes clusters](#)
    + [Using a KMS provider for data encryption](#)
    + [Using sysctls in a Kubernetes Cluster](#)
+ [Manage Kubernetes Objects](#)
    + [Declarative Management of Kubernetes Objects Using Configuration Files](#)
    + [Declarative Management of Kubernetes Objects Using Kustomize](#)
    + [Managing Kubernetes Objects Using Imperative Commands](#)
    + [Imperative Management of Kubernetes Objects Using Configuration Files](#)
+ [Inject Data Into Applications](#)
    + [Define a Command and Arguments for a Container](#)
    + [Define Environment Variables for a Container](#)
    + [Expose Pod Information to Containers Through Environment Variables](#)
    + [Expose Pod Information to Containers Through Files](#)
    + [Distribute Credentials Securely Using Secrets](#)
    + [Inject Information into Pods Using a PodPreset](#)
+ [Run Applications](#)
    + [Run a Stateless Application Using a Deployment](#)
    + [Run a Single-Instance Stateful Application](#)
    + [Run a Replicated Stateful Application](#)
    + [Update API Objects in Place Using kubectl patch](#)
    + [Scale a StatefulSet](#)
    + [Delete a StatefulSet](#)
    + [Force Delete StatefulSet Pods](#)
    + [Perform Rolling Update Using a Replication Controller](#)
    + [Horizontal Pod Autoscaler](#)
    + [Horizontal Pod Autoscaler Walkthrough](#)
    + [Specifying a Disruption Budget for your Application](#)
+ [Run Jobs](#)
    + [Running Automated Tasks with a CronJob](#)
    + [Parallel Processing using Expansions](#)
    + [Coarse Parallel Processing Using a Work Queue](#)
    + [Fine Parallel Processing Using a Work Queue](#)
+ [Access Applications in a Cluster](#)
    + [Web UI (Dashboard)](#)
    + [Accessing Clusters](#)
    + [Configure Access to Multiple Clusters](#)
    + [Use Port Forwarding to Access Applications in a Cluster](#)
    + [Use a Service to Access an Application in a Cluster](#)
    + [Connect a Front End to a Back End Using a Service](#)
    + [Create an External Load Balancer](#)
    + [Configure Your Cloud Provider's Firewalls](#)
    + [List All Container Images Running in a Cluster](#)
    + [Set up Ingress on Minikube with the NGINX Ingress Controller](#)
    + [Communicate Between Containers in the Same Pod Using a Shared Volume](#)
    + [Configure DNS for a Cluster](#)
+ [Monitoring, Logging, and Debugging](#)
    + [Application Introspection and Debugging](#)
    + [Auditing](#)
    + [Debug Init Containers](#)
    + [Debug Pods and ReplicationControllers](#)
    + [Debug Services](#)
    + [Debug a StatefulSet](#)
    + [Debugging Kubernetes nodes with crictl](#)
    + [Determine the Reason for Pod Failure](#)
    + [Developing and debugging services locally](#)
    + [Events in Stackdriver](#)
    + [Get a Shell to a Running Container](#)
    + [Logging Using Elasticsearch and Kibana](#)
    + [Logging Using Stackdriver](#)
    + [Monitor Node Health](#)
    + [Resource metrics pipeline](#)
    + [Tools for Monitoring Resources](#)
    + [Troubleshoot Applications](#)
    + [Troubleshoot Clusters](#)
    + [Troubleshooting](#)
+ [Extend Kubernetes](#)
    + [Use Custom Resources](#)
        + [Extend the Kubernetes API with CustomResourceDefinitions](#)
        + [Versions of CustomResourceDefinitions](#)
    + [Configure the Aggregation Layer](#)
    + [Setup an Extension API Server](#)
    + [Use an HTTP Proxy to Access the Kubernetes API](#)
+ [TLS](#)
    + [Certificate Rotation](#)
    + [Manage TLS Certificates in a Cluster](#)
+ [Federation](#)
    + [Set up Cluster Federation with Kubefed](#)
    + [Set up CoreDNS as DNS provider for Cluster Federation](#)
    + [Set up placement policies in Federation](#)
    + [Cross-cluster Service Discovery using Federated Services](#)
    + [Administer Federation Control Plane](#)
        + [Federated Cluster](#)
        + [Federated ConfigMap](#)
        + [Federated DaemonSet](#)
        + [Federated Deployment](#)
        + [Federated Events](#)
        + [Federated Horizontal Pod Autoscalers (HPA)](#)
        + [Federated Ingress](#)
        + [Federated Jobs](#)
        + [Federated Namespaces](#)
        + [Federated ReplicaSets](#)
        + [Federated Secrets](#)
+ [Manage Cluster Daemons](#)
    + [Perform a Rolling Update on a DaemonSet](#)
    + [Perform a Rollback on a DaemonSet](#)
+ [Install Service Catalog](#)
    + [Install Service Catalog using Helm](#)
    + [Install Service Catalog using SC](#)
+ [Extend kubectl with plugins](#)
+ [Manage HugePages](#)
+ [Schedule GPUs](#)


