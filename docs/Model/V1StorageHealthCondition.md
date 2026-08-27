# V1StorageHealthCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_mode** | **string** | accessMode is the access mode affected. Nil means all access modes are affected. | [optional]
**last_transition_time** | **\DateTime** | lastTransitionTime is when this condition first appeared at its current state. | [optional]
**message** | **string** | message is a human-readable description. Maximum permitted length of a message is 1024 characters. | [optional]
**reason** | **string** | reason is a brief CamelCase machine-parseable reason. Maximum permitted length of a reason is 256 characters. |
**status** | **string** | status is the health status category. One of \&quot;StorageUnreachable\&quot;, \&quot;StorageDegraded\&quot;. |
**volume_mode** | **string** | volumeMode is the volume mode affected. Nil means both are affected. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
