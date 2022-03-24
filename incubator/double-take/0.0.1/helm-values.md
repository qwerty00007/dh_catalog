# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"jakowenko/double-take"` |  |
| image.tag | string | `"1.7.0@sha256:6960ec3f20ae224badb2c3826198286227edd5c5af7edb2c95b5e9eff182fb9a"` |  |
| persistence.data.enabled | bool | `true` |  |
| persistence.data.mountPath | string | `"/.storage"` |  |
| service.main.ports.main.port | int | `10200` |  |
| service.main.ports.main.targetPort | int | `3000` |  |

All Rights Reserved - The TrueCharts Project
