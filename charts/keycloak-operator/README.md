# keycloak-operator

![Version: 0.1.6](https://img.shields.io/badge/Version-0.1.6-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 13.0.0](https://img.shields.io/badge/AppVersion-13.0.0-informational?style=flat-square)

A Helm chart for the [Keycloak Operator](https://github.com/keycloak/keycloak-operator).

Based on the offical Kustomize install configuration (https://github.com/keycloak/keycloak-operator/tree/master/deploy).

```shell
$ helm repo add kubeist https://charts.kube.ist
$ helm search repo kubeist
$ helm install my-release kubeist/keycloak-operator
```

Documentation generated by [helm-docs](https://github.com/norwoodj/helm-docs): `helm-docs --sort-values-order file`.

Released with [chart-releaser](https://github.com/helm/chart-releaser).

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| nameOverride | string | `""` |  |
| fullnameOverride | string | `""` |  |
| singleNamespace | bool | `false` |  |
| installCRDs | bool | `true` |  |
| replicaCount | int | `1` |  |
| podAnnotations | object | `{}` | Annotations for the operator |
| imagePullSecrets | list | `[]` | Image Pull Secrets for the operator |
| affinity | object | `{}` | The operators Node/Pod Affinity |
| tolerations | list | `[]` | The operators tolerations |
| nodeSelector | object | `{}` | The operators node selector |
| priorityClassName | string | `""` | The operators priority |
| podSecurityContext | object | `{}` | The operators pod security context |
| resources | object | `{}` |  |
| image.repository | string | `"quay.io/keycloak/keycloak-operator"` | The operators image repository |
| image.pullPolicy | string | `"IfNotPresent"` | The operators image pull policy |
| image.tag | string | `"13.0.0"` | Overrides the image tag whose default is the chart version. |
| securityContext | object | `{}` | The operators security context |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.name | string | `""` | The name of the service account to use. |
| serviceAccount.rbac.create | bool | `true` | Should rbac rules be created |
| pdb.create | bool | `false` | Should we create a pdb |
| pdb.minAvailable | int | `1` |  |
| pdb.maxUnavailable | int | `1` |  |
