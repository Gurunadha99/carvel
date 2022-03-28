# carvel
Jenkins Package 

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|jenkinsUsername|Jenkins username|string|user|
|service.http|Jenkins service HTTP port|integer|80|
|service.https|Jenkins service HTTPs port|integer|443|
|persistentVolumeClaim.storage|Jenkins persistent volume size|string|8Gi|
|persistentVolumeClaim.storageClassName|Jenkins storage class name|string|default|
|imagePullPolicy|Jenkins image pull policy|string|IfNotPresent|
|jenkinsPassword|Jenkins userpassword|string|admin1|
|serviceAccountName|Jenkins pod service account name|string|default|
|metricsService.prometheus.io/port|Jenkins prometheus.io/port|integer|9122|
|metricsService.port|Jenkins exporter service port|integer|9122|
|metricsService.fsGroup|Set Jenkins Server pod's Security Context fsGroup|integer|1001|
|containerPorts.http|Jenkins  HTTP container port|integer|8080|
|containerPorts.https|Jenkins  HTTPs container port|integer|8443|
|container.securityContext.runAsNonRoot|Set Jenkins container's Security Context runAsNonRoot|boolean|TRUE|
|container.securityContext.runAsUser|Set Jenkins container's Security Context runAsUser|integer|1001|
|container.env.jenkinsHomepath|Jenkins home directory	string|/bitnami/jenkins/home|
|container.env.jenkinsHost|Set Jenkins Host|string|jenkins.local|
|container.env.jenkinsHttp|Set Jenkins HTTP External port|integer|80|
|container.env.jenkinsHttps|Set Jenkins HTTPs External port|integer|443|
|startupProbe.failureThreshold|Failure threshold for startupProbe|integer|6|
|startupProbe.initialDelaySeconds|Initial delay seconds for startupProbe|integer|180|
|startupProbe.periodSeconds|Period seconds for startupProbe|integer|10|
|startupProbe.successThreshold|Success threshold for startupProbe|integer|1|
|startupProbe.timeoutSeconds|Timeout seconds for startupProbe|integer|5|
|livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|180|
|livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|10|
|livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
|livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|6|
|livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|30|
|readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|5|
|readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|3|
|readinessProbe.failureThreshold|Failure seconds for readinessProbe|integer|3|
|readinessProbe.successThreshold|Success seconds for readinessProbe|integer|1|
|securityContext.runAsUser|Jenkins volumeMounts securityContext runAsUser|integer|1001|
|ports.containerPort|Jenkins container port|integer|9118|
|ports.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe volumeMounts|integer|15|
|ports.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe volumeMounts|integer	5|
|ports.readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe volumeMounts|integer	5|
|ports.readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe volumeMounts|integer|1|
|initContainers.enabled|		|boolean|FALSE|
|ingress.enabled|		|boolea|FALSE|
|ingress.host|Default host for the ingress record|string|jenkins.local|
|ingress.pathType|Ingress path type|string|ImplementationSpecific|
|metrics.enabled|		|boolean|FALSE|
|metrics.serviceMonitor.enabled| |boolean|FALSE|
