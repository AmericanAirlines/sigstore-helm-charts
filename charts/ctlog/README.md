# ctlog

![Version: 0.2.50](https://img.shields.io/badge/Version-0.2.50-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.6.14](https://img.shields.io/badge/AppVersion-0.6.14-informational?style=flat-square)

Certificate Log

**Homepage:** <https://sigstore.dev/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| The Sigstore Authors |  |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| createctconfig.annotations | object | `{}` |  |
| createctconfig.backoffLimit | int | `6` |  |
| createctconfig.enabled | bool | `true` |  |
| createctconfig.fulcioURL | string | `"http://fulcio-server.fulcio-system.svc"` |  |
| createctconfig.image.pullPolicy | string | `"IfNotPresent"` |  |
| createctconfig.image.registry | string | `"ghcr.io"` |  |
| createctconfig.image.repository | string | `"sigstore/scaffolding/createctconfig"` |  |
| createctconfig.image.version | string | `"sha256:4e1446a12f32dd8e7bbc7a48c74579de329307feb5cd5e467b15d216ceb4ae45"` | v0.6.14 |
| createctconfig.initContainerImage.curl.imagePullPolicy | string | `"IfNotPresent"` |  |
| createctconfig.initContainerImage.curl.registry | string | `"docker.io"` |  |
| createctconfig.initContainerImage.curl.repository | string | `"curlimages/curl"` |  |
| createctconfig.initContainerImage.curl.version | string | `"sha256:4bfa3e2c0164fb103fb9bfd4dc956facce32b6c5d47cc09fcec883ce9535d5ac"` | 8.5.0 |
| createctconfig.logPrefix | string | `"sigstorescaffolding"` |  |
| createctconfig.name | string | `"createctconfig"` |  |
| createctconfig.privateKeyPasswordSecretName | string | `""` |  |
| createctconfig.privateSecret | string | `""` |  |
| createctconfig.pubkeysecret | string | `"ctlog-public-key"` |  |
| createctconfig.replicaCount | int | `1` |  |
| createctconfig.securityContext.runAsNonRoot | bool | `true` |  |
| createctconfig.securityContext.runAsUser | int | `65533` |  |
| createctconfig.serviceAccount.annotations | object | `{}` |  |
| createctconfig.serviceAccount.create | bool | `true` |  |
| createctconfig.serviceAccount.mountToken | bool | `true` |  |
| createctconfig.serviceAccount.name | string | `""` |  |
| createctconfig.ttlSecondsAfterFinished | int | `3600` |  |
| createtree.annotations | object | `{}` |  |
| createtree.displayName | string | `"ctlog-tree"` |  |
| createtree.enabled | bool | `true` |  |
| createtree.image.pullPolicy | string | `"IfNotPresent"` |  |
| createtree.image.registry | string | `"ghcr.io"` |  |
| createtree.image.repository | string | `"sigstore/scaffolding/createtree"` |  |
| createtree.image.version | string | `"sha256:fe4f41981fce2d6497b9f6a8e9dbdf3b0f3a5396feda6341090f363020ffb8bb"` |  |
| createtree.name | string | `"createtree"` |  |
| createtree.securityContext.runAsNonRoot | bool | `true` |  |
| createtree.securityContext.runAsUser | int | `65533` |  |
| createtree.serviceAccount.annotations | object | `{}` |  |
| createtree.serviceAccount.create | bool | `true` |  |
| createtree.serviceAccount.mountToken | bool | `true` |  |
| createtree.serviceAccount.name | string | `""` |  |
| createtree.ttlSecondsAfterFinished | int | `3600` |  |
| forceNamespace | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| namespace.create | bool | `false` |  |
| namespace.name | string | `"ctlog-system"` |  |
| server.config.key | string | `"treeID"` |  |
| server.config.treeID | string | `""` |  |
| server.extraArgs | list | `[]` |  |
| server.image.pullPolicy | string | `"IfNotPresent"` |  |
| server.image.registry | string | `"ghcr.io"` |  |
| server.image.repository | string | `"sigstore/scaffolding/ct_server"` |  |
| server.image.version | string | `"sha256:7a2f69676bbfe4d93554c662117e7520f9250684e60c2861dc62af6a18b01e18"` |  |
| server.ingress.annotations | object | `{}` |  |
| server.ingress.className | string | `"nginx"` |  |
| server.ingress.enabled | bool | `false` |  |
| server.ingress.hosts[0].path | string | `"/"` |  |
| server.ingress.tls | list | `[]` |  |
| server.ingresses[0].annotations | object | `{}` |  |
| server.ingresses[0].className | string | `"gce"` |  |
| server.ingresses[0].enabled | bool | `false` |  |
| server.ingresses[0].frontendConfigSpec.redirectToHttps.enabled | bool | `true` |  |
| server.ingresses[0].frontendConfigSpec.sslPolicy | string | `"ctlog-ssl-policy"` |  |
| server.ingresses[0].hosts[0].host | string | `"fulcio.localhost"` |  |
| server.ingresses[0].hosts[0].paths[0].path | string | `"/test"` |  |
| server.ingresses[0].hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| server.ingresses[0].hosts[0].paths[1].path | string | `"/other-shard"` |  |
| server.ingresses[0].hosts[0].paths[1].serviceName | string | `"other-shard"` |  |
| server.ingresses[0].name | string | `"gce-ingress"` |  |
| server.ingresses[0].staticGlobalIP | string | `"lb-ext-ip"` |  |
| server.ingresses[0].tls | list | `[]` |  |
| server.livenessProbe.httpGet.path | string | `"/healthz"` |  |
| server.livenessProbe.httpGet.port | int | `6962` |  |
| server.livenessProbe.initialDelaySeconds | int | `10` |  |
| server.podAnnotations."prometheus.io/path" | string | `"/metrics"` |  |
| server.podAnnotations."prometheus.io/port" | string | `"6963"` |  |
| server.podAnnotations."prometheus.io/scrape" | string | `"true"` |  |
| server.portHTTP | int | `6962` |  |
| server.portHTTPMetrics | int | `6963` |  |
| server.readinessProbe.httpGet.path | string | `"/healthz"` |  |
| server.readinessProbe.httpGet.port | int | `6962` |  |
| server.readinessProbe.initialDelaySeconds | int | `10` |  |
| server.replicaCount | int | `1` |  |
| server.securityContext.runAsNonRoot | bool | `true` |  |
| server.securityContext.runAsUser | int | `65533` |  |
| server.service.ports[0].name | string | `"6962-tcp"` |  |
| server.service.ports[0].port | int | `80` |  |
| server.service.ports[0].protocol | string | `"TCP"` |  |
| server.service.ports[0].targetPort | int | `6962` |  |
| server.service.ports[1].name | string | `"6963-tcp"` |  |
| server.service.ports[1].port | int | `6963` |  |
| server.service.ports[1].protocol | string | `"TCP"` |  |
| server.service.ports[1].targetPort | int | `6963` |  |
| server.service.type | string | `"ClusterIP"` |  |
| server.serviceAccount.annotations | object | `{}` |  |
| server.serviceAccount.create | bool | `true` |  |
| server.serviceAccount.mountToken | bool | `false` |  |
| server.serviceAccount.name | string | `""` |  |
| trillian.logServer.name | string | `"trillian-logserver"` |  |
| trillian.logServer.portRPC | int | `8091` |  |
| trillian.namespace | string | `"trillian-system"` |  |

