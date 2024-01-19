# nexus-operator

![Version: 2.17.0](https://img.shields.io/badge/Version-2.17.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.17.0](https://img.shields.io/badge/AppVersion-2.17.0-informational?style=flat-square)

A Helm chart for EDP Nexus Operator

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://epam.github.io/edp-helm-charts/stable | nexus-operator | 2.17.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| nexus-operator.global.admins | list | `["artem_zahumonnyi@epam.com","iryna_churkina@epam.com","mykola_marusenko@epam.com","mykola_serdiuk@epam.com","mykyta_derhunov@epam.com","oleksandr_stepanov@epam.com","oleksandr_taruraiev@epam.com","sergiy_kulanov@epam.com","serhii_fomenko@epam.com","vladyslav_palyvoda@epam.com","zorian_motso@epam.com","andriy_trubitsyn@epam.com"]` | Administrators of your tenant |
| nexus-operator.global.dnsWildCard | string | `"eks-sandbox.aws.main.edp.projects.epam.com"` | a cluster DNS wildcard name |
| nexus-operator.global.edpName | string | `"nexus"` | namespace or a project name (in case of OpenShift) |
| nexus-operator.global.keycloakUrl | string | `"https://keycloak.eks-core.aws.main.edp.projects.epam.com"` | Keycloak Endpoint which is used for SSO integration. Format https://keycloak.example.com |
| nexus-operator.global.platform | string | `"kubernetes"` | platform type that can be "kubernetes" or "openshift" |
| nexus-operator.nexus.deploy | bool | `false` | Flag to enable/disable Nexus deploy |
| nexus-operator.nexusCR.create | bool | `true` | Specifies whether Nexus CR should be created |
| nexus-operator.oauth2_proxy.enabled | bool | `false` | Install oauth2-proxy as a part of nexus deployment. Default: true |

