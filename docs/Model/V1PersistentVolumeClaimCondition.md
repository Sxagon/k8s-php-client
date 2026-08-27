# V1PersistentVolumeClaimCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**last_probe_time** | **\DateTime** | lastProbeTime is the time we probed the condition. | [optional]
**last_transition_time** | **\DateTime** | lastTransitionTime is the time the condition transitioned from one status to another. | [optional]
**message** | **string** | message is the human-readable message indicating details about last transition. | [optional]
**reason** | **string** | reason is a unique, this should be a short, machine understandable string that gives the reason for condition&#39;s last transition. If it reports \&quot;Resizing\&quot; that means the underlying persistent volume is being resized. | [optional]
**status** | **string** |  |
**type** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
