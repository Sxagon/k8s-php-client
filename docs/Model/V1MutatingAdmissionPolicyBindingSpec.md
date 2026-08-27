# V1MutatingAdmissionPolicyBindingSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**match_resources** | [**\Kubernetes\Client\Model\V1MatchResources**](V1MatchResources.md) |  | [optional]
**param_ref** | [**\Kubernetes\Client\Model\V1ParamRef**](V1ParamRef.md) |  | [optional]
**policy_name** | **string** | policyName references a MutatingAdmissionPolicy name which the MutatingAdmissionPolicyBinding binds to. If the referenced resource does not exist, this binding is considered invalid and will be ignored Required. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
