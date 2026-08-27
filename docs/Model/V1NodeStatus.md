# V1NodeStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**addresses** | [**\Kubernetes\Client\Model\V1NodeAddress[]**](V1NodeAddress.md) | List of addresses reachable to the node. Queried from cloud provider, if available. More info: https://kubernetes.io/docs/reference/node/node-status/#addresses Note: This field is declared as mergeable, but the merge key is not sufficiently unique, which can cause data corruption when it is merged. Callers should instead use a full-replacement patch. See https://pr.k8s.io/79391 for an example. Consumers should assume that addresses can change during the lifetime of a Node. However, there are some exceptions where this may not be possible, such as Pods that inherit a Node&#39;s address in its own status or consumers of the downward API (status.hostIP). | [optional]
**allocatable** | **array<string,string>** | Allocatable represents the resources of a node that are available for scheduling. Defaults to Capacity. | [optional]
**capacity** | **array<string,string>** | Capacity represents the total resources of a node. More info: https://kubernetes.io/docs/reference/node/node-status/#capacity | [optional]
**conditions** | [**\Kubernetes\Client\Model\V1NodeCondition[]**](V1NodeCondition.md) | Conditions is an array of current observed node conditions. More info: https://kubernetes.io/docs/reference/node/node-status/#condition | [optional]
**config** | [**\Kubernetes\Client\Model\V1NodeConfigStatus**](V1NodeConfigStatus.md) |  | [optional]
**daemon_endpoints** | [**\Kubernetes\Client\Model\V1NodeDaemonEndpoints**](V1NodeDaemonEndpoints.md) |  | [optional]
**declared_features** | **string[]** | DeclaredFeatures represents the features related to feature gates that are declared by the node. | [optional]
**features** | [**\Kubernetes\Client\Model\V1NodeFeatures**](V1NodeFeatures.md) |  | [optional]
**images** | [**\Kubernetes\Client\Model\V1ContainerImage[]**](V1ContainerImage.md) | List of container images on this node | [optional]
**node_info** | [**\Kubernetes\Client\Model\V1NodeSystemInfo**](V1NodeSystemInfo.md) |  | [optional]
**phase** | **string** | NodePhase is the recently observed lifecycle phase of the node. More info: https://kubernetes.io/docs/concepts/nodes/node/#phase The field is never populated, and now is deprecated. | [optional]
**runtime_handlers** | [**\Kubernetes\Client\Model\V1NodeRuntimeHandler[]**](V1NodeRuntimeHandler.md) | The available runtime handlers. | [optional]
**volumes_attached** | [**\Kubernetes\Client\Model\V1AttachedVolume[]**](V1AttachedVolume.md) | List of volumes that are attached to the node. | [optional]
**volumes_in_use** | **string[]** | List of attachable volumes in use (mounted) by the node. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
