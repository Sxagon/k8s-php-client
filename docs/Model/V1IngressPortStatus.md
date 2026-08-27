# V1IngressPortStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **string** | error is to record the problem with the service port The format of the error shall comply with the following rules: - built-in error values shall be specified in this file and those shall use   CamelCase names - cloud provider specific error values must have names that comply with the   format foo.example.com/CamelCase. | [optional]
**port** | **int** | port is the port number of the ingress port. |
**protocol** | **string** | protocol is the protocol of the ingress port. The supported values are: \&quot;TCP\&quot;, \&quot;UDP\&quot;, \&quot;SCTP\&quot; |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
