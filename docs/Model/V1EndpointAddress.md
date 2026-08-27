# V1EndpointAddress

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hostname** | **string** | The Hostname of this endpoint | [optional]
**ip** | **string** | The IP of this endpoint. May not be loopback (127.0.0.0/8 or ::1), link-local (169.254.0.0/16 or fe80::/10), or link-local multicast (224.0.0.0/24 or ff02::/16). |
**node_name** | **string** | Optional: Node hosting this endpoint. This can be used to determine endpoints local to a node. | [optional]
**target_ref** | [**\Kubernetes\Client\Model\V1ObjectReference**](V1ObjectReference.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
