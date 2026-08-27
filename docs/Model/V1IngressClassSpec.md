# V1IngressClassSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**controller** | **string** | controller refers to the name of the controller that should handle this class. This allows for different \&quot;flavors\&quot; that are controlled by the same controller. For example, you may have different parameters for the same implementing controller. This should be specified as a domain-prefixed path no more than 250 characters in length, e.g. \&quot;acme.io/ingress-controller\&quot;. This field is immutable. | [optional]
**parameters** | [**\Kubernetes\Client\Model\V1IngressClassParametersReference**](V1IngressClassParametersReference.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
