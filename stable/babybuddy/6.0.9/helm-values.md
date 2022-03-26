# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.DB_ENGINE | string | `"django.db.backends.postgresql"` |  |
| env.DB_NAME | string | `"{{ .Values.postgresql.postgresqlDatabase }}"` |  |
| env.DB_PORT | string | `"5432"` |  |
| env.DB_USER | string | `"{{ .Values.postgresql.postgresqlUsername }}"` |  |
| envValueFrom.DB_HOST.secretKeyRef.key | string | `"plainhost"` |  |
| envValueFrom.DB_HOST.secretKeyRef.name | string | `"dbcreds"` |  |
| envValueFrom.DB_PASSWORD.secretKeyRef.key | string | `"postgresql-password"` |  |
| envValueFrom.DB_PASSWORD.secretKeyRef.name | string | `"dbcreds"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/babybuddy"` |  |
| image.tag | string | `"v1.10.2@sha256:e496893090c978f20512c7ccdfd6a23b67f1c50a2f18e51684d9a8290079afcc"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/config"` |  |
| persistence.varrun.enabled | bool | `true` |  |
| podSecurityContext.runAsGroup | int | `0` |  |
| podSecurityContext.runAsUser | int | `0` |  |
| postgresql.enabled | bool | `true` |  |
| postgresql.existingSecret | string | `"dbcreds"` |  |
| postgresql.postgresqlDatabase | string | `"babybuddy"` |  |
| postgresql.postgresqlUsername | string | `"babybuddy"` |  |
| securityContext.allowPrivilegeEscalation | bool | `true` |  |
| securityContext.runAsNonRoot | bool | `false` |  |
| service.main.ports.main.port | int | `10069` |  |
| service.main.ports.main.targetPort | int | `8000` |  |

All Rights Reserved - The TrueCharts Project
