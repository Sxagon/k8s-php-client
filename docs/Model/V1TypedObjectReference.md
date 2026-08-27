# V1TypedObjectReference

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_group** | **string** | APIGroup is the group for the resource being referenced. If APIGroup is not specified, the specified Kind must be in the core API group. For any other third-party types, APIGroup is required. | [optional]
**kind** | **string** | Kind is the type of resource being referenced |
**name** | **string** | Name is the name of resource being referenced |
**namespace** | **string** | Namespace is the namespace of resource being referenced Note that when a namespace is specified, a gateway.networking.k8s.io/ReferenceGrant object is required in the referent namespace to allow that namespace&#39;s owner to accept the reference. See the ReferenceGrant documentation for details. (Alpha) This field requires the CrossNamespaceVolumeDataSource feature gate to be enabled. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
