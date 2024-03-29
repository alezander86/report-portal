# nexus

![Version: 61.0.2](https://img.shields.io/badge/Version-61.0.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3.61.0](https://img.shields.io/badge/AppVersion-3.61.0-informational?style=flat-square)

A Helm chart for Nexus

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://oauth2-proxy.github.io/manifests/ | oauth2-proxy | 6.16.1 |
| https://sonatype.github.io/helm3-charts/ | nexus-repository-manager | 61.0.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| nexus-repository-manager.deployment.initContainers[0].command[0] | string | `"mkdir"` |  |
| nexus-repository-manager.deployment.initContainers[0].command[1] | string | `"-p"` |  |
| nexus-repository-manager.deployment.initContainers[0].command[2] | string | `"/nexus-data/etc"` |  |
| nexus-repository-manager.deployment.initContainers[0].image | string | `"busybox"` |  |
| nexus-repository-manager.deployment.initContainers[0].imagePullPolicy | string | `"IfNotPresent"` |  |
| nexus-repository-manager.deployment.initContainers[0].name | string | `"fmp-volume-permission"` |  |
| nexus-repository-manager.deployment.initContainers[0].securityContext.runAsUser | int | `1000750000` |  |
| nexus-repository-manager.deployment.initContainers[0].volumeMounts[0].mountPath | string | `"/nexus-data"` |  |
| nexus-repository-manager.deployment.initContainers[0].volumeMounts[0].name | string | `"nexus-data"` |  |
| nexus-repository-manager.fullnameOverride | string | `"nexus"` |  |
| nexus-repository-manager.nameOverride | string | `"nexus"` |  |
| nexus-repository-manager.nexus.env[0].name | string | `"NEXUS_SECURITY_RANDOMPASSWORD"` |  |
| nexus-repository-manager.nexus.env[0].value | string | `"false"` |  |
| nexus-repository-manager.nexus.properties.data."jetty.request.header.size" | int | `100000` |  |
| nexus-repository-manager.nexus.properties.data."nexus.scripts.allowCreation" | bool | `true` |  |
| nexus-repository-manager.nexus.properties.override | bool | `true` |  |
| nexus-repository-manager.nexus.resources.limits.memory | string | `"6Gi"` |  |
| nexus-repository-manager.nexus.resources.requests.cpu | string | `"100m"` |  |
| nexus-repository-manager.nexus.resources.requests.memory | string | `"2Gi"` |  |
| nexus-repository-manager.nexus.securityContext.fsGroup | int | `1000750000` |  |
| nexus-repository-manager.nexus.securityContext.runAsGroup | int | `1000750000` |  |
| nexus-repository-manager.nexus.securityContext.runAsUser | int | `1000750000` |  |
| nexus-repository-manager.persistence.enabled | bool | `true` |  |
| nexus-repository-manager.persistence.storageSize | string | `"30Gi"` |  |
| nexus-repository-manager.route.enabled | bool | `true` |  |
| nexus-repository-manager.route.name | string | `"nexus"` |  |
| nexus-repository-manager.route.path | string | `"nexus-ci.apps.okd-sandbox.aws.main.edp.projects.epam.com"` |  |
| nexus-repository-manager.route.portName | string | `"nexus-ui"` |  |
| nexus-repository-manager.service.name | string | `"nexus"` |  |
| nexus-repository-manager.service.portName | string | `"nexus-ui"` |  |
| nexus-repository-manager.serviceAccount.name | string | `"nexus-repo"` |  |
| oauth2-proxy.config.configFile | string | `"allowed_roles = [\"administrator\", \"developer\"]\nclient_id = \"nexus\"\ncode_challenge_method=\"S256\"\ncookie_csrf_expire=\"5m\"\ncookie_csrf_per_request=\"true\"\ncookie_secure = \"false\"\nemail_domains = [ \"*\" ]\ninsecure_oidc_allow_unverified_email = \"true\"\noidc_issuer_url = \"https://keycloak.eks-core.aws.main.edp.projects.epam.com/auth/realms/okd-sandbox\"\npass_access_token = \"true\"\npass_authorization_header = \"true\"\npass_basic_auth = \"false\"\nprovider = \"keycloak-oidc\"\nredirect_url = \"https://nexus.apps.okd-sandbox.aws.main.edp.projects.epam.com/oauth2/callback\"\nskip_jwt_bearer_tokens = \"true\"\nupstreams = [ \"http://nexus:8081\" ]\nwhitelist_domains = [\"*\"]"` |  |
| oauth2-proxy.config.existingSecret | string | `"oauth2-proxy"` |  |
| oauth2-proxy.ingress.annotations."route.openshift.io/termination" | string | `"edge"` |  |
| oauth2-proxy.ingress.enabled | bool | `true` |  |
| oauth2-proxy.ingress.hosts[0] | string | `"nexus.apps.okd-sandbox.aws.main.edp.projects.epam.com"` |  |
| oauth2-proxy.securityContext.fsGroup | int | `1000750001` |  |
| oauth2-proxy.securityContext.runAsGroup | int | `1000750001` |  |
| oauth2-proxy.securityContext.runAsUser | int | `1000750001` |  |
| oauth2-proxy.serviceAccount.name | string | `"nexus-oauth2-proxy"` |  |

