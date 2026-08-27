# V1SuccessPolicy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rules** | [**\Kubernetes\Client\Model\V1SuccessPolicyRule[]**](V1SuccessPolicyRule.md) | rules represents the list of alternative rules for the declaring the Jobs as successful before &#x60;.status.succeeded &gt;&#x3D; .spec.completions&#x60;. Once any of the rules are met, the \&quot;SucceededCriteriaMet\&quot; condition is added, and the lingering pods are removed. The terminal state for such a Job has the \&quot;Complete\&quot; condition. Additionally, these rules are evaluated in order; Once the Job meets one of the rules, other rules are ignored. At most 20 elements are allowed. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
