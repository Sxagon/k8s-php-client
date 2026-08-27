# V1NFSVolumeSource

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path** | **string** | path that is exported by the NFS server. More info: https://kubernetes.io/docs/concepts/storage/volumes#nfs |
**read_only** | **bool** | readOnly here will force the NFS export to be mounted with read-only permissions. Defaults to false. More info: https://kubernetes.io/docs/concepts/storage/volumes#nfs | [optional]
**server** | **string** | server is the hostname or IP address of the NFS server. More info: https://kubernetes.io/docs/concepts/storage/volumes#nfs |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
