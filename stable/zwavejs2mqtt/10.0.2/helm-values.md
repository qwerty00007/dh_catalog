# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | `{}` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/zwavejs2mqtt"` |  |
| image.tag | string | `"v6.5.2@sha256:3cd8e650865bcc8b16adfceb4e51dfd185f3f910ce5b428e165d23229296d6ea"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/usr/src/app/store"` |  |
| probes.liveness.enabled | bool | `true` |  |
| probes.readiness.enabled | bool | `true` |  |
| probes.startup.enabled | bool | `false` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| service.main.ports.main.port | int | `8091` |  |
| service.main.ports.main.targetPort | int | `8091` |  |
| service.ws.enabled | bool | `true` |  |
| service.ws.ports.ws.enabled | bool | `true` |  |
| service.ws.ports.ws.port | int | `10046` |  |
| service.ws.ports.ws.targetPort | int | `3000` |  |

All Rights Reserved - The TrueCharts Project
