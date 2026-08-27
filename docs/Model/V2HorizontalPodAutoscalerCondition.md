# V2HorizontalPodAutoscalerCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**last_transition_time** | **\DateTime** | lastTransitionTime is the last time the condition transitioned from one status to another | [optional]
**message** | **string** | message is a human-readable explanation containing details about the transition | [optional]
**observed_generation** | **int** | observedGeneration represents the .metadata.generation that the condition was set based upon. For instance, if .metadata.generation is currently 12, but the .status.conditions[x].observedGeneration is 9, the condition is out of date with respect to the current state of the instance. | [optional]
**reason** | **string** | reason is the reason for the condition&#39;s last transition. | [optional]
**status** | **string** | status is the status of the condition (True, False, Unknown) |
**type** | **string** | type describes the current condition |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
