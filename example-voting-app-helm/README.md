# Example Voting App Helm Chart

This Helm chart deploys the Example Voting App, which consists of multiple services including a database, Redis, a voting service, a result service, and a worker service. 

## Prerequisites

- Kubernetes cluster
- Helm installed on your local machine

## Installation

To install the chart, use the following command:

```
helm install <release-name> ./example-voting-app-helm
```

Replace `<release-name>` with a name for your release.

## Configuration

You can customize the deployment by modifying the `values.yaml` file. This file contains default configuration values for the various services in the application.

## Services

The following services are included in this chart:

- **Database**: Managed by `db-deployment.yaml` and `db-service.yaml`
- **Redis**: Managed by `redis-deployment.yaml` and `redis-service.yaml`
- **Voting Service**: Managed by `vote-deployment.yaml` and `vote-service.yaml`
- **Result Service**: Managed by `result-deployment.yaml` and `result-service.yaml`
- **Worker Service**: Managed by `worker-deployment.yaml`

## Usage

After installation, you can access the voting service through the service defined in `vote-service.yaml`. 

To upgrade the chart with new configurations, use:

```
helm upgrade <release-name> ./example-voting-app-helm
```

To uninstall the chart, use:

```
helm uninstall <release-name>
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.