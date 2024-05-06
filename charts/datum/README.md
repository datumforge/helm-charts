# datum

![Version: 0.0.1](https://img.shields.io/badge/Version-0.0.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.2.3](https://img.shields.io/badge/AppVersion-0.2.3-informational?style=flat-square)

A Helm chart to deploy the Datum API server

## Requirements

Kubernetes: `>=1.24`

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 2.19.2 |
| https://charts.bitnami.com/bitnami | kafka | 28.2.0 |
| https://charts.bitnami.com/bitnami | redis | 19.1.5 |
| https://openfga.github.io/helm-charts | openfga | 0.2.3 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| api.affinity | object | `{}` |  |
| api.annotations | object | `{}` |  |
| api.commonAnnotations | object | `{}` |  |
| api.commonLabels | object | `{}` |  |
| api.datastore.sqlite.enabled | bool | `true` |  |
| api.datastore.sqlite.local.enabled | bool | `true` |  |
| api.datastore.sqlite.local.primary.storage.accessModes[0] | string | `"ReadWriteOnce"` |  |
| api.datastore.sqlite.local.primary.storage.size | string | `"1Gi"` |  |
| api.datastore.sqlite.local.secondary.enabled | bool | `true` |  |
| api.datastore.sqlite.local.secondary.storage.accessModes[0] | string | `"ReadWriteOnce"` |  |
| api.datastore.sqlite.local.secondary.storage.size | string | `"1Gi"` |  |
| api.imagePullSecrets | list | `[]` |  |
| api.labels | object | `{}` |  |
| api.livenessProbe.httpGet.path | string | `"/metrics"` |  |
| api.livenessProbe.httpGet.port | string | `"http"` |  |
| api.nodeSelector | object | `{}` |  |
| api.podAnnotations | object | `{}` |  |
| api.podLabels | object | `{}` |  |
| api.podSecurityContext | object | `{}` |  |
| api.readinessProbe.httpGet.path | string | `"/metrics"` |  |
| api.readinessProbe.httpGet.port | string | `"http"` |  |
| api.replicas | int | `1` |  |
| api.resources | object | `{}` |  |
| api.securityContext | object | `{}` |  |
| api.tolerations | list | `[]` |  |
| datum.auth.enabled | bool | `true` |  |
| datum.auth.providers.github.clientEndpoint | string | `"http://localhost:17608"` |  |
| datum.auth.providers.github.clientId | string | `""` |  |
| datum.auth.providers.github.clientSecret | string | `""` |  |
| datum.auth.providers.github.redirectUrl | string | `"/v1/github/callback"` |  |
| datum.auth.providers.github.scopes | string | `nil` |  |
| datum.auth.providers.google.clientEndpoint | string | `"http://localhost:17608"` |  |
| datum.auth.providers.google.clientId | string | `""` |  |
| datum.auth.providers.google.clientSecret | string | `""` |  |
| datum.auth.providers.google.redirectUrl | string | `"/v1/google/callback"` |  |
| datum.auth.providers.google.scopes | string | `nil` |  |
| datum.auth.providers.redirectUrl | string | `"http://localhost:3001/api/auth/callback/datum"` |  |
| datum.auth.providers.webauthn.debug | bool | `false` |  |
| datum.auth.providers.webauthn.displayName | string | `"Datum"` |  |
| datum.auth.providers.webauthn.enabled | bool | `true` |  |
| datum.auth.providers.webauthn.enforceTimeout | bool | `true` |  |
| datum.auth.providers.webauthn.maxDevices | int | `10` |  |
| datum.auth.providers.webauthn.relyingPartyId | string | `"localhost"` |  |
| datum.auth.providers.webauthn.requestOrigin | string | `"http://localhost:3001"` |  |
| datum.auth.providers.webauthn.timeout | int | `60000000000` |  |
| datum.auth.supportedProviders | string | `nil` |  |
| datum.auth.token.accessDuration | int | `3600000000000` |  |
| datum.auth.token.audience | string | `"https://datum.net"` |  |
| datum.auth.token.generateKeys | bool | `true` |  |
| datum.auth.token.issuer | string | `"https://auth.datum.net"` |  |
| datum.auth.token.jwksEndpoint | string | `"https://api.datum.net/.well-known/jwks.json"` |  |
| datum.auth.token.keys | string | `nil` |  |
| datum.auth.token.kid | string | `""` |  |
| datum.auth.token.refreshAudience | string | `""` |  |
| datum.auth.token.refreshDuration | int | `7200000000000` |  |
| datum.auth.token.refreshOverlap | int | `-900000000000` |  |
| datum.authz.createNewModel | bool | `false` |  |
| datum.authz.enabled | bool | `true` |  |
| datum.authz.hostUrl | string | `"https://authz.datum.net"` |  |
| datum.authz.modelFile | string | `"fga/model/datum.fga"` |  |
| datum.authz.modelId | string | `""` |  |
| datum.authz.storeId | string | `""` |  |
| datum.authz.storeName | string | `"datum"` |  |
| datum.db.catchTTL | int | `1000000000` |  |
| datum.db.databaseName | string | `"datum"` |  |
| datum.db.debug | bool | `false` |  |
| datum.db.driverName | string | `"libsql"` |  |
| datum.db.enableHistory | bool | `false` |  |
| datum.db.migrationProvider | string | `"atlas"` |  |
| datum.db.multiWrite | bool | `false` |  |
| datum.db.primaryDbSource | string | `"file:datum.db"` |  |
| datum.db.runMigrations | bool | `true` |  |
| datum.db.secondaryDbSource | string | `"file:backup.db"` |  |
| datum.email.adminEmail | string | `"admins@datum.net"` |  |
| datum.email.archive | string | `""` |  |
| datum.email.consoleUrl.consoleBase | string | `"https://console.datum.net"` |  |
| datum.email.consoleUrl.invite | string | `"/invite"` |  |
| datum.email.consoleUrl.reset | string | `"/password-reset"` |  |
| datum.email.consoleUrl.verify | string | `"/verify"` |  |
| datum.email.datumListId | string | `""` |  |
| datum.email.fromEmail | string | `"no-reply@datum.net"` |  |
| datum.email.marketingUrl.defaultSubscriptionOrg | string | `"Datum"` |  |
| datum.email.marketingUrl.marketingBase | string | `"https://www.datum.net"` |  |
| datum.email.marketingUrl.subscriberVerify | string | `"/verify"` |  |
| datum.email.sendGridApiKey | string | `""` |  |
| datum.email.testing | bool | `true` |  |
| datum.geodetic.baseUrl | string | `"http://localhost:1337"` |  |
| datum.geodetic.debug | bool | `false` |  |
| datum.geodetic.enabled | bool | `true` |  |
| datum.geodetic.endpoint | string | `"query"` |  |
| datum.objstorage.fs.enabled | bool | `false` |  |
| datum.objstorage.fs.root | string | `"./storage"` |  |
| datum.objstorage.gcs.bucket | string | `"yourbucketname"` |  |
| datum.objstorage.gcs.credentialsFile | string | `"./credentials.json"` |  |
| datum.objstorage.gcs.enabled | bool | `false` |  |
| datum.objstorage.s3.accessKeyID | string | `""` |  |
| datum.objstorage.s3.bucket | string | `"yourbucketname"` |  |
| datum.objstorage.s3.enabled | bool | `false` |  |
| datum.objstorage.s3.endpoint | string | `""` |  |
| datum.objstorage.s3.region | string | `"us-region-a"` |  |
| datum.objstorage.s3.secretAccessKey | string | `""` |  |
| datum.objstorage.s3.uploadConcurrency | string | `nil` |  |
| datum.posthog.apiKey | string | `""` |  |
| datum.posthog.enabled | bool | `false` |  |
| datum.posthog.host | string | `"https://app.posthog.com"` |  |
| datum.publisherConfig.address | string | `"localhost:10000"` |  |
| datum.publisherConfig.addresses[0] | string | `"localhost:10000"` |  |
| datum.publisherConfig.appName | string | `"datum"` |  |
| datum.publisherConfig.debug | bool | `false` |  |
| datum.publisherConfig.enabled | bool | `false` |  |
| datum.ratelimit.burst | int | `30` |  |
| datum.ratelimit.enabled | bool | `false` |  |
| datum.ratelimit.expires | int | `600000000000` |  |
| datum.ratelimit.limit | int | `10` |  |
| datum.redis.address | string | `"localhost:6379"` |  |
| datum.redis.db | int | `0` |  |
| datum.redis.dialTimeout | int | `5000000000` |  |
| datum.redis.enabled | bool | `true` |  |
| datum.redis.maxActiveConns | int | `0` |  |
| datum.redis.maxIdleConns | int | `0` |  |
| datum.redis.maxRetries | int | `3` |  |
| datum.redis.minIdleConns | int | `0` |  |
| datum.redis.name | string | `"datum"` |  |
| datum.redis.password | string | `""` |  |
| datum.redis.readTimeout | int | `0` |  |
| datum.redis.username | string | `""` |  |
| datum.redis.writeTimeout | int | `0` |  |
| datum.refreshInterval | int | `600000000000` |  |
| datum.sentry.attachStacktrace | bool | `true` |  |
| datum.sentry.debug | bool | `false` |  |
| datum.sentry.dsn | string | `""` |  |
| datum.sentry.enableTracing | bool | `false` |  |
| datum.sentry.enabled | bool | `false` |  |
| datum.sentry.environment | string | `"development"` |  |
| datum.sentry.profileSampleRate | float | `0.2` |  |
| datum.sentry.repanic | bool | `false` |  |
| datum.sentry.sampleRate | float | `0.2` |  |
| datum.sentry.serverName | string | `""` |  |
| datum.sentry.traceSampleRate | float | `0.2` |  |
| datum.sentry.traceSampler | int | `1` |  |
| datum.server.cacheControl.enabled | bool | `true` |  |
| datum.server.cacheControl.etagHeaders | string | `nil` |  |
| datum.server.cacheControl.noCacheHeaders | string | `nil` |  |
| datum.server.cors.allowOrigins | string | `nil` |  |
| datum.server.cors.cookieInsecure | bool | `false` |  |
| datum.server.cors.enabled | bool | `true` |  |
| datum.server.cors.prefixes | string | `nil` |  |
| datum.server.debug | bool | `false` |  |
| datum.server.dev | bool | `false` |  |
| datum.server.idleTimeout | int | `30000000000` |  |
| datum.server.listen | string | `":17608"` |  |
| datum.server.mime.defaultContentType | string | `"application/data"` |  |
| datum.server.mime.enabled | bool | `true` |  |
| datum.server.mime.mimeTypesFile | string | `""` |  |
| datum.server.readHeaderTimeout | int | `2000000000` |  |
| datum.server.readTimeout | int | `15000000000` |  |
| datum.server.redirect.code | int | `0` |  |
| datum.server.redirect.enabled | bool | `true` |  |
| datum.server.redirect.redirects | string | `nil` |  |
| datum.server.secure.contentsecuritypolicy | string | `"default-src 'self'"` |  |
| datum.server.secure.contenttypenosniff | string | `"nosniff"` |  |
| datum.server.secure.cspreportonly | bool | `false` |  |
| datum.server.secure.enabled | bool | `true` |  |
| datum.server.secure.hstsmaxage | int | `31536000` |  |
| datum.server.secure.hstspreloadenabled | bool | `false` |  |
| datum.server.secure.referrerpolicy | string | `"same-origin"` |  |
| datum.server.secure.xframeoptions | string | `"SAMEORIGIN"` |  |
| datum.server.secure.xssprotection | string | `"1; mode=block"` |  |
| datum.server.shutdownGracePeriod | int | `10000000000` |  |
| datum.server.tls.autoCert | bool | `false` |  |
| datum.server.tls.certFile | string | `"server.crt"` |  |
| datum.server.tls.certKey | string | `"server.key"` |  |
| datum.server.tls.config | string | `nil` |  |
| datum.server.tls.enabled | bool | `false` |  |
| datum.server.writeTimeout | int | `15000000000` |  |
| datum.sessions.encryptionKey | string | `"encryptionsecret"` |  |
| datum.sessions.signingKey | string | `"my-signing-secret"` |  |
| datum.totp.codeLength | int | `6` |  |
| datum.totp.enabled | bool | `true` |  |
| datum.totp.issuer | string | `"datum"` |  |
| datum.totp.recoveryCodeCount | int | `16` |  |
| datum.totp.recoveryCodeLength | int | `8` |  |
| datum.totp.redis | bool | `true` |  |
| datum.totp.secret | string | `""` |  |
| datum.tracer.enabled | bool | `false` |  |
| datum.tracer.environment | string | `"development"` |  |
| datum.tracer.otlp.certificate | string | `""` |  |
| datum.tracer.otlp.compression | string | `""` |  |
| datum.tracer.otlp.endpoint | string | `"localhost:4317"` |  |
| datum.tracer.otlp.headers | string | `nil` |  |
| datum.tracer.otlp.insecure | bool | `true` |  |
| datum.tracer.otlp.timeout | int | `10000000000` |  |
| datum.tracer.provider | string | `"stdout"` |  |
| datum.tracer.stdout.disableTimestamp | bool | `false` |  |
| datum.tracer.stdout.pretty | bool | `true` |  |
| extraServices | list | `[]` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/datumforge/datum"` |  |
| image.tag | string | `"1391-de0a31b1"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.extraHosts | list | `[]` |  |
| ingress.extraPaths | list | `[]` |  |
| ingress.extraTLS | list | `[]` |  |
| ingress.hostname | string | `"datum.example.com"` |  |
| ingress.labels | object | `{}` |  |
| ingress.selfSigned | bool | `false` |  |
| ingress.tls | bool | `true` |  |
| kafka.enabled | bool | `false` |  |
| kafka.image.repository | string | `"bitnami/kafka"` |  |
| kafka.image.tag | string | `"2.8.0"` |  |
| kafka.persistence.enabled | bool | `false` |  |
| kafka.persistence.size | string | `"1Gi"` |  |
| kafka.persistence.storageClass | string | `""` |  |
| kafka.replicas | int | `1` |  |
| kafka.zookeeper.enabled | bool | `false` |  |
| openfga.datastore.engine | string | `"memory"` |  |
| openfga.experimentals[0] | string | `"check-query-cache"` |  |
| openfga.playground.enabled | bool | `false` |  |
| openfga.replicaCount | int | `1` |  |
| redis.auth.enabled | bool | `false` |  |
| redis.enabled | bool | `true` |  |
| redis.image.tag | string | `"7.0.13-debian-11-r10"` |  |
| redis.master.nodeSelector | object | `{}` |  |
| redis.replica.nodeSelector | object | `{}` |  |
| redis.replica.replicaCount | int | `1` |  |
| service.annotations | object | `{}` |  |
| service.labels | object | `{}` |  |
| service.port | int | `17608` |  |
| service.portName | string | `"http"` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automountServiceAccountToken | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.imagePullSecrets | list | `[]` |  |
| serviceAccount.labels | object | `{}` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.13.1](https://github.com/norwoodj/helm-docs/releases/v1.13.1)
