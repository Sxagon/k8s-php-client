# V1DeviceAllocationResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**config** | [**\Kubernetes\Client\Model\V1DeviceAllocationConfiguration[]**](V1DeviceAllocationConfiguration.md) | This field is a combination of all the claim and class configuration parameters. Drivers can distinguish between those based on a flag.  This includes configuration parameters for drivers which have no allocated devices in the result because it is up to the drivers which configuration parameters they support. They can silently ignore unknown configuration parameters. | [optional]
**results** | [**\Kubernetes\Client\Model\V1DeviceRequestAllocationResult[]**](V1DeviceRequestAllocationResult.md) | Results lists all allocated devices. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
