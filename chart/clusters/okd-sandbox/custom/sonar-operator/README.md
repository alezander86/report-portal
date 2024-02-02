# sonar-operator

![Version: 3.1.1](https://img.shields.io/badge/Version-3.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3.1.1](https://img.shields.io/badge/AppVersion-3.1.1-informational?style=flat-square)

A Helm chart for EDP Sonar Operator

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://epam.github.io/edp-helm-charts/stable | sonar-operator | 3.1.1 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| oidc.enabled | bool | `true` |  |
| oidc.keycloakRealm | string | `"okd-sandbox"` |  |
| oidc.keycloakUrl | string | `"https://keycloak.eks-core.aws.main.edp.projects.epam.com"` |  |
| sonar-operator.image.repository | string | `"epamedp/sonar-operator"` | EDP sonar-operator Docker image name. The released image can be found on [Dockerhub](https://hub.docker.com/r/epamedp/sonar-operator) |
| sonar-operator.image.tag | string | `"3.1.1"` | EDP sonar-operator Docker image tag. The released image can be found on [Dockerhub](https://hub.docker.com/r/epamedp/sonar-operator/tags) |
| sonar-operator.imagePullPolicy | string | `"IfNotPresent"` |  |
| sonar-operator.name | string | `"sonar-operator"` |  |
| sonar-operator.resources.limits.memory | string | `"192Mi"` |  |
| sonar-operator.resources.requests.cpu | string | `"50m"` |  |
| sonar-operator.resources.requests.memory | string | `"64Mi"` |  |
| sonarSecret | string | `"sonar-admin-password"` |  |
| sonarUrl | string | `"https://sonar.apps.okd-sandbox.aws.main.edp.projects.epam.com"` |  |

