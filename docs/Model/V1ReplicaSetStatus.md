# V1ReplicaSetStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**available_replicas** | **int** | The number of available replicas (ready for at least minReadySeconds) for this replica set. | [optional]
**conditions** | [**\Kubernetes\Client\Model\V1ReplicaSetCondition[]**](V1ReplicaSetCondition.md) | Represents the latest available observations of a replica set&#39;s current state. | [optional]
**fully_labeled_replicas** | **int** | The number of pods that have labels matching the labels of the pod template of the replicaset. | [optional]
**observed_generation** | **int** | ObservedGeneration reflects the generation of the most recently observed ReplicaSet. | [optional]
**ready_replicas** | **int** | readyReplicas is the number of pods targeted by this ReplicaSet with a Ready Condition. | [optional]
**replicas** | **int** | Replicas is the most recently observed number of replicas. More info: https://kubernetes.io/docs/concepts/workloads/controllers/replicationcontroller/#what-is-a-replicationcontroller |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
