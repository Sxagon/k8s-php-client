# V1CustomResourceDefinitionCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**last_transition_time** | **\DateTime** | lastTransitionTime last time the condition transitioned from one status to another. | [optional]
**message** | **string** | message is a human-readable message indicating details about last transition. | [optional]
**observed_generation** | **int** | observedGeneration represents the .metadata.generation that the condition was set based upon. For instance, if .metadata.generation is currently 12, but the .status.conditions[x].observedGeneration is 9, the condition is out of date with respect to the current state of the instance. | [optional]
**reason** | **string** | reason is a unique, one-word, CamelCase reason for the condition&#39;s last transition. | [optional]
**status** | **string** | status is the status of the condition. Can be True, False, Unknown. |
**type** | **string** | type is the type of the condition. Types include Established, NamesAccepted and Terminating. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
