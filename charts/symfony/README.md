# symfony

![Version: 0.1.1](https://img.shields.io/badge/Version-0.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: latest](https://img.shields.io/badge/AppVersion-latest-informational?style=flat-square)

A Helm chart for Kubernetes

**Homepage:** <https://shokohsc.github.io/charts/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| shokohsc | shokohsc@gmail.com |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | node/pod affinities (requires Kubernetes >=1.6) |
| autoscaling.enabled | bool | `false` | HorizontalPodAutoscaler toggle |
| autoscaling.maxReplicas | int | `100` | HorizontalPodAutoscaler maximum replicas |
| autoscaling.minReplicas | int | `1` | HorizontalPodAutoscaler minimum replicas |
| autoscaling.targetCPUUtilizationPercentage | int | `80` | HorizontalPodAutoscaler targetCPUUtilizationPercentage |
| envVars | object | `{}` | Pod environment variables |
| extraVolumes | list | `[]` | Pod extra volumes |
| fullnameOverride | string | `""` | release full release name override option |
| image.pullPolicy | string | `"IfNotPresent"` | container image pull policy |
| image.repository | string | `"symfony"` | container image repository: some symfony app |
| image.tag | string | `""` | container image tag or Chart appVersion if undefined |
| imagePullSecrets | list | `[]` | registry secret |
| ingress.annotations | object | `{}` | Ingress annotations |
| ingress.enabled | bool | `false` | Ingress toggle |
| ingress.hosts | list | `[{"host":"chart-example.local","paths":[]}]` | Ingress hosts entries |
| ingress.tls | list | `[]` | Ingress tls entries |
| initContainers | list | `[]` | Pod init containers |
| nameOverride | string | `""` | release name override option |
| nginx.envVars | object | `{}` | nginx container environment variables |
| nginx.extraVolumes | list | `[]` | nginx container extra volumes |
| nginx.image.repository | string | `"nginx"` | nginx image repository |
| nginx.image.tag | string | `"1-alpine"` | nginx image tag |
| nodeSelector | object | `{}` | node labels for pod assignment |
| php.envVars | object | `{}` | php container environment variables |
| php.extraVolumes | list | `[]` | php container extra volumes |
| php.image.repository | string | `"php"` | php image repository |
| php.image.tag | string | `"7-fpm-alpine"` | php image tag |
| podAnnotations | object | `{}` | Pod annotations |
| podSecurityContext | object | `{}` | Pod security group context |
| replicaCount | int | `1` | pods replica count |
| resources | object | `{}` | pod resource requests & limits |
| securityContext | object | `{}` | Deployment security group context |
| service.annotations | object | `{}` | Service annotations |
| service.port | int | `80` | Service port |
| service.type | string | `"ClusterIP"` | Service type |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | The name of the service account to use |
| tolerations | list | `[]` | node taints to tolerate (requires Kubernetes >=1.6) |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.4.0](https://github.com/norwoodj/helm-docs/releases/v1.4.0)