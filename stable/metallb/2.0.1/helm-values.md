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
| image.repository | string | `"placeholder"` |  |
| image.tag | string | `"upstream"` |  |
| metallb.configInline | object | `{}` |  format. When configInline is used, Helm manages MetalLB's configuration ConfigMap as part of the release, and existingConfigMap is ignored. Refer to https://metallb.universe.tf/configuration/ for available options. |

All Rights Reserved - The TrueCharts Project
