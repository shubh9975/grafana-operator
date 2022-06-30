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
|operator.extraVolumes|Optionally specify extra list of additional volumes for etcd pods|string|[]|
|operator.extraVolumeMounts|Optionally specify extra list of additional volumeMounts for etcd container(s)|string|[]|
|operator.initContainers|Add additional init containers to the etcd pods|string|[]|
|operator.sidecars|Add additional sidecar containers to the etcd pods|string|[]|
|operator.watchNamespace|Override the namespace to watch|string|""|
|operator.topologySpreadConstraints|Topology Spread Constraints for pod assignment|string|[]|
|operator.priorityClassName|%%MAIN_CONTAINER_NAME%% pods' priorityClassName|string|""|
|operator.terminationGracePeriodSeconds|In seconds, time the given to the %%MAIN_CONTAINER_NAME%% pod needs to terminate gracefully|string|""|
|operator.updateStrategy.type|Set up update strategy for Grafana Operator installation.|string|Recreate|
