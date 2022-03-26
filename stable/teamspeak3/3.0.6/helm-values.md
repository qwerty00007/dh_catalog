# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.TS3SERVER_LICENSE | string | `"accept"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/teamspeak"` |  |
| image.tag | string | `"v3.13.6@sha256:5de10cc5953c908ca92fb7662f16b9a88e8dd6b2f7d54705f2126df0bd595688"` |  |
| persistence.data.enabled | bool | `true` |  |
| persistence.data.mountPath | string | `"/var/ts3server"` |  |
| podSecurityContext.runAsGroup | int | `0` |  |
| podSecurityContext.runAsUser | int | `0` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| securityContext.runAsNonRoot | bool | `false` |  |
| service.files.enabled | bool | `true` |  |
| service.files.ports.files.enabled | bool | `true` |  |
| service.files.ports.files.port | int | `30033` |  |
| service.files.ports.files.targetPort | int | `30033` |  |
| service.main.ports.main.port | int | `10011` |  |
| service.main.ports.main.targetPort | int | `10011` |  |
| service.voice.enabled | bool | `true` |  |
| service.voice.ports.voice.enabled | bool | `true` |  |
| service.voice.ports.voice.port | int | `9987` |  |
| service.voice.ports.voice.protocol | string | `"UDP"` |  |
| service.voice.ports.voice.targetPort | int | `9987` |  |

All Rights Reserved - The TrueCharts Project
