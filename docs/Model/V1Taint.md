# V1Taint

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**effect** | **string** | Required. The effect of the taint on pods that do not tolerate the taint. Valid effects are NoSchedule, PreferNoSchedule and NoExecute. |
**key** | **string** | Required. The taint key to be applied to a node. |
**time_added** | **\DateTime** | TimeAdded represents the time at which the taint was added. | [optional]
**value** | **string** | The taint value corresponding to the taint key. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
