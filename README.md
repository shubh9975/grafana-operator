# grafana-operator package

## Configuration Reference
You can configure th|operator.updateStrategy.type|Set up update strategy for Grafana Operator installation.|string|Recreate|e following:

# Grafana Operator parameters
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|operator.enabled|Enable the deployment of the Grafana Operator|strng|true|
|operator.command|Default container command (useful when using custom images)|string|[]|
|operator.args|Default container args (useful when using custom images)|string|[]|
|operator.schedulerName|Alternative scheduler|string|""|
|operator.lifecycleHooks|for the grafana-operator container to automate configuration before or after startup|string|{}|
|operator.replicaCount|Number of grafana-operator Pod replicas|integer|1|
|operator.customLivenessProbe|Override default liveness probe|string|{}|
|operator.customReadinessProbe|Override default readiness probe|string|{}|
|operator.customStartupProbe|Override default startup probe|string|{}|
|operator.extraVolume|Grafana Operator image registry|string|Optionally specify extra list of additional volumes for etcd pods|string|[]|
|operator.extraVolumeMounts|Optionally specify extra list of additional volumeMounts for etcd container(s)|string|[]|
|operator.initContainers|Add additional init containers to the etcd pods|string|[]|
|operator.sidecars|Add additional sidecar containers to the etcd pods|string|[]|
|operator.watchNamespace|Override the namespace to watch|string|""|
|operator.topologySpreadConstraints|Topology Spread Constraints for pod assignment|string|[]|
|operator.priorityClassName|%%MAIN_CONTAINER_NAME%% pods' priorityClassName|string|""|
|operator.terminationGracePeriodSeconds|In seconds, time the given to the %%MAIN_CONTAINER_NAME%% pod needs to terminate gracefully|string|""|
|operator.updateStrategy.type|Set up update strategy for Grafana Operator installation.|string|Recreate|
|operator.image.registry|Grafana Operator image registry|string|docker.io|
|operator.image.repository|Grafana Operator image name|string|bitnami/grafana-operator|
|operator.image.tag|Grafana Operator image tag|string|4.4.1-debian-10-r10|
|operator.image.pullPolicy|Grafana Operator image pull policy|string|IfNotPresent|
|operator.image.pullSecrets|Grafana Operator image pull secrets|string|[]|
|operator.leaderElect|Enables or disables the operator leader Election.|string|true|
|operator.scanAllNamespaces|Specify if all namespace should be scanned for dashboards and datasources. (Creates ClusterRole)|string|false|
|operator.scanNamespaces|Specify the namespaces which should be scanned for dashboards and datasources (Creates ClusterRole)|string|[]|
|operator.zapDevel|Enable zap development mode (changes defaults to console encoder, debug log level, disables sampling and stacktrace from 'warning' level)|string|false|
|operator.zapEncoder|Zap log encoding ('json' or 'console')|string|""|
|operator.zapLevel|Zap log level (one of 'debug', 'info', 'error' or any integer value > 0) (default info)|string|""|
|operator.zapSample|Enable zap log sampling. Sampling will be disabled for integer log levels > 1|string|""|
|operator.zapStacktraceLevel|Set the minimum log level that triggers stacktrace generation (default error)|string|""|
|operator.zapTimeEncoding|Sets the zap time format ('epoch', 'millis', 'nano', or 'iso8601') (default )|string|""|
|operator.extraArgs|Extra arguments for the grafana operator (Evaluated as a template)|string|[]|
|operator.rbac.create|Create specifies whether to install and use RBAC rules|string|true|
|operator.serviceAccount.create|Specifies whether a service account should be created|string|true|
|operator.serviceAccount.name|The name of the service account to use. If not set and create is true, a name is generated using the fullname template|string|""|
|operator.serviceAccount.annotations|Add annotations|string|{}|
|operator.serviceAccount.automountServiceAccountToken|Automount API credentials for a service account.|string|true|
|operator.podSecurityContext.enabled|Enable pods security context|string|true|
|operator.podSecurityContext.runAsUser|User ID for the pods|integer|1001|
|operator.podSecurityContext.runAsGroup|User ID for the pods|integer|1001|
|operator.podSecurityContext.runAsNonRoot|Grafana Operator must run as nonRoot|string|true|
|operator.podSecurityContext.fsGroup|Group ID for the pods|integer|1001|
|operator.podSecurityContext.supplementalGroups|Which group IDs containers add|string|[]|
|operator.containerSecurityContext.enabled|Enable container security context|string|true|
|operator.containerSecurityContext.runAsUser|User ID for the operator container|integer|1001|
|operator.containerSecurityContext.runAsGroup|User ID for the operator container|integer|1001|
|operator.containerSecurityContext.runAsNonRoot|Force the container to be run as non-root|string|true|
|operator.containerSecurityContext.privileged|Decide if the container runs privileged.|string|false|
|operator.containerSecurityContext.readOnlyRootFilesystem|ReadOnlyRootFilesystem fot the operator container|string|false|
|operator.containerSecurityContext.allowPrivilegeEscalation|Allow Privilege Escalation for the operator container|string|false|
|operator.resources|Container resource requests and limits|string|{}|
|operator.containerPorts.metrics|Grafana Operator container port (used for metrics)|integer|8080|
|operator.hostAliases|Add deployment host aliases|string|[]|
|operator.extraEnvVars|Array with extra environment variables to add to RabbitMQ Cluster Operator nodes|string|[]|
|operator.extraEnvVarsCM|Name of existing ConfigMap containing extra env vars for RabbitMQ Cluster Operator nodes|string|""|
|operator.extraEnvVarsSecret|Name of existing Secret containing extra env vars for RabbitMQ Cluster Operator nodes|string|""|
|operator.podAffinityPreset|Pod affinity preset|string|""|
|operator.podAntiAffinityPreset|Pod anti-affinity preset. Allowed values: soft or hard|string|soft|
|operator.nodeAffinityPreset.type|Node affinity preset type. Allowed values: soft or hard|string|""|
|operator.nodeAffinityPreset.key|Set nodeAffinity preset key|string|""|
|operator.nodeAffinityPreset.values|Set nodeAffinity preset values|string|[]|
|operator.podAnnotations|Pod annotations|string|{}|
|operator.podLabels|Additional pod labels|string|{}|
|operator.nodeSelector|Node labels for pod assignment|string|{}|
|operator.tolerations|Tolerations for controller pod assignment|string|[]|
|operator.affinity|Affinity for controller pod assignment|string|{}|
|operator.prometheus.serviceMonitor.enabled|Specify if a ServiceMonitor will be deployed for prometheus-operator|string|false|
|operator.prometheus.serviceMonitor.namespace|Namespace for the ServiceMonitor Resource (defaults to the Release Namespace)|string|""|
|operator.prometheus.serviceMonitor.jobLabel|Specify the jobLabel to use for the prometheus-operator|string|app.kubernetes.io/name|
|operator.prometheus.serviceMonitor.interval|Scrape interval. If not set, the Prometheus default scrape interval is used|string|""|
|operator.prometheus.serviceMonitor.scrapeTimeout|Timeout after which the scrape is ended|string|""|
|operator.prometheus.serviceMonitor.metricRelabelings|Specify additional relabeling of metrics|string|[]|
|operator.prometheus.serviceMonitor.relabelings|Specify general relabeling|string|[]|
|operator.prometheus.serviceMonitor.selector|ServiceMonitor selector labels|string|{}|
|operator.prometheus.serviceMonitor.labels|Extra labels for the ServiceMonitor|string|{}|
|operator.prometheus.serviceMonitor.honorLabels|honorLabels chooses the metric's labels on collisions with target labels|string|false|
|operator.livenessProbe.enabled|Enable livenessProbe|string|true|
|operator.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|10|
|operator.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|10|
|operator.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|1|
|operator.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|3|
|operator.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
