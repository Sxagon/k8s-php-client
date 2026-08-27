# V1beta1AllocationResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allocation_timestamp** | **\DateTime** | AllocationTimestamp stores the time when the resources were allocated. This field is not guaranteed to be set, in which case that time is unknown.  This is a beta field and requires enabling the DRADeviceBindingConditions and DRAResourceClaimDeviceStatus feature gate. | [optional]
**devices** | [**\Kubernetes\Client\Model\V1beta1DeviceAllocationResult**](V1beta1DeviceAllocationResult.md) |  | [optional]
**node_selector** | [**\Kubernetes\Client\Model\V1NodeSelector**](V1NodeSelector.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
