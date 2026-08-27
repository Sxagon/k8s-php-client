# V1ConfigMapKeySelector

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **string** | The key to select from the ConfigMap&#39;s Data field. Keys in the BinaryData field are not currently propagated to container env vars. |
**name** | **string** | Name of the referent. This field is effectively required, but due to backwards compatibility is allowed to be empty. Instances of this type with an empty value here are almost certainly wrong. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names | [optional]
**optional** | **bool** | Specify whether the ConfigMap or its key must be defined | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
