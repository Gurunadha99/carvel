# carvel
### InfluxDB

InfluxDB(TM) is an open source time-series database. It is a core component of the TICK (Telegraf, InfluxDB(TM), Chronograf, Kapacitor) stack.

Overview of InfluxDB™

InfluxDB(TM) is a trademark owned by InfluxData, which is not affiliated with, and does not endorse, this site.

### Parameters

Configuration Reference

You can configure the following:

### InfluxDB parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|auth.adminPassword|InfluxDB admin user's password|string|mypassword|
|auth.adminToken|nfluxDB admin-user-token|string|""|
|influxdb.replica|set influxdb replicaset|integer|1|
|influxdb.securityContext.fsGroup|Set InfluxDB pod's Security Context fsGroup|integer|1001|
|influxdb.securityContext.runAsUser|Set InfluxDB containers Security Context runAsUser|integer|0|
|influxdb.containers.securityContext.runAsNonRoot|Set Controller container's Security Context runAsNonRoot|string|true|
|influxdb.containers.securityContext.runAsUser|Set InfluxDB containers' Security Context runAsUser|integer|1001|
|influxdb.containers.ports.http|InfluxDB container HTTP port|integer|8086|
|influxdb.containers.ports.rpc|InfluxDB container RPC port|integer|8088|
|influxdb.livenessProbe.enabled|Enable livenessProbe|string|true|
|influxdb.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|180|
|influxdb.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|45|
|influxdb.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|30|
|influxdb.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|6|
|influxdb.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|influxdb.readinessProbe.enabled|Enable readinessProbe|string|true|
|influxdb.readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|60|
|influxdb.readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|45|
|influxdb.readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|30|
|influxdb.readinessProbe.failureThreshold|Failure threshold for readinessProbe|integer|6|
|influxdb.readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|
|service.type|Influxdb Kubernetes Service type|string|LoadBalancer|
|service.http|container HTTP port|integer|8086|
|service.rpc|container RPC port|integer|8088|

### Exposing parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|ingress.enabled|Enable ingress|string|false|

### Metrics parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|networkPolicy.enabled|Enable networkPolicy|string|false|
|networkPolicy.ports.http|enabled networkpolicy ingress inbound ports|integer|8086|
|networkPolicy.ports.rpc|enabled networkpolicy ingress tcp ports|integer|8088|
|pvc.storage|Size of data volume|string|8Gi|
|serviceMetrics.prometheus.io/port|Prometheus port|integer|9122|
|serviceMetrics.port|Service Metrics http port|integer|9122|





