# [Concepts](#)

+ [Overview](#)
    + [What is Kubernetes](#)
    + [Kubernetes Components](#)
    + [The Kubernetes API](#)
    + [Working with Kubernetes Objects](#)
        + [Understanding Kubernetes Objects](#)
        + [Kubernetes Object Management](#)
        + [Names](#)
        + [Namespaces](#)
        + [Labels and Selectors](#)
        + [Annotations](#)
        + [Field Selectors](#)
        + [Recommended Labels](#)
+ [Kubernetes Architecture](#)
    + [Nodes](#)
    + [Master-Node communication](#)
    + [Concepts Underlying the Cloud Controller Manager](#)
+ [Containers](#)
    + [Images](#)
    + [Container Environment Variables](#)
    + [Runtime Class](#)
    + [Container Lifecycle Hooks](#)
+ [Workloads](#)
    + [Pods](#)
        + [Pod Overview](#)
        + [Pods](#)
        + [Pod Lifecycle](#)
        + [Init Containers](#)
        + [Pod Preset](#)
        + [Disruptions](#)
    + [Controllers](#)
        + [ReplicaSet](#)
        + [ReplicationController](#)
        + [Deployments](#)
        + [StatefulSets](#)
        + [DaemonSet](#)
        + [Garbage Collection](#)
        + [TTL Controller for Finished Resources](#)
        + [Jobs - Run to Completion](#)
        + [CronJob](#)
+ [Services, Load Balancing, and Networking](#)
    + [Service](#)
    + [DNS for Services and Pods](#)
    + [Connecting Applications with Services](#)
    + [Ingress](#)
    + [Ingress Controllers](#)
    + [Network Policies](#)
    + [Adding entries to Pod /etc/hosts with HostAliases](#)
+ [Storage](#)
    + [Volumes](#)
    + [Persistent Volumes](#)
    + [Volume Snapshots](#)
    + [CSI Volume Cloning](#)
    + [Storage Classes](#)
    + [Volume Snapshot Classes](#)
    + [Dynamic Volume Provisioning](#)
    + [Node-specific Volume Limits](#)
+ [Configuration](#)
    + [Configuration Best Practices](#)
    + [Managing Compute Resources for Containers](#)
    + [Assigning Pods to Nodes](#)
    + [Taints and Tolerations](#)
    + [Secrets](#)
    + [Organizing Cluster Access Using kubeconfig Files](#)
    + [Pod Priority and Preemption](#)
    + [Scheduler Performance Tuning](#)
    + [Scheduling Framework](#)
+ [Security](#)
    + [Overview of Cloud Native Security](#)
+ [Policies](#)
    + [Limit Ranges](#)
    + [Resource Quotas](#)
    + [Pod Security Policies](#)
+ [Cluster Administration](#)
    + [Cluster Administration Overview](#)
    + [Certificates](#)
    + [Cloud Providers](#)
    + [Managing Resources](#)
    + [Cluster Networking](#)
    + [Logging Architecture](#)
    + [Configuring kubelet Garbage Collection](#)
    + [Federation](#)
    + [Proxies in Kubernetes](#)
    + [Controller manager metrics](#)
    + [Installing Addons](#)
+ [Extending Kubernetes](#)
    + [Extending your Kubernetes Cluster](#)
    + [Extending the Kubernetes API](#)
        + [Extending the Kubernetes API with the aggregation layer](#)
        + [Custom Resources](#)
    + [Compute, Storage, and Networking Extensions](#)
        + [Network Plugins](#)
        + [Device Plugins](#)
    + [Service Catalog](#)
    + [Poseidon-Firmament - An alternate scheduler](#)

