---
title: Installation
classes: wide
toc: false
permalink: /guide/install/
---
## Prerequisites

* Kubernetes v1.8+ is recommended for the improved CRD support, especially
  garbage collection on custom resources.

### Grant yourself cluster-admin (GKE only)

Due to a [known issue](https://cloud.google.com/container-engine/docs/role-based-access-control#defining_permissions_in_a_role)
in GKE, you'll need to first grant yourself `cluster-admin` privileges before
you can install the necessary RBAC manifests.

```sh
kubectl create clusterrolebinding <user>-cluster-admin-binding --clusterrole=cluster-admin --user=<user>@<domain>
```

Replace `<user>` and `<domain>` above based on the account you use to authenticate to GKE.

## Install Metacontroller

```sh
# Create 'metacontroller' namespace, service account, and role/binding.
kubectl apply -f {{ site.repo_raw }}/manifests/metacontroller-rbac.yaml
# Create CRDs for Metacontroller APIs, and the Metacontroller Deployment.
kubectl apply -f {{ site.repo_raw }}/manifests/metacontroller.yaml
```

If you prefer to build and host your own images, please see the
[build instructions](/contrib/build/) in the contributor guide.