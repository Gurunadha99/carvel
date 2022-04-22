# carvel
Mysql Package 
MySQL is a fast, reliable, scalable, and easy to use open source relational database system. Designed to handle mission-critical, heavy-load production applications

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|image.pullPolicy|MySQL image pull policy|string|IfNotPresent|
|auth.rootPassword|Password for the root user Ignored if existing secret is provided|string|admin1|
|auth.Password|Password for the new user Ignored if existing secret is provided	string|mysqlpassword|
|primary.podSecurityContext.fsGroup|Group ID for the mounted volumes filesystem|integer|1001|
|primary.containerSecurityContext.runAsUser|User ID for the MySQL primary container|integer|1001|
|primary.livenessProbe.enabled|Enable livenessProbe|string|true|
|primary.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|5|
|primary.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|10|
|primary.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|1|
|primary.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|3|
|primary.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|primary.readinessProbe.enabled|Enable readinessProbe	string|true|
|primary.readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|5|
|primary.readinessProbe.periodSeconds	|Period seconds for readinessProbe|integer|10|
|primary.readinessProbe.timeoutSeconds	|Timeout seconds for readinessProbe|	integer|	1|
|primary.readinessProbe.failureThreshold	|Failure threshold for readinessProbe	|integer|	3|
|primary.readinessProbe.successThreshold	|Success threshold for readinessProbe|	integer|	1|
|primary.startupProbe.enabled|Enable startupProbe|string|true|
|primary.startupProbe.initialDelaySeconds|Initial delay seconds for startupProbe|integer|15|
|primary.startupProbe.periodSeconds	|Period seconds for startupProbe	|integer|	10|
|primary.startupProbe.timeoutSeconds	|Timeout seconds for startupProbe	|integer|	1|
|primary.startupProbe.failureThreshold	|Failure threshold for startupProbe|	integer	10|
|primary.startupProbe.successThreshold	|Success threshold for startupProbe|integer|1|
|secondary.replicaCount	|Number of MySQL secondary replicas	|integer	|1|
|primary.persistence.size	|MySQL primary persistent volume size|	integer|8Gi|
|metrics.enabled	|Start a side-car prometheus exporter	|string|false|
|metrics.service.port|	MySQL Prometheus Exporter service port|	integer|9104|
|metrics.livenessProbe. enabled	|Enable livenessProbe	|string|true|
|metrics.livenessProbe.initialDelaySeconds	|Initial delay seconds for livenessProbe|integer|120|
|metrics.livenessProbe.periodSeconds	|Period seconds for livenessProbe	|integer	|10|
|metrics.livenessProbe.timeoutSeconds	|Timeout seconds for livenessProbe|	integer|	1|
|metrics.livenessProbe.failureThreshold	|Failure threshold for livenessProbe|	integer|	3|
|metrics.livenessProbe.successThreshold	|Success threshold for livenessProbe|	integer|	1|
|metrics. readinessProbe.enabled	|Enable readinessProbe	|string|true|
|metrics.readinessProbe.initialDelaySeconds|	Initial delay seconds for readinessProbe|integer|30|
|metrics.readinessProbe.periodSeconds	|Period seconds for readinessProbe	|integer|	10|
|metrics.readinessProbe. timeoutSeconds	|Timeout seconds for readinessProbe|	integer|	1|
|metrics.readinessProbe.failureThreshold	|Failure threshold for readinessProbe	|integer|	3|
|metrics.readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|
|networkpolicy.enabled|Enable networkpolicy|string|false|
|initContainers.enabled|Enable initContainers|string|false|



