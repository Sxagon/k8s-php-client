# V1VolumeMountStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mount_path** | **string** | MountPath corresponds to the original VolumeMount. |
**name** | **string** | Name corresponds to the name of the original VolumeMount. |
**read_only** | **bool** | ReadOnly corresponds to the original VolumeMount. | [optional]
**recursive_read_only** | **string** | RecursiveReadOnly must be set to Disabled, Enabled, or unspecified (for non-readonly mounts). An IfPossible value in the original VolumeMount must be translated to Disabled or Enabled, depending on the mount result. | [optional]
**volume_status** | [**\Kubernetes\Client\Model\V1VolumeStatus**](V1VolumeStatus.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
