# V1alpha3PartitionTypeStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allocatable** | **int** | Allocatable is the number of additional devices of this partition type that could still be allocated given current shared-counter consumption. |
**attribute** | **string** | Attribute is the fully qualified name of the device attribute whose value groups this entry. It is the PartitionTypeAttribute declared by the devices&#39; own slice, or the default named in the request when their slice declares none. |
**total** | **int** | Total is the number of devices of this partition type in the pool. |
**type** | **string** | Type is the partition type value (e.g. \&quot;Full\&quot; or \&quot;Half\&quot;). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
