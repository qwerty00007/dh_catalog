# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.CLEAN_TMP_DIR | int | `1` |  |
| env.DISPLAY_HEIGHT | int | `768` |  |
| env.DISPLAY_WIDTH | int | `1280` |  |
| env.KEEP_APP_RUNNING | int | `0` |  |
| env.PUID | int | `568` |  |
| env.SECURE_CONNECTION | int | `0` |  |
| env.USER_ID | string | `"{{ .Values.env.PUID }}"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/jdownloader-2"` |  |
| image.tag | string | `"v1.7.1@sha256:ba37e3a795f6e64466de3e81152af78c5fe8f6c3beeeee5a2bc948c41a631b16"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/config"` |  |
| podSecurityContext.runAsGroup | int | `0` |  |
| podSecurityContext.runAsUser | int | `0` |  |
| secret.VNC_PASSWORD | string | `""` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| securityContext.runAsNonRoot | bool | `false` |  |
| service.main.ports.main.port | int | `10054` |  |
| service.main.ports.main.targetPort | int | `5800` |  |
| service.myjd.enabled | bool | `true` |  |
| service.myjd.ports.myjd.enabled | bool | `true` |  |
| service.myjd.ports.myjd.port | int | `3129` |  |
| service.myjd.ports.myjd.targetPort | int | `3129` |  |
| service.vnc.enabled | bool | `true` |  |
| service.vnc.ports.vnc.enabled | bool | `true` |  |
| service.vnc.ports.vnc.port | int | `10056` |  |
| service.vnc.ports.vnc.targetPort | int | `5900` |  |

All Rights Reserved - The TrueCharts Project
