# pihole

![Version: 0.1.1](https://img.shields.io/badge/Version-0.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v5.1.2](https://img.shields.io/badge/AppVersion-v5.1.2-informational?style=flat-square)

A Helm chart for Kubernetes

**Homepage:** <https://shokohsc.github.io/charts/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| shokohsc | shokohsc@gmail.com |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| adlists | object | `{}` | blocklists |
| admin.existingSecret | string | `""` | Use an existing secret for the admin password. |
| admin.passwordKey | string | `"password"` | secret key |
| adminPassword | string | `"admin"` | Administrator password when not using an existing secret (see below) |
| affinity | object | `{}` | node/pod affinities (requires Kubernetes >=1.6) |
| autoscaling.enabled | bool | `false` | HorizontalPodAutoscaler toggle |
| autoscaling.maxReplicas | int | `100` | HorizontalPodAutoscaler maximum replicas |
| autoscaling.minReplicas | int | `1` | HorizontalPodAutoscaler minimum replicas |
| autoscaling.targetCPUUtilizationPercentage | int | `80` | HorizontalPodAutoscaler targetCPUUtilizationPercentage |
| blacklist | object | `{}` | blacklists |
| dhcp.enabled | bool | `false` | DHCP functionality toggle |
| dhcp.image.repository | string | `"shokohsc/dhcp-relay"` | DHCP image repository |
| dhcp.image.tag | string | `"latest"` | DHCP image tag |
| dhcp.service.annotations | object | `{}` | DHCP service annotations |
| dhcp.service.type | string | `"ClusterIP"` | DHCP service type |
| dnsmasq.additionalHostsEntries | list | `[]` | additional host entries |
| dnsmasq.customDnsEntries | list | `[]` | custom dns entries |
| dnsmasq.upstreamServers | list | `[]` | upstream dns servers |
| doh.enabled | bool | `false` | DNS over https functionality toggle |
| doh.image.repository | string | `"crazymax/cloudflared"` | DNS over https image repository |
| doh.image.tag | string | `"latest"` | DNS over https image tag |
| doh.service.annotations | object | `{}` | DNS over https service annotations |
| doh.service.type | string | `"ClusterIP"` | DNS over https service type |
| doh.upstream | string | `"https://1.1.1.1/dns-query"` | DNS over https upstream server |
| extraEnvVars | object | `{}` | extraEnvironmentVars is a list of extra enviroment variables to set for pihole to use https://github.com/pi-hole/docker-pi-hole/tree/v5.1.2#environment-variables |
| fullnameOverride | string | `""` | release full release name override option |
| image.pullPolicy | string | `"IfNotPresent"` | container image pull policy |
| image.repository | string | `"pihole/pihole"` | container image repository |
| image.tag | string | `""` | container image tag or Chart appVersion if undefined |
| imagePullSecrets | list | `[]` | registry secret |
| ingress.annotations | object | `{}` | Ingress annotations |
| ingress.enabled | bool | `false` | Ingress toggle |
| ingress.hosts | list | `[{"host":"chart-example.local","paths":[]}]` | Ingress hosts entries |
| ingress.tls | list | `[]` | Ingress tls entries |
| nameOverride | string | `""` | release name override option |
| nodeSelector | object | `{}` | node labels for pod assignment |
| persistentVolumeClaim | object | `{"accessModes":["ReadWriteOnce"],"annotations":{},"enabled":false,"size":"500Mi"}` | Enable persistence using Persistent Volume Claims |
| persistentVolumeClaim.annotations | object | `{}` | PersistentVolumeClaim annotations |
| persistentVolumeClaim.enabled | bool | `false` | set to true to use pvc |
| podAnnotations | object | `{}` | Pod annotations |
| podSecurityContext | object | `{}` | Pod security group context |
| probes.liveness | object | `{"enabled":true,"failureThreshold":10,"initialDelaySeconds":60,"timeoutSeconds":5}` | Configure the healthcheck for the ingress controller |
| probes.readiness | object | `{"enabled":true,"failureThreshold":3,"initialDelaySeconds":60,"timeoutSeconds":5}` | Configure the healthcheck for the ingress controller |
| regex | object | `{}` | regexes |
| replicaCount | int | `1` | pods replica count |
| resources | object | `{}` | pod resource requests & limits |
| securityContext | object | `{}` | Deployment security group context |
| service.annotations | object | `{}` | Service annotations |
| service.port | int | `80` | Pihole web port |
| service.type | string | `"ClusterIP"` | Service type |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | The name of the service account to use |
| timezone | string | `"UTC"` | timezone i.e Europe/Paris |
| tolerations | list | `[]` | node taints to tolerate (requires Kubernetes >=1.6) |
| virtualHost | string | `"chart-example.local"` | Pihole virtual host |
| whitelist | object | `{}` | whitelists |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.4.0](https://github.com/norwoodj/helm-docs/releases/v1.4.0)
