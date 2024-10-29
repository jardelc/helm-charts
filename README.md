
# Helm Charts Repository

Welcome to the **Helm Charts Repository**! This repository hosts a collection of Helm charts for various applications, packaged and ready for deployment. Charts are available for easy integration and deployment using GitLab Pages.

## 🚀 Getting Started

To use these Helm charts in your Kubernetes environment, first ensure that you have [Helm](https://helm.sh/docs/intro/install/) installed.

## 📥 Adding this Helm Repository

Add this repository to Helm by running:
```bash
helm repo add my-charts  https://git.vwoa.na.vwg/chattanoogaitprodsys/kubecluster/helm-charts/charts
helm repo update
```

## 📦 Available Charts

| Chart Name | Description                | Latest Version |
|------------|----------------------------|----------------|
| node-red   | A Helm chart for Node-Red  | 0.33.0        |

To install a chart:
```bash
helm install <release-name> my-charts/<chart-name>
```

## 🛠 Manual Packaging and Index Update

To manually package new or updated charts and add them to the `index.yaml` file, follow these steps:

1. **Package the Chart:**
   Run the following command to create a `.tgz` package of the chart:
   ```bash
   helm package chart-src/<your-app> --destination charts/
   ```

2. **Update the `index.yaml` File:**
   After packaging, update the `index.yaml` file to include the new or updated chart by running:
   ```bash
   helm repo index charts/ --url https://git.vwoa.na.vwg/chattanoogaitprodsys/kubecluster/helm-charts/charts
   ```

   This command will regenerate the `index.yaml` file, listing all available charts and their versions.

