# sonar-operator

![Version: 2.14.0-RC.5](https://img.shields.io/badge/Version-2.14.0--RC.5-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.14.0-RC.5](https://img.shields.io/badge/AppVersion-2.14.0--RC.5-informational?style=flat-square)

A Helm chart for EDP Sonar Operator

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://epam.github.io/edp-helm-charts/snapshot | sonar-operator | 2.14.0-RC.5 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| keycloak.realm | string | `"okd-sandbox"` |  |
| keycloak.url | string | `"keycloak.eks-core.aws.main.edp.projects.epam.com"` |  |
| sonar-operator.global.dnsWildCard | string | `"apps.okd-sandbox.aws.main.edp.projects.epam.com"` | a cluster DNS wildcard name |
| sonar-operator.global.edpName | string | `"sonar"` | namespace or a project name (in case of OpenShift) |
| sonar-operator.global.openshift.deploymentType | string | `"deployments"` | Wich type of kind will be deployed to Openshift (values: deployments/deploymentConfigs) |
| sonar-operator.global.platform | string | `"openshift"` | platform type that can be "kubernetes" or "openshift" |
| sonar-operator.image.repository | string | `"epamedp/sonar-operator"` | EDP sonar-operator Docker image name. The released image can be found on [Dockerhub](https://hub.docker.com/r/epamedp/sonar-operator) |
| sonar-operator.image.tag | string | `"2.14.0-RC.5"` | EDP sonar-operator Docker image tag. The released image can be found on [Dockerhub](https://hub.docker.com/r/epamedp/sonar-operator/tags) |
| sonar-operator.name | string | `"sonar-operator"` | component name |
| sonar-operator.sonar.deploy | bool | `false` | Flag to enable/disable Sonar deploy |

