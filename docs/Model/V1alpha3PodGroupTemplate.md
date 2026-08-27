# V1alpha3PodGroupTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**disruption_mode** | [**\Kubernetes\Client\Model\V1alpha3DisruptionMode**](V1alpha3DisruptionMode.md) |  | [optional]
**name** | **string** | name is a unique identifier for the PodGroupTemplate within the Workload. It must be a DNS label. This field is immutable. |
**preemption_policy** | **string** | preemptionPolicy is the Policy for preempting pods/podgroups with lower priority. One of Never, PreemptLowerPriority. This field is immutable. This field is available only when the PodGroupPreemptionPolicy feature gate is enabled. | [optional]
**priority** | **int** | priority is the value of priority of pod groups created from this template. Various system components use this field to find the priority of the pod group. The higher the value, the higher the priority. This field is immutable. | [optional]
**priority_class_name** | **string** | priorityClassName indicates the priority that should be considered when scheduling a pod group created from this template. This field is immutable. | [optional]
**resource_claims** | [**\Kubernetes\Client\Model\V1alpha3PodGroupResourceClaim[]**](V1alpha3PodGroupResourceClaim.md) | resourceClaims defines which ResourceClaims may be shared among Pods in the group. Pods consume the devices allocated to a PodGroup&#39;s claim by defining a claim in its own Spec.ResourceClaims that matches the PodGroup&#39;s claim exactly. The claim must have the same name and refer to the same ResourceClaim or ResourceClaimTemplate.  This is a beta-level field and requires that the DRAWorkloadResourceClaims feature gate is enabled.  This field is immutable. | [optional]
**scheduling_constraints** | [**\Kubernetes\Client\Model\V1alpha3PodGroupSchedulingConstraints**](V1alpha3PodGroupSchedulingConstraints.md) |  | [optional]
**scheduling_policy** | [**\Kubernetes\Client\Model\V1alpha3PodGroupSchedulingPolicy**](V1alpha3PodGroupSchedulingPolicy.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
