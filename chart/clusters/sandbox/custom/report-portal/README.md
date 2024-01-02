# report-portal

![Version: 5.8.1](https://img.shields.io/badge/Version-5.8.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 5.8.1](https://img.shields.io/badge/AppVersion-5.8.1-informational?style=flat-square)

A Helm chart for report-portal

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | minio | 11.10.3 |
| https://charts.bitnami.com/bitnami | rabbitmq | 10.3.8 |
| https://helm.elastic.co | elasticsearch | 7.17.3 |
| https://reportportal.io/kubernetes | reportportal | 5.8.1 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| elasticsearch.replicas | int | `1` |  |
| elasticsearch.resources.requests.cpu | string | `"100m"` |  |
| elasticsearch.resources.requests.memory | string | `"2Gi"` |  |
| elasticsearch.volumeClaimTemplate.resources.requests.storage | string | `"3Gi"` |  |
| minio.auth.existingSecret | string | `"reportportal-minio-creds"` |  |
| minio.persistence.size | string | `"1Gi"` |  |
| rabbitmq.auth.existingErlangSecret | string | `"reportportal-rabbitmq-creds"` |  |
| rabbitmq.auth.existingPasswordSecret | string | `"reportportal-rabbitmq-creds"` |  |
| rabbitmq.persistence.size | string | `"1Gi"` |  |
| reportportal.elasticsearch.endpoint | string | `"http://elasticsearch-master.report-portal.svc.cluster.local:9200"` |  |
| reportportal.ingress.hosts[0] | string | `"report-portal.eks-sandbox.aws.main.edp.projects.epam.com"` |  |
| reportportal.ingress.usedomainname | bool | `true` |  |
| reportportal.postgresql.SecretName | string | `"reportportal-postgresql-creds"` |  |
| reportportal.postgresql.endpoint.address | string | `"postgresql-primary.report-portal.svc.cluster.local"` |  |
| reportportal.rabbitmq.SecretName | string | `"reportportal-rabbitmq-creds"` |  |
| reportportal.rabbitmq.endpoint.address | string | `"report-portal-rabbitmq.report-portal.svc.cluster.local"` |  |
| reportportal.rabbitmq.endpoint.apiuser | string | `"user"` |  |
| reportportal.rabbitmq.endpoint.user | string | `"user"` |  |
| reportportal.serviceanalyzer.resources.requests.cpu | string | `"50m"` |  |
| reportportal.serviceanalyzertrain.resources.requests.cpu | string | `"50m"` |  |
| reportportal.serviceapi.resources.requests.cpu | string | `"50m"` |  |
| reportportal.serviceindex.resources.requests.cpu | string | `"50m"` |  |
| reportportal.serviceui.resources.requests.cpu | string | `"50m"` |  |
| reportportal.storage.accesskeyName | string | `"root-user"` |  |
| reportportal.storage.endpoint | string | `"http://report-portal-minio.report-portal.svc.cluster.local:9000"` |  |
| reportportal.storage.endpointshort | string | `"report-portal-minio.report-portal.svc.cluster.local:9000"` |  |
| reportportal.storage.secretName | string | `"reportportal-minio-creds"` |  |
| reportportal.storage.secretkeyName | string | `"root-password"` |  |
| reportportal.storage.type | string | `"minio"` |  |
| reportportal.uat.resources.requests.cpu | string | `"50m"` |  |

