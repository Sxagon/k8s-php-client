# V1alpha3CompositePodGroupTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**composite_pod_group_templates** | [**\Kubernetes\Client\Model\V1alpha3CompositePodGroupTemplate[]**](V1alpha3CompositePodGroupTemplate.md) | compositePodGroupTemplates is the list of templates for children CompositePodGroups. The maximum number of templates is 8. At least one entry in CompositePodGroupTemplates or PodGroupTemplates must be set. | [optional]
**disruption_mode** | [**\Kubernetes\Client\Model\V1alpha3CompositeDisruptionMode**](V1alpha3CompositeDisruptionMode.md) |  | [optional]
**name** | **string** | name is a unique identifier for the CompositePodGroupTemplate within the Workload. It must be a DNS label. This field is required. |
**pod_group_templates** | [**\Kubernetes\Client\Model\V1alpha3PodGroupTemplate[]**](V1alpha3PodGroupTemplate.md) | podGroupTemplates is the list of templates for children PodGroups. The maximum number of templates is 8. At least one entry in CompositePodGroupTemplates or PodGroupTemplates must be set. | [optional]
**preemption_policy** | **string** | preemptionPolicy is the Policy for preempting pods/podgroups with lower priority. One of Never, PreemptLowerPriority. This field is immutable. This field is available only when the PodGroupPreemptionPolicy feature gate is enabled. | [optional]
**priority** | **int** | priority is the value of priority of composite pod groups created from this template. Various system components use this field to find the priority of the composite pod group. When Priority Admission Controller is enabled, it prevents users from setting this field. The admission controller populates this field from PriorityClassName. The higher the value, the higher the priority. This field is immutable. | [optional]
**priority_class_name** | **string** | priorityClassName indicates the priority that should be considered when scheduling a composite pod group created from this template. If no priority class is specified, admission control can set this to the global default priority class if it exists. Otherwise, composite pod groups created from this template will have the priority set to zero. This field is immutable. | [optional]
**scheduling_constraints** | [**\Kubernetes\Client\Model\V1alpha3CompositePodGroupSchedulingConstraints**](V1alpha3CompositePodGroupSchedulingConstraints.md) |  | [optional]
**scheduling_policy** | [**\Kubernetes\Client\Model\V1alpha3CompositePodGroupSchedulingPolicy**](V1alpha3CompositePodGroupSchedulingPolicy.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
