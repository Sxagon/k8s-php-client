# V1NodeAllocatableResourceClaimStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**containers** | **string[]** | Containers lists the names of all containers in this pod that reference the claim. | [optional]
**mapping** | [**\Kubernetes\Client\Model\V1NodeAllocatableMappedResources[]**](V1NodeAllocatableMappedResources.md) | Mapping contains allocations through devices mapped in the device spec&#39;s &#x60;nodeAllocatableResources[...].mapping&#x60; field. This is used by kubelet for pod level and container-level cgroup enforcement. | [optional]
**overhead** | [**\Kubernetes\Client\Model\V1NodeAllocatableOverheadResources[]**](V1NodeAllocatableOverheadResources.md) | Overhead contains allocations through devices mapped in the device spec&#39;s &#x60;nodeAllocatableResources[...].overhead&#x60; field. This is used by kubelet for pod level and container-level cgroup enforcement. | [optional]
**resource_claim_name** | **string** | ResourceClaimName is the resource claim referenced by the pod that resulted in this node allocatable resource allocation. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
