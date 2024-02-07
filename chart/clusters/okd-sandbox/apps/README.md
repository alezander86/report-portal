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
| argocd.createNamespace | bool | `true` |  |
| argocd.enable | bool | `true` |  |
| destinationServer | string | `"okd-sandbox"` |  |
| extensionsOIDC.createNamespace | bool | `true` |  |
| extensionsOIDC.enable | bool | `true` |  |
| harborHAOKD.createNamespace | bool | `true` |  |
| harborHAOKD.enable | bool | `true` |  |
| nexus-okd.createNamespace | bool | `true` |  |
| nexus-okd.enable | bool | `true` |  |
| nexusOperator.createNamespace | bool | `true` |  |
| nexusOperator.enable | bool | `true` |  |
| postgres-operator.createNamespace | bool | `true` |  |
| postgres-operator.enable | bool | `true` |  |
| sonar-operator.createNamespace | bool | `true` |  |
| sonar-operator.enable | bool | `true` |  |
| sonar.createNamespace | bool | `true` |  |
| sonar.enable | bool | `true` |  |
| vault.createNamespace | bool | `true` |  |
| vault.enable | bool | `true` |  |

