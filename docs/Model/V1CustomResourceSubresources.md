# V1CustomResourceSubresources

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scale** | [**\Kubernetes\Client\Model\V1CustomResourceSubresourceScale**](V1CustomResourceSubresourceScale.md) |  | [optional]
**status** | **object** | status indicates the custom resource should serve a &#x60;/status&#x60; subresource. When enabled: 1. requests to the custom resource primary endpoint ignore changes to the &#x60;status&#x60; stanza of the object. 2. requests to the custom resource &#x60;/status&#x60; subresource ignore changes to anything other than the &#x60;status&#x60; stanza of the object. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
