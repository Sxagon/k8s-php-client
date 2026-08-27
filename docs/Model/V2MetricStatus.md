# V2MetricStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**container_resource** | [**\Kubernetes\Client\Model\V2ContainerResourceMetricStatus**](V2ContainerResourceMetricStatus.md) |  | [optional]
**external** | [**\Kubernetes\Client\Model\V2ExternalMetricStatus**](V2ExternalMetricStatus.md) |  | [optional]
**object** | [**\Kubernetes\Client\Model\V2ObjectMetricStatus**](V2ObjectMetricStatus.md) |  | [optional]
**pods** | [**\Kubernetes\Client\Model\V2PodsMetricStatus**](V2PodsMetricStatus.md) |  | [optional]
**resource** | [**\Kubernetes\Client\Model\V2ResourceMetricStatus**](V2ResourceMetricStatus.md) |  | [optional]
**type** | **string** | type is the type of metric source.  It will be one of \&quot;ContainerResource\&quot;, \&quot;External\&quot;, \&quot;Object\&quot;, \&quot;Pods\&quot; or \&quot;Resource\&quot;, each corresponds to a matching field in the object. Note: \&quot;ContainerResource\&quot; type is available on when the feature-gate HPAContainerMetrics is enabled |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
