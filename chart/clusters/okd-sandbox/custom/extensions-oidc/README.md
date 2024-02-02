# extensions-oidc

![Version: 1.20.0](https://img.shields.io/badge/Version-1.20.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.20.0](https://img.shields.io/badge/AppVersion-1.20.0-informational?style=flat-square)

A Helm chart for extensions-oidc

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://epam.github.io/edp-helm-charts/stable | keycloak-operator | 1.20.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| extensionsOIDC.keycloakUrl | string | `"https://keycloak.eks-core.aws.main.edp.projects.epam.com"` |  |
| extensionsOIDC.mainRealm.enabled | bool | `false` |  |
| extensionsOIDC.mainRealm.name | string | `"openshift"` |  |
| extensionsOIDC.sharedRealm | string | `"okd-sandbox"` |  |
| keycloak-operator.clusterReconciliationEnabled | bool | `true` |  |

