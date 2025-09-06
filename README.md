
## Project Overview

**Java Web App Helm Chart** automates deployment of a Java web application on Kubernetes.  
It provides a production-ready deployment with **Deployment, Service, and Horizontal Pod Autoscaler (HPA) and EKS cluster-auto scaler**.  

This Helm chart allows developers and DevOps engineers to deploy, scale, and manage the application reliably using Helm.

**Key Features:**
- Configurable Docker image and tag via `values.yaml`
- Scalable Deployment with HPA (CPU 60%, Memory 75%)
- NodePort or LoadBalancer service configuration
- Resource requests and limits for optimal pod performance
- Easy upgrades and CI/CD ready

---

## Project Highlights

- **End-to-End Deployment:** From templated manifests to HPA scaling
- **Helm Best Practices:** Values configurable, linted, and packaged
- **Documentation Ready:** Includes README and Helm commands




## Chart Details
- **Chart Name:** java-web-app
- **Version:** 0.1.0
- **App Version:** 1.0.1
- **Repository:** [GitHub](https://github.com/Sivakrishnachekuri/PROJECTS)

## Prerequisites
- Kubernetes 1.16+
- Helm 3.x
- Cluster configured and accessible via `kubectl`

## Installing the Chart
```bash
helm install my-java-web-app ./java-web-app


## Configuration

  Override default values in values.yaml or via --set:

      helm install my-java-web-app ./java-web-app \
       --set image.tag=1.0.2 \
       --set service.type=LoadBalancer

# Upgrading the Chart


   helm upgrade my-java-web-app ./java-web-app


#List Installed Releases 

 helm list

# Upgrade chart
helm upgrade my-java-web-app ./java-web-app

# Uninstall chart
helm uninstall my-java-web-app

# View release status
helm status my-java-web-app

# List all Helm releases
helm list

# Render templates locally
helm template my-java-web-app ./java-web-app

# Test Helm chart
helm test my-java-web-app

# Package the chart
helm package ./java-web-app

# Lint the chart
helm lint ./java-web-app

# Rollback a release
helm rollback my-java-web-app 1


