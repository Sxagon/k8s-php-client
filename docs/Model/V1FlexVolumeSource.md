# V1FlexVolumeSource

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**driver** | **string** | driver is the name of the driver to use for this volume. |
**fs_type** | **string** | fsType is the filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. \&quot;ext4\&quot;, \&quot;xfs\&quot;, \&quot;ntfs\&quot;. The default filesystem depends on FlexVolume script. | [optional]
**options** | **array<string,string>** | options is Optional: this field holds extra command options if any. | [optional]
**read_only** | **bool** | readOnly is Optional: defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts. | [optional]
**secret_ref** | [**\Kubernetes\Client\Model\V1LocalObjectReference**](V1LocalObjectReference.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
