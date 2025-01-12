# postgresql-ha

![Version: 8.6.13](https://img.shields.io/badge/Version-8.6.13-informational?style=flat-square) ![AppVersion: 11.15.0](https://img.shields.io/badge/AppVersion-11.15.0-informational?style=flat-square)

This PostgreSQL cluster solution includes the PostgreSQL replication manager, an open-source tool for managing replication and failover on PostgreSQL clusters.

**Homepage:** <https://github.com/bitnami/charts/tree/master/bitnami/postgresql-ha>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Bitnami | <containers@bitnami.com> |  |

## Source Code

* <https://github.com/bitnami/bitnami-docker-postgresql>
* <https://www.postgresql.org/>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| clusterDomain | string | `"cluster.local"` |  |
| commonAnnotations | object | `{}` |  |
| commonLabels | object | `{}` |  |
| diagnosticMode.args[0] | string | `"infinity"` |  |
| diagnosticMode.command[0] | string | `"sleep"` |  |
| diagnosticMode.enabled | bool | `false` |  |
| extraDeploy | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.imageRegistry | string | `""` |  |
| global.ldap.bindpw | string | `""` |  |
| global.ldap.existingSecret | string | `""` |  |
| global.pgpool.adminPassword | string | `""` |  |
| global.pgpool.adminUsername | string | `""` |  |
| global.pgpool.existingSecret | string | `""` |  |
| global.postgresql.database | string | `""` |  |
| global.postgresql.existingSecret | string | `""` |  |
| global.postgresql.password | string | `""` |  |
| global.postgresql.repmgrDatabase | string | `""` |  |
| global.postgresql.repmgrPassword | string | `""` |  |
| global.postgresql.repmgrUsername | string | `""` |  |
| global.postgresql.username | string | `""` |  |
| global.storageClass | string | `""` |  |
| ldap.base | string | `""` |  |
| ldap.binddn | string | `""` |  |
| ldap.bindpw | string | `""` |  |
| ldap.bslookup | string | `""` |  |
| ldap.enabled | bool | `false` |  |
| ldap.existingSecret | string | `""` |  |
| ldap.nssInitgroupsIgnoreusers | string | `"root,nslcd"` |  |
| ldap.scope | string | `""` |  |
| ldap.tlsReqcert | string | `""` |  |
| ldap.uri | string | `""` |  |
| metrics.annotations."prometheus.io/port" | string | `"9187"` |  |
| metrics.annotations."prometheus.io/scrape" | string | `"true"` |  |
| metrics.containerPort | int | `9187` |  |
| metrics.customMetrics | object | `{}` |  |
| metrics.enabled | bool | `false` |  |
| metrics.extraEnvVars | object | `{}` |  |
| metrics.livenessProbe.enabled | bool | `true` |  |
| metrics.livenessProbe.failureThreshold | int | `6` |  |
| metrics.livenessProbe.initialDelaySeconds | int | `30` |  |
| metrics.livenessProbe.periodSeconds | int | `10` |  |
| metrics.livenessProbe.successThreshold | int | `1` |  |
| metrics.livenessProbe.timeoutSeconds | int | `5` |  |
| metrics.readinessProbe.enabled | bool | `true` |  |
| metrics.readinessProbe.failureThreshold | int | `6` |  |
| metrics.readinessProbe.initialDelaySeconds | int | `5` |  |
| metrics.readinessProbe.periodSeconds | int | `10` |  |
| metrics.readinessProbe.successThreshold | int | `1` |  |
| metrics.readinessProbe.timeoutSeconds | int | `5` |  |
| metrics.resources.limits | object | `{}` |  |
| metrics.resources.requests | object | `{}` |  |
| metrics.securityContext.enabled | bool | `true` |  |
| metrics.securityContext.runAsUser | int | `1001` |  |
| metrics.service.clusterIP | string | `""` |  |
| metrics.service.externalTrafficPolicy | string | `"Cluster"` |  |
| metrics.service.loadBalancerIP | string | `""` |  |
| metrics.service.loadBalancerSourceRanges | list | `[]` |  |
| metrics.service.nodePort | string | `""` |  |
| metrics.service.port | int | `9187` |  |
| metrics.service.type | string | `"ClusterIP"` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| metrics.serviceMonitor.interval | string | `""` |  |
| metrics.serviceMonitor.metricRelabelings | list | `[]` |  |
| metrics.serviceMonitor.namespace | string | `""` |  |
| metrics.serviceMonitor.relabelings | list | `[]` |  |
| metrics.serviceMonitor.scrapeTimeout | string | `""` |  |
| metrics.serviceMonitor.selector.prometheus | string | `"kube-prometheus"` |  |
| metrics.startupProbe.enabled | bool | `false` |  |
| metrics.startupProbe.failureThreshold | int | `10` |  |
| metrics.startupProbe.initialDelaySeconds | int | `5` |  |
| metrics.startupProbe.periodSeconds | int | `10` |  |
| metrics.startupProbe.successThreshold | int | `1` |  |
| metrics.startupProbe.timeoutSeconds | int | `5` |  |
| metricsImage.debug | bool | `false` |  |
| metricsImage.pullPolicy | string | `"IfNotPresent"` |  |
| metricsImage.pullSecrets | list | `[]` |  |
| metricsImage.registry | string | `"docker.io"` |  |
| metricsImage.repository | string | `"bitnami/postgres-exporter"` |  |
| metricsImage.tag | string | `"0.10.1-debian-10-r87"` |  |
| nameOverride | string | `""` |  |
| networkPolicy.allowExternal | bool | `true` |  |
| networkPolicy.egressRules.customRules | list | `[]` |  |
| networkPolicy.egressRules.denyConnectionsToExternal | bool | `false` |  |
| networkPolicy.enabled | bool | `false` |  |
| persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.enabled | bool | `true` |  |
| persistence.existingClaim | string | `""` |  |
| persistence.mountPath | string | `"/bitnami/postgresql"` |  |
| persistence.selector | object | `{}` |  |
| persistence.size | string | `"8Gi"` |  |
| persistence.storageClass | string | `""` |  |
| pgpool.adminPassword | string | `""` |  |
| pgpool.adminUsername | string | `"admin"` |  |
| pgpool.affinity | object | `{}` |  |
| pgpool.args | list | `[]` |  |
| pgpool.childLifeTime | string | `""` |  |
| pgpool.childMaxConnections | string | `""` |  |
| pgpool.clientIdleLimit | string | `""` |  |
| pgpool.clientMinMessages | string | `"error"` |  |
| pgpool.command | list | `[]` |  |
| pgpool.configuration | string | `""` |  |
| pgpool.configurationCM | string | `""` |  |
| pgpool.connectionLifeTime | string | `""` |  |
| pgpool.containerPort | int | `5432` |  |
| pgpool.containerSecurityContext.enabled | bool | `true` |  |
| pgpool.containerSecurityContext.runAsUser | int | `1001` |  |
| pgpool.customLivenessProbe | object | `{}` |  |
| pgpool.customReadinessProbe | object | `{}` |  |
| pgpool.customStartupProbe | object | `{}` |  |
| pgpool.customUsers | object | `{}` |  |
| pgpool.customUsersSecret | string | `""` |  |
| pgpool.existingSecret | string | `""` |  |
| pgpool.extraEnvVars | list | `[]` |  |
| pgpool.extraEnvVarsCM | string | `""` |  |
| pgpool.extraEnvVarsSecret | string | `""` |  |
| pgpool.extraVolumeMounts | list | `[]` |  |
| pgpool.extraVolumes | list | `[]` |  |
| pgpool.hostAliases | list | `[]` |  |
| pgpool.initContainers | list | `[]` |  |
| pgpool.initdbScripts | object | `{}` |  |
| pgpool.initdbScriptsCM | string | `""` |  |
| pgpool.initdbScriptsSecret | string | `""` |  |
| pgpool.labels | object | `{}` |  |
| pgpool.lifecycleHooks | object | `{}` |  |
| pgpool.livenessProbe.enabled | bool | `true` |  |
| pgpool.livenessProbe.failureThreshold | int | `5` |  |
| pgpool.livenessProbe.initialDelaySeconds | int | `30` |  |
| pgpool.livenessProbe.periodSeconds | int | `10` |  |
| pgpool.livenessProbe.successThreshold | int | `1` |  |
| pgpool.livenessProbe.timeoutSeconds | int | `5` |  |
| pgpool.loadBalancingOnWrite | string | `"transaction"` |  |
| pgpool.logConnections | bool | `false` |  |
| pgpool.logHostname | bool | `true` |  |
| pgpool.logLinePrefix | string | `""` |  |
| pgpool.logPerNodeStatement | bool | `false` |  |
| pgpool.maxPool | string | `""` |  |
| pgpool.minReadySeconds | string | `""` |  |
| pgpool.nodeAffinityPreset.key | string | `""` |  |
| pgpool.nodeAffinityPreset.type | string | `""` |  |
| pgpool.nodeAffinityPreset.values | list | `[]` |  |
| pgpool.nodeSelector | object | `{}` |  |
| pgpool.numInitChildren | string | `""` |  |
| pgpool.passwords | string | `""` |  |
| pgpool.pdb.create | bool | `false` |  |
| pgpool.pdb.maxUnavailable | string | `""` |  |
| pgpool.pdb.minAvailable | int | `1` |  |
| pgpool.podAffinityPreset | string | `""` |  |
| pgpool.podAnnotations | object | `{}` |  |
| pgpool.podAntiAffinityPreset | string | `"soft"` |  |
| pgpool.podLabels | object | `{}` |  |
| pgpool.priorityClassName | string | `""` |  |
| pgpool.readinessProbe.enabled | bool | `true` |  |
| pgpool.readinessProbe.failureThreshold | int | `5` |  |
| pgpool.readinessProbe.initialDelaySeconds | int | `5` |  |
| pgpool.readinessProbe.periodSeconds | int | `5` |  |
| pgpool.readinessProbe.successThreshold | int | `1` |  |
| pgpool.readinessProbe.timeoutSeconds | int | `5` |  |
| pgpool.replicaCount | int | `1` |  |
| pgpool.reservedConnections | int | `1` |  |
| pgpool.resources.limits | object | `{}` |  |
| pgpool.resources.requests | object | `{}` |  |
| pgpool.securityContext.enabled | bool | `true` |  |
| pgpool.securityContext.fsGroup | int | `1001` |  |
| pgpool.serviceLabels | object | `{}` |  |
| pgpool.sidecars | list | `[]` |  |
| pgpool.srCheckDatabase | string | `"postgres"` |  |
| pgpool.startupProbe.enabled | bool | `false` |  |
| pgpool.startupProbe.failureThreshold | int | `10` |  |
| pgpool.startupProbe.initialDelaySeconds | int | `5` |  |
| pgpool.startupProbe.periodSeconds | int | `10` |  |
| pgpool.startupProbe.successThreshold | int | `1` |  |
| pgpool.startupProbe.timeoutSeconds | int | `5` |  |
| pgpool.tls.autoGenerated | bool | `false` |  |
| pgpool.tls.certCAFilename | string | `""` |  |
| pgpool.tls.certFilename | string | `""` |  |
| pgpool.tls.certKeyFilename | string | `""` |  |
| pgpool.tls.certificatesSecret | string | `""` |  |
| pgpool.tls.enabled | bool | `false` |  |
| pgpool.tls.preferServerCiphers | bool | `true` |  |
| pgpool.tolerations | list | `[]` |  |
| pgpool.updateStrategy | object | `{}` |  |
| pgpool.useLoadBalancing | bool | `true` |  |
| pgpool.usernames | string | `""` |  |
| pgpoolImage.debug | bool | `false` |  |
| pgpoolImage.pullPolicy | string | `"IfNotPresent"` |  |
| pgpoolImage.pullSecrets | list | `[]` |  |
| pgpoolImage.registry | string | `"docker.io"` |  |
| pgpoolImage.repository | string | `"bitnami/pgpool"` |  |
| pgpoolImage.tag | string | `"4.3.1-debian-10-r57"` |  |
| postgresql.affinity | object | `{}` |  |
| postgresql.args | list | `[]` |  |
| postgresql.audit.clientMinMessages | string | `"error"` |  |
| postgresql.audit.logConnections | bool | `false` |  |
| postgresql.audit.logDisconnections | bool | `false` |  |
| postgresql.audit.logHostname | bool | `true` |  |
| postgresql.audit.logLinePrefix | string | `""` |  |
| postgresql.audit.logTimezone | string | `""` |  |
| postgresql.audit.pgAuditLog | string | `""` |  |
| postgresql.audit.pgAuditLogCatalog | string | `"off"` |  |
| postgresql.command | list | `[]` |  |
| postgresql.configuration | string | `""` |  |
| postgresql.configurationCM | string | `""` |  |
| postgresql.containerPort | int | `5432` |  |
| postgresql.containerSecurityContext.enabled | bool | `true` |  |
| postgresql.containerSecurityContext.runAsUser | int | `1001` |  |
| postgresql.customLivenessProbe | object | `{}` |  |
| postgresql.customReadinessProbe | object | `{}` |  |
| postgresql.customStartupProbe | object | `{}` |  |
| postgresql.database | string | `""` |  |
| postgresql.dbUserConnectionLimit | string | `""` |  |
| postgresql.existingSecret | string | `""` |  |
| postgresql.extendedConf | string | `""` |  |
| postgresql.extendedConfCM | string | `""` |  |
| postgresql.extraEnvVars | list | `[]` |  |
| postgresql.extraEnvVarsCM | string | `""` |  |
| postgresql.extraEnvVarsSecret | string | `""` |  |
| postgresql.extraInitContainers | list | `[]` |  |
| postgresql.extraVolumeMounts | list | `[]` |  |
| postgresql.extraVolumes | list | `[]` |  |
| postgresql.hostAliases | list | `[]` |  |
| postgresql.hostIPC | bool | `false` |  |
| postgresql.hostNetwork | bool | `false` |  |
| postgresql.initContainers | list | `[]` |  |
| postgresql.initdbScripts | object | `{}` |  |
| postgresql.initdbScriptsCM | string | `""` |  |
| postgresql.initdbScriptsSecret | string | `""` |  |
| postgresql.labels | object | `{}` |  |
| postgresql.lifecycleHooks | object | `{}` |  |
| postgresql.livenessProbe.enabled | bool | `true` |  |
| postgresql.livenessProbe.failureThreshold | int | `6` |  |
| postgresql.livenessProbe.initialDelaySeconds | int | `30` |  |
| postgresql.livenessProbe.periodSeconds | int | `10` |  |
| postgresql.livenessProbe.successThreshold | int | `1` |  |
| postgresql.livenessProbe.timeoutSeconds | int | `5` |  |
| postgresql.maxConnections | string | `""` |  |
| postgresql.nodeAffinityPreset.key | string | `""` |  |
| postgresql.nodeAffinityPreset.type | string | `""` |  |
| postgresql.nodeAffinityPreset.values | list | `[]` |  |
| postgresql.nodeSelector | object | `{}` |  |
| postgresql.password | string | `""` |  |
| postgresql.pdb.create | bool | `false` |  |
| postgresql.pdb.maxUnavailable | string | `""` |  |
| postgresql.pdb.minAvailable | int | `1` |  |
| postgresql.pgHbaConfiguration | string | `""` |  |
| postgresql.pgHbaTrustAll | bool | `false` |  |
| postgresql.pghbaRemoveFilters | string | `""` |  |
| postgresql.podAffinityPreset | string | `""` |  |
| postgresql.podAnnotations | object | `{}` |  |
| postgresql.podAntiAffinityPreset | string | `"soft"` |  |
| postgresql.podLabels | object | `{}` |  |
| postgresql.postgresConnectionLimit | string | `""` |  |
| postgresql.postgresPassword | string | `""` |  |
| postgresql.priorityClassName | string | `""` |  |
| postgresql.readinessProbe.enabled | bool | `true` |  |
| postgresql.readinessProbe.failureThreshold | int | `6` |  |
| postgresql.readinessProbe.initialDelaySeconds | int | `5` |  |
| postgresql.readinessProbe.periodSeconds | int | `10` |  |
| postgresql.readinessProbe.successThreshold | int | `1` |  |
| postgresql.readinessProbe.timeoutSeconds | int | `5` |  |
| postgresql.replicaCount | int | `3` |  |
| postgresql.repmgrChildNodesCheckInterval | int | `5` |  |
| postgresql.repmgrChildNodesConnectedMinCount | int | `1` |  |
| postgresql.repmgrChildNodesDisconnectTimeout | int | `30` |  |
| postgresql.repmgrConfiguration | string | `""` |  |
| postgresql.repmgrConnectTimeout | int | `5` |  |
| postgresql.repmgrDatabase | string | `"repmgr"` |  |
| postgresql.repmgrFenceOldPrimary | bool | `false` |  |
| postgresql.repmgrLogLevel | string | `"NOTICE"` |  |
| postgresql.repmgrPassfilePath | string | `""` |  |
| postgresql.repmgrPassword | string | `""` |  |
| postgresql.repmgrReconnectAttempts | int | `2` |  |
| postgresql.repmgrReconnectInterval | int | `3` |  |
| postgresql.repmgrUsePassfile | string | `""` |  |
| postgresql.repmgrUsername | string | `"repmgr"` |  |
| postgresql.resources.limits | object | `{}` |  |
| postgresql.resources.requests | object | `{}` |  |
| postgresql.securityContext.enabled | bool | `true` |  |
| postgresql.securityContext.fsGroup | int | `1001` |  |
| postgresql.sharedPreloadLibraries | string | `"pgaudit, repmgr"` |  |
| postgresql.sidecars | list | `[]` |  |
| postgresql.startupProbe.enabled | bool | `false` |  |
| postgresql.startupProbe.failureThreshold | int | `10` |  |
| postgresql.startupProbe.initialDelaySeconds | int | `5` |  |
| postgresql.startupProbe.periodSeconds | int | `10` |  |
| postgresql.startupProbe.successThreshold | int | `1` |  |
| postgresql.startupProbe.timeoutSeconds | int | `5` |  |
| postgresql.statementTimeout | string | `""` |  |
| postgresql.syncReplication | bool | `false` |  |
| postgresql.tcpKeepalivesCount | string | `""` |  |
| postgresql.tcpKeepalivesIdle | string | `""` |  |
| postgresql.tcpKeepalivesInterval | string | `""` |  |
| postgresql.tls.certCAFilename | string | `""` |  |
| postgresql.tls.certFilename | string | `""` |  |
| postgresql.tls.certKeyFilename | string | `""` |  |
| postgresql.tls.certificatesSecret | string | `""` |  |
| postgresql.tls.enabled | bool | `false` |  |
| postgresql.tls.preferServerCiphers | bool | `true` |  |
| postgresql.tolerations | list | `[]` |  |
| postgresql.updateStrategyType | string | `"RollingUpdate"` |  |
| postgresql.upgradeRepmgrExtension | bool | `false` |  |
| postgresql.usePasswordFile | string | `""` |  |
| postgresql.usePgRewind | bool | `false` |  |
| postgresql.username | string | `"postgres"` |  |
| postgresqlImage.debug | bool | `false` |  |
| postgresqlImage.pullPolicy | string | `"IfNotPresent"` |  |
| postgresqlImage.pullSecrets | list | `[]` |  |
| postgresqlImage.registry | string | `"docker.io"` |  |
| postgresqlImage.repository | string | `"bitnami/postgresql-repmgr"` |  |
| postgresqlImage.tag | string | `"11.15.0-debian-10-r65"` |  |
| psp.create | bool | `false` |  |
| rbac.create | bool | `false` |  |
| service.annotations | object | `{}` |  |
| service.clusterIP | string | `""` |  |
| service.externalTrafficPolicy | string | `"Cluster"` |  |
| service.loadBalancerIP | string | `""` |  |
| service.loadBalancerSourceRanges | list | `[]` |  |
| service.nodePort | string | `""` |  |
| service.port | int | `5432` |  |
| service.portName | string | `"postgresql"` |  |
| service.serviceLabels | object | `{}` |  |
| service.sessionAffinity | string | `"None"` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.enabled | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| topologySpreadConstraints | object | `{}` |  |
| volumePermissions.enabled | bool | `false` |  |
| volumePermissions.resources.limits | object | `{}` |  |
| volumePermissions.resources.requests | object | `{}` |  |
| volumePermissions.securityContext.runAsUser | int | `0` |  |
| volumePermissionsImage.pullPolicy | string | `"IfNotPresent"` |  |
| volumePermissionsImage.pullSecrets | list | `[]` |  |
| volumePermissionsImage.registry | string | `"docker.io"` |  |
| volumePermissionsImage.repository | string | `"bitnami/bitnami-shell"` |  |
| volumePermissionsImage.tag | string | `"10-debian-10-r399"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
