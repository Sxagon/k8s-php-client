# V1NodeAllocatableOverheadResources

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name is the name of the resource (e.g., cpu, memory). |
**per_container** | **string** | PerContainer is the variable overhead quantity applied for each container referencing the claim. The container references are recorded in &#x60;nodeAllocatableResourceClaimStatuses.containers&#x60;. The total overhead quantity allocated for the claim is computed as: Quantity &#x3D; PerPod + (PerContainer * NumReferences) Kubelet accounts for this overhead in cgroups: - Pod-level cgroup (requests and limits): Kubelet adds PerPod + (PerContainer * NumReferences). - Container-level cgroup (limits only): Kubelet adds PerPod + PerContainer for each referencing container. This allows any single container to access the pod-level overhead, while the parent cgroup caps the total usage to account for PerPod exactly once. At least one of PerPod or PerContainer must be specified. Specifying neither is an invalid configuration. | [optional]
**per_pod** | **string** | PerPod is the flat overhead quantity allocated per pod. Adding to each container limit allows individual containers to utilize the overhead, while the parent pod-level cgroup limit caps the total usage at the pod boundary where the overhead is accounted for exactly once. At least one of PerPod or PerContainer must be specified. Specifying neither is an invalid configuration. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
