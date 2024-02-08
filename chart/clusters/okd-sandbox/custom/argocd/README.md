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
| argo-cd.configs.params."application.namespaces" | string | `"edp-delivery-okd-gerrit-qa, edp-delivery-okd-github-qa, edp-delivery-okd-gitlab-qa, edp-delivery-okd-jenkins-qa, edp-delivery-okd-sit, edp-delivery-okd-qa, edp-delivery-az-delivery-dev, edp-delivery-okd-sit-okd, edp-delivery-okd-qa-okd, edp-delivery-okd-shared-qa-okd-shared, edp-delivery-okd-shared-sit-okd-shared, edp-delivery-ms-delivery-dev, edp-delivery-okd-qa-qa"` |  |
| argo-cd.controller.enableStatefulSet | bool | `true` |  |
| argo-cd.dex.enabled | bool | `false` |  |
| argo-cd.redis-ha.enabled | bool | `true` |  |
| argo-cd.repoServer.replicas | int | `2` |  |
| argo-cd.repoServer.serviceAccount.name | string | `"argocd-repo-server"` |  |
| argo-cd.server.config."application.instanceLabelKey" | string | `"argocd.argoproj.io/instance-edp"` |  |
| argo-cd.server.config."oidc.config" | string | `"name: Keycloak\nissuer: https://keycloak.eks-core.aws.main.edp.projects.epam.com/auth/realms/okd-sandbox\nclientID: argocd-tenant\nclientSecret: $keycloak-client-argocd-secret:clientSecret\nrequestedScopes:\n  - openid\n  - profile\n  - email\n  - groups\n"` |  |
| argo-cd.server.config.url | string | `"https://argocd-dev.apps.okd-sandbox.aws.main.edp.projects.epam.com"` |  |
| argo-cd.server.env[0].name | string | `"ARGOCD_API_SERVER_REPLICAS"` |  |
| argo-cd.server.env[0].value | string | `"2"` |  |
| argo-cd.server.extraArgs[0] | string | `"--insecure"` |  |
| argo-cd.server.rbacConfig."policy.csv" | string | `"# default global admins\ng, ArgoCDAdmins, role:admin\n"` |  |
| argo-cd.server.rbacConfig."policy.default" | string | `""` |  |
| argo-cd.server.rbacConfig.scopes | string | `"[groups]"` |  |
| argo-cd.server.replicas | int | `2` |  |
| oidc.enabled | bool | `true` |  |

