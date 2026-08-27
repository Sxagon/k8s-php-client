# V1beta1WorkloadSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**composite_pod_group_templates** | [**\Kubernetes\Client\Model\V1beta1CompositePodGroupTemplate[]**](V1beta1CompositePodGroupTemplate.md) | compositePodGroupTemplates is the list of CompositePodGroup templates that make up the Workload. The maximum number of templates is 8. This field is immutable. Exactly one of CompositePodGroupTemplates and PodGroupTemplates must be set.  This field is used only when the CompositePodGroup feature gate is enabled. | [optional]
**controller_ref** | [**\Kubernetes\Client\Model\V1beta1TypedLocalObjectReference**](V1beta1TypedLocalObjectReference.md) |  | [optional]
**pod_group_templates** | [**\Kubernetes\Client\Model\V1beta1PodGroupTemplate[]**](V1beta1PodGroupTemplate.md) | podGroupTemplates is the list of templates that make up the Workload. The maximum number of templates is 8. Templates cannot be added or removed after the workload is created. Existing templates may still be updated where their individual fields allow it. Exactly one of CompositePodGroupTemplates and PodGroupTemplates must be set. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
