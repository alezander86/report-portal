# edp-cluster-add-ons

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

EDP Cluster Addons that extend the Kubernetes Cluster Functionality

**Homepage:** <https://epam.github.io/edp-install/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| epmd-edp | <SupportEPMD-EDP@epam.com> | <https://solutionshub.epam.com/solution/epam-delivery-platform> |
| sergk |  | <https://github.com/SergK> |

## Source Code

* <https://github.com/epam/edp-cluster-add-ons>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| argo-cd.createNamespace | bool | `true` |  |
| argo-cd.enable | bool | `true` |  |
| argocd-app-project.createNamespace | bool | `false` |  |
| argocd-app-project.enable | bool | `true` |  |
| capsule.createNamespace | bool | `true` |  |
| capsule.enable | bool | `true` |  |
| destinationServer | string | `"in-cluster"` |  |
| extensions-oidc.createNamespace | bool | `true` |  |
| extensions-oidc.enable | bool | `true` |  |
| harbor-ha.createNamespace | bool | `true` |  |
| harbor-ha.enable | bool | `true` |  |
| ingress-nginx.createNamespace | bool | `false` |  |
| ingress-nginx.enable | bool | `true` |  |
| nexus-operator.createNamespace | bool | `true` |  |
| nexus-operator.enable | bool | `true` |  |
| nexus.createNamespace | bool | `true` |  |
| nexus.enable | bool | `true` |  |
| opensearch.createNamespace | bool | `true` |  |
| opensearch.enable | bool | `true` |  |
| postgres-operator.createNamespace | bool | `true` |  |
| postgres-operator.enable | bool | `true` |  |
| report-portal.createNamespace | bool | `true` |  |
| report-portal.enable | bool | `true` |  |
| sonar-operator.createNamespace | bool | `true` |  |
| sonar-operator.enable | bool | `true` |  |
| sonar.createNamespace | bool | `true` |  |
| sonar.enable | bool | `true` |  |
| vault-kms.createNamespace | bool | `true` |  |
| vault-kms.enable | bool | `true` |  |

