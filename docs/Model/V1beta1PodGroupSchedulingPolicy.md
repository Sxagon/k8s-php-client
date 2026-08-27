# V1beta1PodGroupSchedulingPolicy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**basic** | **object** | basic specifies that the pods in this group should be scheduled using standard Kubernetes scheduling behavior. Setting this field at group creation time opts this group to basic scheduling; this field cannot be changed afterward. | [optional]
**gang** | [**\Kubernetes\Client\Model\V1beta1GangSchedulingPolicy**](V1beta1GangSchedulingPolicy.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
