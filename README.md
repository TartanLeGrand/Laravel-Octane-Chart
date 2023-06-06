# 🚀 Laravel Octane Kubernetes Helm Chart
This repository contains a [Helm](https://helm.sh/) chart for deploying a [Laravel Octane](https://github.com/laravel/octane) application to a Kubernetes cluster.

## 📋 Prerequisites
- Kubernetes 1.24+
- Helm 3.0+

## 💽 Installation
Clone the repository:

```bash
git clone https://github.com/your-github-account/laravel-octane-chart.git
cd laravel-octane-chart
```

Install the chart with the release name my-release:

```bash
helm install my-release .
```

## ⚙️ Configuration
The following table lists the configurable parameters of the Laravel Octane chart and their default values.

| Parameter	| Description |	Default |
|-----------|-------------|---------|
| replicaCount	| Number of replicas	| 2 |
| image.repository	| Laravel Octane image name	| your-docker-repository/laravel-octane |
| image.pullPolicy	| Image pull policy	| IfNotPresent |
| image.tag	| Image tag	| "" |
| service.type	| Kubernetes Service type	| ClusterIP |
| service.port	| Kubernetes Service port	| 8000 |
| ingress.enabled	| Enable ingress controller resource	| false |
| ingress.hosts	| Hosts for the ingress	| chart-example.local |
| resources	CPU/Memory resource requests/limits	| {} |

## 🎯 Using the Chart
To deploy your Laravel Octane application:

Build and push the Laravel Octane Docker image to your Docker registry.
Modify the values.yaml file to reference your Docker image and any other configurations you wish to change.
Install the chart as described above.
This chart also includes an optional Ingress object which can be used to expose your Laravel Octane application to the internet. You can enable and configure the Ingress object by modifying the ingress values in the values.yaml file.

## 👥 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## 📜 License
MIT