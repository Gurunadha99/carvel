# carvel
### Spark 

Apache Spark is a high-performance engine for large-scale computing tasks, such as data processing, machine learning and real-time data streaming. It includes APIs for Java, Python, Scala and R.

### Parameters

Configuration Reference

You can configure the following:

### Spark common parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|image.pullPolicy|MySQL image pull policy|string|IfNotPresent|
|master. replicas|set Master replicaset|integer|1|
|master.configurationConfigMap|Set a custom configuration by using an existing configMap with the configuration file|integer|""|
|master.webPort|Specify the port where the web interface will listen on the master over HTTP|integer|8080|
|master.webPortWithQuotes|Specify the port with quotes where the web interface will listen on the master over HTTP|integer|"8080"|
|master.webPortHttps|Specify the port where the web interface will listen on the master over HTTPS|integer|80|
|master.clustrePort|Specify the port where the master listens to communicate with workers|integer|7077|
|master.daemonMemoryLimit|Set the memory limit for the master daemon|integer|""|
|master.configOptions|Use a string to set the config options for in the form -Dx=y|integer|""|
|master.clustrePortWithQuotes|Specify the port  with quotes where the master listens to communicate with workers|integer|"7077"|
|master.prometheusPort|Specify the port prometheus.io/port|integer|'8080'|
|master.securityContext.enabled|Enable security context|string|TRUE|
|master.securityContext.fsGroup|Group ID for the container|integer|1001|
|master.securityContext.runAsUser|User ID for the container|integer|1001|
|master.securityContext.runAsGroup|Group ID for the container|integer|0|
|master.livenessProbe.enabled|Enable livenessProbe|string|true|
|master.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|180|
|master.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|20|
|master.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
|master.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|6|
|master.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|master.readinessProbe. enabled|Enable readinessProbe|string|true|
|master.readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|30|
|master.readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|10|
|master.readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|5|
|master.readinessProbe.failureThreshold|Failure threshold for readinessProbe|integer|6|
|master.readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|
|worker.webPort|Specify the port where the web interface will listen on the worker over HTTP|integer|8081|
|worker.webPortHttps|Specify the port where the web interface will listen on the worker over HTTPS|integer|8481|
|worker.webPortWithQuotes|Specify the port with quotes where the web interface will listen on the master over HTTP|integer|"8081"|
|worker.daemonMemoryLimit|Set the memory limit for the worker daemon|integer|""|
|worker.javaOptions|Set options for the JVM in the form -Dx=y|integer|""|
|worker.replicaCount|Number of spark workers (will be the minimum number when autoscaling is enabled)|integer|2|
|worker.podManagementPolicy|Statefulset Pod Management Policy Type|string|OrderedReady|
|worker.prometheusPort|Specify the port prometheus.io/port|integer|8081|
|worker.securityContext.enabled|Enable security context|string|TRUE|
|worker.securityContext.fsGroup|Group ID for the container|integer|1001|
|worker.securityContext.runAsUser|User ID for the container|integer|1001|
|worker.securityContext.runAsGroup|Group ID for the container|integer|0|
|worker.livenessProbe.enabled|Enable livenessProbe|string|TRUE|
|worker.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|180|
|worker.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|20|
|worker.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
|worker.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|6|
|worker.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|worker.readinessProbe.enabled|Enable readinessProbe|string|TRUE|
|worker.readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|30|
|worker.readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|10|
|worker.readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|5|
|worker.readinessProbe.failureThreshold|Failure threshold for readinessProbe|integer|6|
|worker.readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|
|worker.autoscaling.enabled|Enable replica autoscaling depending on CPU	|string|FALSE|
|worker.autoscaling.CpuTargetPercentag|	Kubernetes HPA CPU target percentage|integer|50|
|worker.autoscaling. replicasMax|Maximum number of workers when using autoscaling|integer|5|
|service.type	Kubernetes|Service type|string|ClusterIP|
|service.clusterPort|Spark clusterport|integer|7077|
|service.webPort|Spark client port for HTTP|integer|80|
|service.webPortHttps|Spark client port for HTTPS|integer|443|
|service.nodePorts.cluster|Kubernetes cluster node port|integer|""|
|service.nodePorts.web|Kubernetes web node port for HTTP|integer|""|
|service.nodePorts.webHttps|Kubernetes web node port for HTTPS|integer|""|
|service.loadBalancerIP|Load balancer IP if spark service type is LoadBalancer|integer|""|
|service.nodePorts.annotations|Annotations for spark service|integer|{}|
|ingress.enabled	|Enable ingress controller resource|strin|FALSE|
|ingress.pathType|Ingress path type|string|ImplementationSpecific|
|ingress. hostname|Default host for the ingress resource|string|spark.local|
|metrics.enabled|Enable metrics|string|FALSE|
