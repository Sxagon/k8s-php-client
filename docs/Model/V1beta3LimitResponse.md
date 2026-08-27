# V1beta3LimitResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**queuing** | [**\Kubernetes\Client\Model\V1beta3QueuingConfiguration**](V1beta3QueuingConfiguration.md) |  | [optional]
**type** | **string** | &#x60;type&#x60; is \&quot;Queue\&quot; or \&quot;Reject\&quot;. \&quot;Queue\&quot; means that requests that can not be executed upon arrival are held in a queue until they can be executed or a queuing limit is reached. \&quot;Reject\&quot; means that requests that can not be executed upon arrival are rejected. Required. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
