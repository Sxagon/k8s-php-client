# V2APIResourceDiscovery

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **string** | resource is the plural name of the resource. |
**response_kind** | [**\Kubernetes\Client\Model\V1GroupVersionKind**](V1GroupVersionKind.md) |  | [optional]
**scope** | **string** | scope indicates the scope of a resource, either Cluster or Namespaced |
**singular_resource** | **string** | singularResource is the singular name of the resource. |
**verbs** | **string[]** | verbs is a list of supported API operation types |
**short_names** | **string[]** | shortNames is a list of suggested short names of the resource. | [optional]
**categories** | **string[]** | categories is a list of the grouped resources this resource belongs to. | [optional]
**subresources** | [**\Kubernetes\Client\Model\V2APISubresourceDiscovery[]**](V2APISubresourceDiscovery.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
