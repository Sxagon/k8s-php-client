# V1VolumeHealthStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**health_conditions** | [**\Kubernetes\Client\Model\V1VolumeHealthCondition[]**](V1VolumeHealthCondition.md) | conditions is the set of adverse conditions reported by the CSI controller plugin. An empty list means no adverse condition. At most 16 conditions may be reported. | [optional]
**last_transition_time** | **\DateTime** | lastTransitionTime is when the current set of conditions first appeared. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
