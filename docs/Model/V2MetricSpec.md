# V2MetricSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**container_resource** | [**\Kubernetes\Client\Model\V2ContainerResourceMetricSource**](V2ContainerResourceMetricSource.md) |  | [optional]
**external** | [**\Kubernetes\Client\Model\V2ExternalMetricSource**](V2ExternalMetricSource.md) |  | [optional]
**object** | [**\Kubernetes\Client\Model\V2ObjectMetricSource**](V2ObjectMetricSource.md) |  | [optional]
**pods** | [**\Kubernetes\Client\Model\V2PodsMetricSource**](V2PodsMetricSource.md) |  | [optional]
**resource** | [**\Kubernetes\Client\Model\V2ResourceMetricSource**](V2ResourceMetricSource.md) |  | [optional]
**type** | **string** | type is the type of metric source.  It should be one of \&quot;ContainerResource\&quot;, \&quot;External\&quot;, \&quot;Object\&quot;, \&quot;Pods\&quot; or \&quot;Resource\&quot;, each mapping to a matching field in the object. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
