# V1VolumeAttachmentSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attacher** | **string** | attacher indicates the name of the volume driver that MUST handle this request. This is the name returned by GetPluginName(). |
**node_name** | **string** | nodeName represents the node that the volume should be attached to. |
**source** | [**\Kubernetes\Client\Model\V1VolumeAttachmentSource**](V1VolumeAttachmentSource.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
