# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.dictionaries | string | `"de_DE en_GB en_US es_ES fr_FR it nl pt_BR pt_PT ru"` |  |
| env.domain | string | `"nextcloud\\.domain\\.tld"` |  |
| env.extra_params | string | `"-o:welcome.enable=false -o:user_interface.mode=notebookbar -o:ssl.termination=true -o:ssl.enable=false"` |  |
| env.server_name | string | `"collabora\\.domain\\.tld"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/collabora"` |  |
| image.tag | string | `"v21.11.2.4.1@sha256:c87ee0a73f081f5987ed7eb4226fa208d5d0ecd6ac15e31fa1046194d01059b0"` |  |
| podSecurityContext.runAsGroup | int | `106` |  |
| podSecurityContext.runAsUser | int | `104` |  |
| secret.password | string | `"changeme"` |  |
| secret.username | string | `"admin"` |  |
| securityContext.allowPrivilegeEscalation | bool | `true` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| service.main.ports.main.port | int | `10105` |  |
| service.main.ports.main.targetPort | int | `9980` |  |

All Rights Reserved - The TrueCharts Project
