# V1EndpointConditions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ready** | **bool** | ready indicates that this endpoint is ready to receive traffic, according to whatever system is managing the endpoint. A nil value should be interpreted as \&quot;true\&quot;. In general, an endpoint should be marked ready if it is serving and not terminating, though this can be overridden in some cases, such as when the associated Service has set the publishNotReadyAddresses flag. | [optional]
**serving** | **bool** | serving indicates that this endpoint is able to receive traffic, according to whatever system is managing the endpoint. For endpoints backed by pods, the EndpointSlice controller will mark the endpoint as serving if the pod&#39;s Ready condition is True. A nil value should be interpreted as \&quot;true\&quot;. | [optional]
**terminating** | **bool** | terminating indicates that this endpoint is terminating. A nil value should be interpreted as \&quot;false\&quot;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
