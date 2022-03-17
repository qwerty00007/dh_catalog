# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.REDMINE_DB_DATABASE | string | `"{{ .Values.postgresql.postgresqlDatabase }}"` |  |
| env.REDMINE_DB_PORT | string | `"5432"` |  |
| env.REDMINE_DB_USERNAME | string | `"{{ .Values.postgresql.postgresqlUsername }}"` |  |
| env.REDMINE_NO_DB_MIGRATE | string | `"{{ ternary \"true\" \"\" .Values.redmine.no_db_migrate }}"` |  |
| env.REDMINE_PLUGINS_MIGRATE | string | `"{{ ternary \"true\" \"\" .Values.redmine.plugins_migrate }}"` |  |
| envValueFrom.REDMINE_DB_PASSWORD.secretKeyRef.key | string | `"postgresql-password"` |  |
| envValueFrom.REDMINE_DB_PASSWORD.secretKeyRef.name | string | `"dbcreds"` |  |
| envValueFrom.REDMINE_DB_POSTGRES.secretKeyRef.key | string | `"plainhost"` |  |
| envValueFrom.REDMINE_DB_POSTGRES.secretKeyRef.name | string | `"dbcreds"` |  |
| envValueFrom.REDMINE_SECRET_KEY_BASE.secretKeyRef.key | string | `"REDMINE_SECRET_KEY_BASE"` |  |
| envValueFrom.REDMINE_SECRET_KEY_BASE.secretKeyRef.name | string | `"redmine-secrets"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/redmine"` |  |
| image.tag | string | `"v4.2.4@sha256:5dec2ce2ea609a1b59101ab4903efa5177082c6603d73e8d5b7e6a0136ccb42a"` |  |
| persistence.data.enabled | bool | `true` |  |
| persistence.data.mountPath | string | `"/usr/src/redmine/files"` |  |
| postgresql.enabled | bool | `true` |  |
| postgresql.existingSecret | string | `"dbcreds"` |  |
| postgresql.postgresqlDatabase | string | `"redmine"` |  |
| postgresql.postgresqlUsername | string | `"redmine"` |  |
| redmine.no_db_migrate | bool | `false` |  |
| redmine.plugins_migrate | bool | `true` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| service.main.ports.main.port | int | `10171` |  |
| service.main.ports.main.targetPort | int | `3000` |  |

All Rights Reserved - The TrueCharts Project
