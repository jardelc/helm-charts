# node-red ⚙

## Forked from:
* <https://github.com/SchwarzIT/node-red-chart> -- version 0.33.0>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | The affinity constraint |
| clusterRoleRules.enabled | bool | `false` | Enable custom rules for the application controller's ClusterRole resource default: false |
| clusterRoleRules.rules | list | `[]` | List of custom rules for the application controller's ClusterRole resource default: [] |
| deploymentAnnotations | object | `{}` | Deployment annotations |
| deploymentStrategy | string | `""` | Specifies the strategy used to replace old Pods by new ones, default: `RollingUpdate` |
| env | list | `[]` | node-red env, see more environment variables in the [node-red documentation](https://nodered.org/docs/getting-started/docker) |
| envFrom | list | `[]` |  |
| extraSidecars | list | `[]` | You can configure extra sidecars containers to run alongside the node-red pod. default: [] |
| extraVolumeMounts | string | `nil` | Extra Volume Mounts for the node-red pod |
| extraVolumes | string | `nil` | Extra Volumes for the pod |
| fullnameOverride | string | `""` | String to fully override "node-red.fullname" |
| image.pullPolicy | string | `"IfNotPresent"` | The image pull policy |
| image.registry | string | `"docker.io"` | The image registry to pull from |
| image.repository | string | `"nodered/node-red"` | The image repository to pull from |
| image.tag | string | `""` | The image tag to pull, default: `Chart.appVersion` |
| imagePullSecrets | string | `""` | The image pull secrets |
| ingress.annotations | object | `{}` | Additional ingress annotations |
| ingress.className | string | `""` | Defines which ingress controller will implement the resource |
| ingress.enabled | bool | `false` | Enable an ingress resource for the server |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0] | object | `{"path":"/","pathType":"ImplementationSpecific"}` | The base path |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` | Ingress type of path |
| ingress.tls | list | `[]` | Ingress TLS configuration |
| initContainers | list | `[]` | containers which are run before the app containers are started |
| livenessProbe | object | `{"httpGet":{"path":"/","port":"http"}}` | Liveness probe for the Deployment |
| metrics.enabled | bool | `false` | Deploy metrics service |
| metrics.path | string | `"/metrics"` |  |
| metrics.serviceMonitor.additionalLabels | object | `{}` | Prometheus ServiceMonitor labels |
| metrics.serviceMonitor.basicAuth | object | `{}` | Prometheus basicAuth configuration for ServiceMonitor endpoint |
| metrics.serviceMonitor.enabled | bool | `false` | Enable a prometheus ServiceMonitor |
| metrics.serviceMonitor.interval | string | `"30s"` | Prometheus ServiceMonitor interval |
| metrics.serviceMonitor.metricRelabelings | list | `[]` | Prometheus [MetricRelabelConfigs] to apply to samples before ingestion |
| metrics.serviceMonitor.namespace | string | `""` | Prometheus ServiceMonitor namespace |
| metrics.serviceMonitor.relabelings | list | `[]` | Prometheus [RelabelConfigs] to apply to samples before scraping |
| metrics.serviceMonitor.selector | object | `{}` | Prometheus ServiceMonitor selector |
| nameOverride | string | `""` | Provide a name in place of node-red |
| nodeSelector | object | `{}` | Node selector |
| npmrc.content | string | `"# Custom npmrc config\n"` | Configuration to add custom npmrc config |
| npmrc.enabled | bool | `false` | Enable custom npmrc config |
| npmrc.registry | string | `"https://registry.npmjs.org"` | Configuration to use any compatible registry |
| persistence.accessMode | string | `"ReadWriteOnce"` | Persistence access mode |
| persistence.enabled | bool | `false` | Use persistent volume to store data |
| persistence.keepPVC | bool | `false` | ## Keep a created Persistent volume claim when uninstalling the helm chart (default: false) |
| persistence.size | string | `"5Gi"` | Size of persistent volume claim |
| podAnnotations | object | `{}` | Pod annotations |
| podLabels | object | `{}` | Labels to add to the node-red pod. default: {} |
| podSecurityContext | object | `{"fsGroup":1000,"runAsUser":1000}` | Pod Security Context see [values.yaml](values.yaml) |
| podSecurityContext.fsGroup | int | `1000` | node-red group is 1000 |
| podSecurityContext.runAsUser | int | `1000` | node-red user is 1000 |
| rbac.createClusterRole | bool | `false` | Create a ClusterRole resource for the node-red pod. default: false |
| rbac.enabled | bool | `true` |  |
| readinessProbe | object | `{"httpGet":{"path":"/","port":"http"}}` | Readiness probe for the Deployment |
| resources | object | `{"limits":{"cpu":"500m","memory":"512Mi"},"requests":{"cpu":"100m","memory":"128Mi"}}` | CPU/Memory resource requests/limits |
| securityContext | object | `{"allowPrivilegeEscalation":false,"capabilities":{"drop":["ALL"]},"privileged":false,"readOnlyRootFilesystem":true,"runAsGroup":10003,"runAsNonRoot":true,"runAsUser":10003,"seccompProfile":{"type":"RuntimeDefault"}}` | Security Context see [values.yaml](values.yaml) |
| service.annotations | object | `{}` | Annotations for the service |
| service.port | int | `1880` | Kubernetes port where service is exposed |
| service.type | string | `"ClusterIP"` | Kubernetes service type |
| serviceAccount.annotations | object | `{}` | Additional ServiceAccount annotations |
| serviceAccount.create | bool | `true` | Create service account |
| serviceAccount.name | string | `""` | Service account name to use, when empty will be set to created account if |
| settings | object | `{}` | You can configure node-red using a settings file. default: {} |
| sidecar.enabled | bool | `false` | Enable the sidecar |
| sidecar.env.label | string | `"node-red-settings"` | Label that should be used for filtering |
| sidecar.env.label_value | string | `"1"` | The value for the label you want to filter your resources on. Don't set a value to filter by any value |
| sidecar.env.method | string | `"watch"` | If METHOD is set to LIST, the sidecar will just list config-maps/secrets and exit. With SLEEP it will list all config-maps/secrets, then sleep for SLEEP_TIME seconds. Anything else will continuously watch for changes (see https://kubernetes.io/docs/reference/using-api/api-concepts/#efficient-detection-of-changes). |
| sidecar.env.password | string | `""` | Password as key value pair |
| sidecar.env.passwordFromExistingSecret | object | `{}` | Password from existing secret |
| sidecar.env.script | string | `"flow_refresh.py"` | Absolute path to shell script to execute after a configmap got reloaded. |
| sidecar.env.sleep_time_sidecar | string | `"5s"` | Set the sleep time for refresh script |
| sidecar.env.username | string | `""` |  |
| sidecar.extraEnv | list | `[]` | Extra Environments for the sidecar |
| sidecar.extraNodeModules | list | `[]` | Extra Node-Modules that will be installed  from the sidecar script |
| sidecar.image.pullPolicy | string | `"IfNotPresent"` | The image pull policy, default: `IfNotPresent` |
| sidecar.image.registry | string | `"quay.io"` | The image registry to pull the sidecar from |
| sidecar.image.repository | string | `"kiwigrid/k8s-sidecar"` | The image repository to pull from |
| sidecar.image.tag | string | `"1.28.0"` | The image tag to pull, default: `1.28.0` |
| sidecar.resources | object | `{}` | Resources for the sidecar |
| sidecar.securityContext | object | `{}` | Security context for the sidecar |
| sidecar.volumeMounts | list | `[]` | The extra volume mounts for the sidecar |
| terminationGracePeriodSeconds | int | `30` | The terminationGracePeriodSeconds for the pod here we explicitly set the default value defined in kubernetes https://github.com/kubernetes/api/blob/d4b94f478bb2e6467873657dd7b4e1b0ac8351be/core/v1/types.go#L3114-L3118 |
| tolerations | list | `[]` | Toleration labels for pod assignment |

