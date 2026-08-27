# V1AzureFilePersistentVolumeSource

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**read_only** | **bool** | readOnly defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts. | [optional]
**secret_name** | **string** | secretName is the name of secret that contains Azure Storage Account Name and Key |
**secret_namespace** | **string** | secretNamespace is the namespace of the secret that contains Azure Storage Account Name and Key default is the same as the Pod | [optional]
**share_name** | **string** | shareName is the azure Share Name |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
