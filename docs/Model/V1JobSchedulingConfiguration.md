# V1JobSchedulingConfiguration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**disruption_mode** | [**\Kubernetes\Client\Model\V1alpha3WorkloadPodGroupDisruptionMode**](V1alpha3WorkloadPodGroupDisruptionMode.md) |  | [optional]
**resource_claims** | [**\Kubernetes\Client\Model\V1alpha3WorkloadPodGroupResourceClaim[]**](V1alpha3WorkloadPodGroupResourceClaim.md) | ResourceClaims defines which ResourceClaims may be shared among Pods in the Job. Pods consume the devices allocated to a PodGroup&#39;s claim by defining a claim in its own Spec.ResourceClaims that matches the PodGroup&#39;s claim exactly. The claim must have the same name and refer to the same ResourceClaim or ResourceClaimTemplate. At most 4 claims may be set, matching the limit on the resulting PodGroup. This list is immutable after creation: entries may neither be added, removed, nor modified. | [optional]
**scheduling_constraints** | [**\Kubernetes\Client\Model\V1alpha3WorkloadPodGroupSchedulingConstraints**](V1alpha3WorkloadPodGroupSchedulingConstraints.md) |  | [optional]
**scheduling_policy** | [**\Kubernetes\Client\Model\V1alpha3WorkloadPodGroupSchedulingPolicy**](V1alpha3WorkloadPodGroupSchedulingPolicy.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
