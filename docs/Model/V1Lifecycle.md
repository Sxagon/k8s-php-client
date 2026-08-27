# V1Lifecycle

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_start** | [**\Kubernetes\Client\Model\V1LifecycleHandler**](V1LifecycleHandler.md) |  | [optional]
**pre_stop** | [**\Kubernetes\Client\Model\V1LifecycleHandler**](V1LifecycleHandler.md) |  | [optional]
**stop_signal** | **string** | StopSignal defines which signal will be sent to a container when it is being stopped. If not specified, the default is defined by the container runtime in use. StopSignal can only be set for Pods with a non-empty .spec.os.name | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
