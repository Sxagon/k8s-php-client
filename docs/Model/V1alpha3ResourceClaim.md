# V1alpha3ResourceClaim

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_version** | **string** | APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources | [optional]
**kind** | **string** | Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds | [optional]
**metadata** | [**\Kubernetes\Client\Model\V1ObjectMeta**](V1ObjectMeta.md) |  | [optional]
**spec** | [**\Kubernetes\Client\Model\V1alpha3ResourceClaimSpec**](V1alpha3ResourceClaimSpec.md) |  |
**status** | [**\Kubernetes\Client\Model\V1alpha3ResourceClaimStatus**](V1alpha3ResourceClaimStatus.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
