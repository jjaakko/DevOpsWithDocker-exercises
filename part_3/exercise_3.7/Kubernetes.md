# Kubernetes

> Kubernetes (K8s) is an open-source system for automating deployment, scaling, and management of containerized applications.

Source: https://kubernetes.io/

Docker-compose can manage multiple containers in the same host machine. However, if you need multiple host machines, you need other tools.

Kubernetes is currently the most used tool to for managing multiple containers and containerized host machines. Big vendors such as Google Cloud Platform and Amazon Web Services offer Kubernetes based deployments. Other options include Red Hat's (Open Shift)[https://www.openshift.com/] which is also based on Kubernetes under the hood.

## A couple of Kubernetes related terms

* Node
    * A host machine. Can be physical or virtual.
    * Master node communicates with worker nodes.
* Pod
    * A set of one or more containers. Smallest entity that can be deployed.
* Kubelet
    * Handles the communication between master node and the worker node. Also executes pod containers.

## Why to use Kubernetes?

Kubernetes makes it easier to scale the application(s). It takes care of starting new container instances when needed and killing of non-responding containers. It also takes care of load balancing and makes rollback to previous state possible. This is not an exhaustive list of reasons to use Kubernetes.

