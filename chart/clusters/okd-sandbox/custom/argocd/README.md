# argo-cd

![Version: 5.55.0](https://img.shields.io/badge/Version-5.55.0-informational?style=flat-square) ![AppVersion: v2.10.0](https://img.shields.io/badge/AppVersion-v2.10.0-informational?style=flat-square)

A Helm chart for Argo CD Install

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://argoproj.github.io/argo-helm | argo-cd | 5.55.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| argo-cd.applicationSet.enabled | bool | `true` |  |
| argo-cd.configs.cm."application.instanceLabelKey" | string | `"argocd.argoproj.io/instance-edp"` |  |
| argo-cd.configs.cm."oidc.config" | string | `"name: Keycloak\nissuer: https://keycloak.eks-core.aws.main.edp.projects.epam.com/auth/realms/okd-sandbox\nclientID: argocd-tenant\nclientSecret: $keycloak-client-argocd-secret:clientSecret\nrequestedScopes:\n  - openid\n  - profile\n  - email\n  - groups\n"` |  |
| argo-cd.configs.cm.url | string | `"https://argocd-dev.apps.okd-sandbox.aws.main.edp.projects.epam.com"` |  |
| argo-cd.configs.params."application.namespaces" | string | `"edp-delivery-ot-delivery-dev, edp-delivery-mm-delivery-dev, edp-delivery-okd-qa-okd, edp-delivery-az-delivery-dev, edp-delivery-okd-sit-okd, edp-delivery-vp-dev, edp-delivery-sk-dev, edp-delivery-ms-delivery-dev, edp-delivery-okd-qa-qa, edp-delivery-zm-dev, edp-delivery-os-dev, edp-delivery-sf-dev, edp-delivery-vp-dev,"` |  |
| argo-cd.configs.params."applicationsetcontroller.allowed.scm.providers" | string | `"https://git.example.com/,https://gitlab.example.com/"` |  |
| argo-cd.configs.params."applicationsetcontroller.enable.scm.providers" | string | `"false"` |  |
| argo-cd.configs.params."applicationsetcontroller.namespaces" | string | `"edp-delivery-ot-delivery-dev, edp-delivery-mm-delivery-dev, edp-delivery-okd-qa-okd, edp-delivery-az-delivery-dev, edp-delivery-okd-sit-okd, edp-delivery-vp-dev, edp-delivery-sk-dev, edp-delivery-ms-delivery-dev, edp-delivery-okd-qa-qa, edp-delivery-zm-dev, edp-delivery-os-dev, edp-delivery-sf-dev, edp-delivery-vp-dev,"` |  |
| argo-cd.configs.params."server.insecure" | bool | `true` |  |
| argo-cd.configs.rbac."policy.csv" | string | `"# default global admins\ng, Administrator, role:admin\n# Default global developers\ng, Developer, role:readonly\n"` |  |
| argo-cd.configs.rbac.scopes | string | `"[groups]"` |  |
| argo-cd.configs.secret.createSecret | bool | `true` | Create the argocd-secret |
| argo-cd.controller.enableStatefulSet | bool | `true` |  |
| argo-cd.dex.enabled | bool | `false` |  |
| argo-cd.notifications.enabled | bool | `false` |  |
| argo-cd.redis-ha.enabled | bool | `true` |  |
| argo-cd.redis.enabled | bool | `false` |  |
| argo-cd.server.env[0].name | string | `"ARGOCD_API_SERVER_REPLICAS"` |  |
| argo-cd.server.env[0].value | string | `"1"` |  |
| argo-cd.server.replicas | int | `1` |  |
| oidc.enabled | bool | `true` |  |

