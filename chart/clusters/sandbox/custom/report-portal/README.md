# report-portal

![Version: 5.7.2](https://img.shields.io/badge/Version-5.7.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 5.7.2](https://img.shields.io/badge/AppVersion-5.7.2-informational?style=flat-square)

A Helm chart for report-portal

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | minio | 11.10.3 |
| https://charts.bitnami.com/bitnami | rabbitmq | 10.3.8 |
| https://helm.elastic.co | elasticsearch | 7.17.3 |
| https://raw.githubusercontent.com/bitnami/charts/archive-full-index/bitnami | postgresql | 10.9.4 |
| https://reportportal.io/kubernetes | reportportal | 5.7.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| elasticsearch.extraEnvs[0].name | string | `"discovery.type"` |  |
| elasticsearch.extraEnvs[0].value | string | `"single-node"` |  |
| elasticsearch.extraEnvs[1].name | string | `"cluster.initial_master_nodes"` |  |
| elasticsearch.extraEnvs[1].value | string | `""` |  |
| elasticsearch.replicas | int | `1` |  |
| elasticsearch.resources.requests.cpu | string | `"100m"` |  |
| elasticsearch.resources.requests.memory | string | `"2Gi"` |  |
| elasticsearch.volumeClaimTemplate.resources.requests.storage | string | `"3Gi"` |  |
| minio.auth.existingSecret | string | `"reportportal-minio-creds"` |  |
| minio.persistence.size | string | `"1Gi"` |  |
| postgresql.existingSecret | string | `"reportportal-postgresql-creds"` |  |
| postgresql.initdbScripts."init_postgres.sh" | string | `"#!/bin/sh\n/opt/bitnami/postgresql/bin/psql -U postgres -d ${POSTGRES_DB} -c 'CREATE EXTENSION IF NOT EXISTS ltree; CREATE EXTENSION IF NOT EXISTS pgcrypto; CREATE EXTENSION IF NOT EXISTS pg_trgm;'\n"` |  |
| postgresql.persistence.size | string | `"1Gi"` |  |
| postgresql.postgresqlDatabase | string | `"reportportal"` |  |
| postgresql.postgresqlUsername | string | `"rpuser"` |  |
| postgresql.resources.requests.cpu | string | `"100m"` |  |
| rabbitmq.auth.existingErlangSecret | string | `"reportportal-rabbitmq-creds"` |  |
| rabbitmq.auth.existingPasswordSecret | string | `"reportportal-rabbitmq-creds"` |  |
| rabbitmq.persistence.size | string | `"1Gi"` |  |
| reportportal.elasticsearch.endpoint | string | `"http://elasticsearch-master.report-portal.svc.cluster.local:9200"` |  |
| reportportal.ingress.hosts[0] | string | `"report-portal.eks-test.aws.main.edp.projects.epam.com"` |  |
| reportportal.ingress.usedomainname | bool | `true` |  |
| reportportal.minio.accesskeyName | string | `"root-user"` |  |
| reportportal.minio.endpoint | string | `"http://sandbox-minio.report-portal.svc.cluster.local:9000"` |  |
| reportportal.minio.endpointshort | string | `"sandbox-minio.report-portal.svc.cluster.local:9000"` |  |
| reportportal.minio.secretName | string | `"reportportal-minio-creds"` |  |
| reportportal.minio.secretkeyName | string | `"root-password"` |  |
| reportportal.postgresql.SecretName | string | `"reportportal-postgresql-creds"` |  |
| reportportal.postgresql.endpoint.address | string | `"sandbox-postgresql.report-portal.svc.cluster.local"` |  |
| reportportal.rabbitmq.SecretName | string | `"reportportal-rabbitmq-creds"` |  |
| reportportal.rabbitmq.endpoint.address | string | `"sandbox-rabbitmq.report-portal.svc.cluster.local"` |  |
| reportportal.rabbitmq.endpoint.apiuser | string | `"user"` |  |
| reportportal.rabbitmq.endpoint.user | string | `"user"` |  |
| reportportal.serviceanalyzer.resources.requests.cpu | string | `"50m"` |  |
| reportportal.serviceanalyzertrain.resources.requests.cpu | string | `"50m"` |  |
| reportportal.serviceapi.resources.requests.cpu | string | `"50m"` |  |
| reportportal.serviceindex.resources.requests.cpu | string | `"50m"` |  |
| reportportal.serviceui.resources.requests.cpu | string | `"50m"` |  |
| reportportal.uat.resources.requests.cpu | string | `"50m"` |  |

