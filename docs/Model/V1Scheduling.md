# V1Scheduling

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_selector** | **array<string,string>** | nodeSelector lists labels that must be present on nodes that support this RuntimeClass. Pods using this RuntimeClass can only be scheduled to a node matched by this selector. The RuntimeClass nodeSelector is merged with a pod&#39;s existing nodeSelector. Any conflicts will cause the pod to be rejected in admission. | [optional]
**tolerations** | [**\Kubernetes\Client\Model\V1Toleration[]**](V1Toleration.md) | tolerations are appended (excluding duplicates) to pods running with this RuntimeClass during admission, effectively unioning the set of nodes tolerated by the pod and the RuntimeClass. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
