# V1GRPCAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mode** | **string** | mode specifies the connection mode for the gRPC health probe. Set to \&quot;TLS\&quot; to use TLS without certificate verification. Set to \&quot;Plaintext\&quot; to use a plaintext (insecure) connection explicitly. If not specified, the probe uses a plaintext (insecure) connection. | [optional]
**port** | **int** | Port number of the gRPC service. Number must be in the range 1 to 65535. |
**service** | **string** | Service is the name of the service to place in the gRPC HealthCheckRequest (see https://github.com/grpc/grpc/blob/master/doc/health-checking.md).  If this is not specified, the default behavior is defined by gRPC. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
