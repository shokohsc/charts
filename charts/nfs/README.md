# nfs

![Version: 0.0.1](https://img.shields.io/badge/Version-0.0.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.0.2](https://img.shields.io/badge/AppVersion-v0.0.2-informational?style=flat-square)

A Helm chart for Kubernetes

**Homepage:** <https://shokohsc.github.io/charts/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| shokohsc | shokohsc@gmail.com |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Pod affinity |
| autoscaling.enabled | bool | `false` | Specifies whether autoscaling should be enabled |
| autoscaling.maxReplicas | int | `100` | Maximum replicas |
| autoscaling.minReplicas | int | `1` | Minimum replicas |
| autoscaling.targetCPUUtilizationPercentage | int | `80` | threshold to activate autoscaling |
| fullnameOverride | string | `""` | Release name override (full) |
| image.pullPolicy | string | `"Always"` | Kubernetes pull policy image |
| image.repository | string | `"shokohsc/volume-nfs"` | Container project image |
| imagePullSecrets | list | `[]` | Registry pull secrets |
| ingress.annotations | object | `{}` | Annotations to add to the ingress |
| ingress.enabled | bool | `false` | Specifies whether an ingress should be created |
| ingress.hosts | list | `[{"host":"chart-example.local","paths":[]}]` | Ingress rules |
| ingress.tls | list | `[]` | Ingress certificates |
| nameOverride | string | `""` | Release name override |
| nodeSelector | object | `{}` | Pod nodeSelector labels |
| podAnnotations | object | `{}` | Annotations to add to the pod |
| podSecurityContext | object | `{}` | securityContext to add to the pod |
| replicaCount | int | `1` | The number of replica pods 0-n |
| resources | object | `{}` | Resources to define on the pod |
| securityContext | object | `{"privileged":true}` | securityContext & capabilities to add to the pod |
| securityContext.privileged | bool | `true` | add privileged (full capabilities) to the nfs server |
| service.port | int | `2049` | Service port |
| service.type | string | `"ClusterIP"` | Service type |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `false` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and create is true, a name is generated using the fullname template |
| tolerations | list | `[]` | Pod tolerations |
| volumes | list | `[]` | Volumes to add to the pod |
