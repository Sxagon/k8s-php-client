# V1alpha3ResourceClaimSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**controller** | **string** | Controller is the name of the DRA driver that is meant to handle allocation of this claim. If empty, allocation is handled by the scheduler while scheduling a pod.  Must be a DNS subdomain and should end with a DNS domain owned by the vendor of the driver.  This is an alpha field and requires enabling the DRAControlPlaneController feature gate. | [optional]
**devices** | [**\Kubernetes\Client\Model\V1alpha3DeviceClaim**](V1alpha3DeviceClaim.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
