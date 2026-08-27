# V1HTTPGetAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **string** | Host name to connect to, defaults to the pod IP. You probably want to set \&quot;Host\&quot; in httpHeaders instead. | [optional]
**http_headers** | [**\Kubernetes\Client\Model\V1HTTPHeader[]**](V1HTTPHeader.md) | Custom headers to set in the request. HTTP allows repeated headers. | [optional]
**path** | **string** | Path to access on the HTTP server. | [optional]
**port** | **object** | Name or number of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME. |
**protocol** | **string** | Protocol selects the wire protocol for the probe connection. Nil defaults to HTTP/1.1. | [optional]
**scheme** | **string** | Scheme to use for connecting to the host. Defaults to HTTP. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
