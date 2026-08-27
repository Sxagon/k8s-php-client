# V1VolumeHealthCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **string** | message is a human-readable description. Maximum permitted length of a message is 1024 bytes. | [optional]
**reason** | **string** | reason is a brief CamelCase machine-parseable reason. Together with status it forms the unique identity of a condition entry. Maximum permitted length of a reason is 256 bytes. |
**status** | **string** | status is the machine-parseable health category. Possible values: - \&quot;Inaccessible\&quot;: the volume cannot be accessed. - \&quot;DataLoss\&quot;: data loss has been detected on the volume. - \&quot;Degraded\&quot;: the volume is functioning with reduced capability. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
