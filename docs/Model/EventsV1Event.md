# EventsV1Event

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **string** | action is what action was taken/failed regarding to the regarding object. It is machine-readable. This field cannot be empty for new Events and it can have at most 128 characters. | [optional]
**api_version** | **string** | APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources | [optional]
**deprecated_count** | **int** | deprecatedCount is the deprecated field assuring backward compatibility with core.v1 Event type. | [optional]
**deprecated_first_timestamp** | **\DateTime** | deprecatedFirstTimestamp is the deprecated field assuring backward compatibility with core.v1 Event type. | [optional]
**deprecated_last_timestamp** | **\DateTime** | deprecatedLastTimestamp is the deprecated field assuring backward compatibility with core.v1 Event type. | [optional]
**deprecated_source** | [**\Kubernetes\Client\Model\V1EventSource**](V1EventSource.md) |  | [optional]
**event_time** | **\DateTime** | eventTime is the time when this Event was first observed. It is required. |
**kind** | **string** | Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds | [optional]
**metadata** | [**\Kubernetes\Client\Model\V1ObjectMeta**](V1ObjectMeta.md) |  | [optional]
**note** | **string** | note is a human-readable description of the status of this operation. Maximal length of the note is 1kB, but libraries should be prepared to handle values up to 64kB. | [optional]
**reason** | **string** | reason is why the action was taken. It is human-readable. This field cannot be empty for new Events and it can have at most 128 characters. | [optional]
**regarding** | [**\Kubernetes\Client\Model\V1ObjectReference**](V1ObjectReference.md) |  | [optional]
**related** | [**\Kubernetes\Client\Model\V1ObjectReference**](V1ObjectReference.md) |  | [optional]
**reporting_controller** | **string** | reportingController is the name of the controller that emitted this Event, e.g. &#x60;kubernetes.io/kubelet&#x60;. This field cannot be empty for new Events. | [optional]
**reporting_instance** | **string** | reportingInstance is the ID of the controller instance, e.g. &#x60;kubelet-xyzf&#x60;. This field cannot be empty for new Events and it can have at most 128 characters. | [optional]
**series** | [**\Kubernetes\Client\Model\EventsV1EventSeries**](EventsV1EventSeries.md) |  | [optional]
**type** | **string** | type is the type of this event (Normal, Warning), new types could be added in the future. It is machine-readable. This field cannot be empty for new Events. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
