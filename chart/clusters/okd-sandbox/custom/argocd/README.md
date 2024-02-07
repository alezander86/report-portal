# argo-cd

![Version: 5.52.1](https://img.shields.io/badge/Version-5.52.1-informational?style=flat-square) ![AppVersion: v2.9.3](https://img.shields.io/badge/AppVersion-v2.9.3-informational?style=flat-square)

A Helm chart for Argo CD Install

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://argoproj.github.io/argo-helm | argo-cd | 5.52.1 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configs.params."application.namespaces" | string | `"edp-delivery-okd-gerrit-qa, edp-delivery-okd-github-qa, edp-delivery-okd-gitlab-qa, edp-delivery-okd-jenkins-qa, edp-delivery-okd-sit, edp-delivery-okd-qa, edp-delivery-az-delivery-dev, edp-delivery-okd-sit-okd, edp-delivery-okd-qa-okd, edp-delivery-okd-shared-qa-okd-shared, edp-delivery-okd-shared-sit-okd-shared, edp-delivery-ms-delivery-dev, edp-delivery-okd-qa-qa"` |  |
| controller.enableStatefulSet | bool | `true` |  |
| dex.enabled | bool | `false` |  |
| redis-ha.enabled | bool | `true` |  |
| repoServer.replicas | int | `2` |  |
| server.config."application.instanceLabelKey" | string | `"argocd.argoproj.io/instance-edp"` |  |
| server.config."oidc.config".clientID | string | `"argocd-tenant"` |  |
| server.config."oidc.config".clientSecret | string | `"$argocd-secret:clientSecret"` |  |
| server.config."oidc.config".issuer | string | `"https://keycloak.apps.okd-sandbox.aws.main.edp.projects.epam.com/auth/realms/control-plane"` |  |
| server.config."oidc.config".name | string | `"Keycloak"` |  |
| server.config."oidc.config".requestedScopes[0] | string | `"openid"` |  |
| server.config."oidc.config".requestedScopes[1] | string | `"profile"` |  |
| server.config."oidc.config".requestedScopes[2] | string | `"email"` |  |
| server.config."oidc.config".requestedScopes[3] | string | `"groups"` |  |
| server.config.url | string | `"https://argocd.apps.okd-sandbox.aws.main.edp.projects.epam.com"` |  |
| server.env[0].name | string | `"ARGOCD_API_SERVER_REPLICAS"` |  |
| server.env[0].value | string | `"2"` |  |
| server.extraArgs[0] | string | `"--insecure"` |  |
| server.rbacConfig."policy.csv" | string | `"# default global admins\ng, ArgoCDAdmins, role:admin\n"` |  |
| server.rbacConfig."policy.default" | string | `""` |  |
| server.rbacConfig.scopes | string | `"[groups]"` |  |
| server.replicas | int | `2` |  |
| server.route.enabled | bool | `true` |  |
| server.route.hostname | string | `"argocd.apps.okd-sandbox.aws.main.edp.projects.epam.com"` |  |
| server.route.termination_policy | string | `"Redirect"` |  |
| server.route.termination_type | string | `"edge"` |  |

