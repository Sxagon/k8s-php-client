# V1alpha3DeviceClaim

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**config** | [**\Kubernetes\Client\Model\V1alpha3DeviceClaimConfiguration[]**](V1alpha3DeviceClaimConfiguration.md) | This field holds configuration for multiple potential drivers which could satisfy requests in this claim. It is ignored while allocating the claim. | [optional]
**constraints** | [**\Kubernetes\Client\Model\V1alpha3DeviceConstraint[]**](V1alpha3DeviceConstraint.md) | These constraints must be satisfied by the set of devices that get allocated for the claim. | [optional]
**requests** | [**\Kubernetes\Client\Model\V1alpha3DeviceRequest[]**](V1alpha3DeviceRequest.md) | Requests represent individual requests for distinct devices which must all be satisfied. If empty, nothing needs to be allocated. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
