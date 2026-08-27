# V1ScaleIOPersistentVolumeSource

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fs_type** | **string** | fsType is the filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. \&quot;ext4\&quot;, \&quot;xfs\&quot;, \&quot;ntfs\&quot;. Default is \&quot;xfs\&quot; | [optional]
**gateway** | **string** | gateway is the host address of the ScaleIO API Gateway. |
**protection_domain** | **string** | protectionDomain is the name of the ScaleIO Protection Domain for the configured storage. | [optional]
**read_only** | **bool** | readOnly defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts. | [optional]
**secret_ref** | [**\Kubernetes\Client\Model\V1SecretReference**](V1SecretReference.md) |  |
**ssl_enabled** | **bool** | sslEnabled is the flag to enable/disable SSL communication with Gateway, default false | [optional]
**storage_mode** | **string** | storageMode indicates whether the storage for a volume should be ThickProvisioned or ThinProvisioned. Default is ThinProvisioned. | [optional]
**storage_pool** | **string** | storagePool is the ScaleIO Storage Pool associated with the protection domain. | [optional]
**system** | **string** | system is the name of the storage system as configured in ScaleIO. |
**volume_name** | **string** | volumeName is the name of a volume already created in the ScaleIO system that is associated with this volume source. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
