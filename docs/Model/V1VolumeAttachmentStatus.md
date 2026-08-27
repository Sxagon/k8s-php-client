# V1VolumeAttachmentStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attach_error** | [**\Kubernetes\Client\Model\V1VolumeError**](V1VolumeError.md) |  | [optional]
**attached** | **bool** | attached indicates the volume is successfully attached. This field must only be set by the entity completing the attach operation, i.e. the external-attacher. |
**attachment_metadata** | **array<string,string>** | attachmentMetadata is populated with any information returned by the attach operation, upon successful attach, that must be passed into subsequent WaitForAttach or Mount calls. This field must only be set by the entity completing the attach operation, i.e. the external-attacher. | [optional]
**detach_error** | [**\Kubernetes\Client\Model\V1VolumeError**](V1VolumeError.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
