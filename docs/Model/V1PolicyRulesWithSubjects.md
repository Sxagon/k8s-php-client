# V1PolicyRulesWithSubjects

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**non_resource_rules** | [**\Kubernetes\Client\Model\V1NonResourcePolicyRule[]**](V1NonResourcePolicyRule.md) | &#x60;nonResourceRules&#x60; is a list of NonResourcePolicyRules that identify matching requests according to their verb and the target non-resource URL. | [optional]
**resource_rules** | [**\Kubernetes\Client\Model\V1ResourcePolicyRule[]**](V1ResourcePolicyRule.md) | &#x60;resourceRules&#x60; is a slice of ResourcePolicyRules that identify matching requests according to their verb and the target resource. At least one of &#x60;resourceRules&#x60; and &#x60;nonResourceRules&#x60; has to be non-empty. | [optional]
**subjects** | [**\Kubernetes\Client\Model\FlowcontrolV1Subject[]**](FlowcontrolV1Subject.md) | subjects is the list of normal user, serviceaccount, or group that this rule cares about. There must be at least one member in this slice. A slice that includes both the system:authenticated and system:unauthenticated user groups matches every request. Required. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
