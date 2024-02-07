# nexus-repository-manager

![Version: 61.0.2](https://img.shields.io/badge/Version-61.0.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3.61.0](https://img.shields.io/badge/AppVersion-3.61.0-informational?style=flat-square)

Sonatype Nexus Repository Manager - Universal Binary repository

**Homepage:** <https://www.sonatype.com/nexus-repository-oss>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Sonatype | <support@sonatype.com> |  |

## Source Code

* <https://github.com/sonatype/nexus-public>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| config.data | list | `[]` |  |
| config.enabled | bool | `false` |  |
| config.mountPath | string | `"/sonatype-nexus-conf"` |  |
| deployment.additionalContainers | string | `nil` |  |
| deployment.additionalVolumeMounts | string | `nil` |  |
| deployment.additionalVolumes | string | `nil` |  |
| deployment.annotations | object | `{}` |  |
| deployment.initContainers | string | `nil` |  |
| deployment.postStart.command | string | `nil` |  |
| deployment.preStart.command | string | `nil` |  |
| deployment.terminationGracePeriodSeconds | int | `120` |  |
| deploymentStrategy | string | `"Recreate"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"sonatype/nexus3"` |  |
| image.tag | string | `"3.61.0"` |  |
| imagePullSecrets | string | `nil` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/proxy-body-size" | string | `"0"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hostPath | string | `"/"` |  |
| ingress.hostRepo | string | `"repo.demo"` |  |
| ingress.ingressClassName | string | `"nginx"` |  |
| nameOverride | string | `""` |  |
| nexus.docker.enabled | bool | `false` |  |
| nexus.env[0].name | string | `"INSTALL4J_ADD_VM_PARAMS"` |  |
| nexus.env[0].value | string | `"-Xms2703M -Xmx2703M\n-XX:MaxDirectMemorySize=2703M\n-XX:+UnlockExperimentalVMOptions\n-XX:+UseCGroupMemoryLimitForHeap\n-Djava.util.prefs.userRoot=/nexus-data/javaprefs"` |  |
| nexus.env[1].name | string | `"NEXUS_SECURITY_RANDOMPASSWORD"` |  |
| nexus.env[1].value | string | `"true"` |  |
| nexus.hostAliases | list | `[]` |  |
| nexus.livenessProbe.failureThreshold | int | `6` |  |
| nexus.livenessProbe.initialDelaySeconds | int | `30` |  |
| nexus.livenessProbe.path | string | `"/"` |  |
| nexus.livenessProbe.periodSeconds | int | `30` |  |
| nexus.livenessProbe.timeoutSeconds | int | `10` |  |
| nexus.nexusPort | int | `8081` |  |
| nexus.podAnnotations | object | `{}` |  |
| nexus.properties.data."nexus.scripts.allowCreation" | bool | `true` |  |
| nexus.properties.override | bool | `false` |  |
| nexus.readinessProbe.failureThreshold | int | `6` |  |
| nexus.readinessProbe.initialDelaySeconds | int | `30` |  |
| nexus.readinessProbe.path | string | `"/"` |  |
| nexus.readinessProbe.periodSeconds | int | `30` |  |
| nexus.readinessProbe.timeoutSeconds | int | `10` |  |
| nexus.resources | string | `nil` |  |
| nexus.securityContext.fsGroup | int | `200` |  |
| nexus.securityContext.runAsGroup | int | `200` |  |
| nexus.securityContext.runAsUser | int | `200` |  |
| nexusProxyRoute.annotations | string | `nil` |  |
| nexusProxyRoute.enabled | bool | `false` |  |
| nexusProxyRoute.labels | string | `nil` |  |
| persistence.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.enabled | bool | `true` |  |
| persistence.storageSize | string | `"8Gi"` |  |
| route.annotations | string | `nil` |  |
| route.enabled | bool | `false` |  |
| route.labels | string | `nil` |  |
| route.name | string | `"docker"` |  |
| route.portName | string | `"docker"` |  |
| secret.data | list | `[]` |  |
| secret.enabled | bool | `false` |  |
| secret.mountPath | string | `"/etc/secret-volume"` |  |
| secret.readOnly | bool | `true` |  |
| service.annotations | object | `{}` |  |
| service.enabled | bool | `true` |  |
| service.labels | object | `{}` |  |
| service.name | string | `"nexus3"` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| statefulset.enabled | bool | `false` |  |
| tolerations | list | `[]` |  |

