
# Helm Charts Repository

Welcome to the **Helm Charts Repository**! This repository hosts a collection of Helm charts for various applications, packaged and ready for deployment. Charts are available for easy integration and deployment using GitLab Pages.

## 🚀 Getting Started

To use these Helm charts in your Kubernetes environment, first ensure that you have [Helm](https://helm.sh/docs/intro/install/) installed.

## 📦 Available Charts

| Chart Name      | Description                | Latest Version | Based/copied from                                                  | Last Merged Version |
|-----------------|----------------------------|----------------|--------------------------------------------------------------------|---------------------|
| node-red        | Node-Red                   | 0.33.0         | https://artifacthub.io/packages/helm/node-red/node-red             | 0.33.0              |
| emqx            | EMQX                       | 1.1.2          | https://artifacthub.io/packages/helm/emqx-operator/emqx            | 5.8.1               |
| nfs-provisioner | NFS Provisioner            | 4.0.18         | https://github.com/kubernetes-sigs/nfs-subdir-external-provisioner | 4.0.18              |
| grafana         | Grafana                    | 8.5.11         | https://artifacthub.io/packages/helm/grafana/grafana               | 8.5.11              |

To install a chart:
```bash
helm install <release-name> my-charts/<chart-name>
```
