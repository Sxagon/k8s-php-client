# V1EndpointSubset

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**addresses** | [**\Kubernetes\Client\Model\V1EndpointAddress[]**](V1EndpointAddress.md) | IP addresses which offer the related ports that are marked as ready. These endpoints should be considered safe for load balancers and clients to utilize. | [optional]
**not_ready_addresses** | [**\Kubernetes\Client\Model\V1EndpointAddress[]**](V1EndpointAddress.md) | IP addresses which offer the related ports but are not currently marked as ready because they have not yet finished starting, have recently failed a readiness check, or have recently failed a liveness check. | [optional]
**ports** | [**\Kubernetes\Client\Model\CoreV1EndpointPort[]**](CoreV1EndpointPort.md) | Port numbers available on the related IP addresses. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
