# Kubernetes\Client\AuthorizationV1Api



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createNamespacedLocalSubjectAccessReview()**](AuthorizationV1Api.md#createNamespacedLocalSubjectAccessReview) | **POST** /apis/authorization.k8s.io/v1/namespaces/{namespace}/localsubjectaccessreviews |  |
| [**createSelfSubjectAccessReview()**](AuthorizationV1Api.md#createSelfSubjectAccessReview) | **POST** /apis/authorization.k8s.io/v1/selfsubjectaccessreviews |  |
| [**createSelfSubjectRulesReview()**](AuthorizationV1Api.md#createSelfSubjectRulesReview) | **POST** /apis/authorization.k8s.io/v1/selfsubjectrulesreviews |  |
| [**createSubjectAccessReview()**](AuthorizationV1Api.md#createSubjectAccessReview) | **POST** /apis/authorization.k8s.io/v1/subjectaccessreviews |  |
| [**getAPIResources()**](AuthorizationV1Api.md#getAPIResources) | **GET** /apis/authorization.k8s.io/v1/ |  |


## `createNamespacedLocalSubjectAccessReview()`

```php
createNamespacedLocalSubjectAccessReview($namespace, $body, $dry_run, $field_manager, $field_validation, $pretty): \Kubernetes\Client\Model\V1LocalSubjectAccessReview
```



create a LocalSubjectAccessReview

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\AuthorizationV1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$namespace = 'namespace_example'; // string | object name and auth scope, such as for teams and projects
$body = new \Kubernetes\Client\Model\V1LocalSubjectAccessReview(); // \Kubernetes\Client\Model\V1LocalSubjectAccessReview
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed. Defaults to 'false' unless the user-agent indicates a browser or command-line HTTP tool (curl and wget).

try {
    $result = $apiInstance->createNamespacedLocalSubjectAccessReview($namespace, $body, $dry_run, $field_manager, $field_validation, $pretty);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizationV1Api->createNamespacedLocalSubjectAccessReview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **namespace** | **string**| object name and auth scope, such as for teams and projects | |
| **body** | [**\Kubernetes\Client\Model\V1LocalSubjectAccessReview**](../Model/V1LocalSubjectAccessReview.md)|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. | [optional] |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. Defaults to &#39;false&#39; unless the user-agent indicates a browser or command-line HTTP tool (curl and wget). | [optional] |

### Return type

[**\Kubernetes\Client\Model\V1LocalSubjectAccessReview**](../Model/V1LocalSubjectAccessReview.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`, `application/cbor`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createSelfSubjectAccessReview()`

```php
createSelfSubjectAccessReview($body, $dry_run, $field_manager, $field_validation, $pretty): \Kubernetes\Client\Model\V1SelfSubjectAccessReview
```



create a SelfSubjectAccessReview

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\AuthorizationV1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Kubernetes\Client\Model\V1SelfSubjectAccessReview(); // \Kubernetes\Client\Model\V1SelfSubjectAccessReview
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed. Defaults to 'false' unless the user-agent indicates a browser or command-line HTTP tool (curl and wget).

try {
    $result = $apiInstance->createSelfSubjectAccessReview($body, $dry_run, $field_manager, $field_validation, $pretty);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizationV1Api->createSelfSubjectAccessReview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\Kubernetes\Client\Model\V1SelfSubjectAccessReview**](../Model/V1SelfSubjectAccessReview.md)|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. | [optional] |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. Defaults to &#39;false&#39; unless the user-agent indicates a browser or command-line HTTP tool (curl and wget). | [optional] |

### Return type

[**\Kubernetes\Client\Model\V1SelfSubjectAccessReview**](../Model/V1SelfSubjectAccessReview.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`, `application/cbor`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createSelfSubjectRulesReview()`

```php
createSelfSubjectRulesReview($body, $dry_run, $field_manager, $field_validation, $pretty): \Kubernetes\Client\Model\V1SelfSubjectRulesReview
```



create a SelfSubjectRulesReview

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\AuthorizationV1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Kubernetes\Client\Model\V1SelfSubjectRulesReview(); // \Kubernetes\Client\Model\V1SelfSubjectRulesReview
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed. Defaults to 'false' unless the user-agent indicates a browser or command-line HTTP tool (curl and wget).

try {
    $result = $apiInstance->createSelfSubjectRulesReview($body, $dry_run, $field_manager, $field_validation, $pretty);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizationV1Api->createSelfSubjectRulesReview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\Kubernetes\Client\Model\V1SelfSubjectRulesReview**](../Model/V1SelfSubjectRulesReview.md)|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. | [optional] |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. Defaults to &#39;false&#39; unless the user-agent indicates a browser or command-line HTTP tool (curl and wget). | [optional] |

### Return type

[**\Kubernetes\Client\Model\V1SelfSubjectRulesReview**](../Model/V1SelfSubjectRulesReview.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`, `application/cbor`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createSubjectAccessReview()`

```php
createSubjectAccessReview($body, $dry_run, $field_manager, $field_validation, $pretty): \Kubernetes\Client\Model\V1SubjectAccessReview
```



create a SubjectAccessReview

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\AuthorizationV1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Kubernetes\Client\Model\V1SubjectAccessReview(); // \Kubernetes\Client\Model\V1SubjectAccessReview
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed. Defaults to 'false' unless the user-agent indicates a browser or command-line HTTP tool (curl and wget).

try {
    $result = $apiInstance->createSubjectAccessReview($body, $dry_run, $field_manager, $field_validation, $pretty);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizationV1Api->createSubjectAccessReview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\Kubernetes\Client\Model\V1SubjectAccessReview**](../Model/V1SubjectAccessReview.md)|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. | [optional] |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. Defaults to &#39;false&#39; unless the user-agent indicates a browser or command-line HTTP tool (curl and wget). | [optional] |

### Return type

[**\Kubernetes\Client\Model\V1SubjectAccessReview**](../Model/V1SubjectAccessReview.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`, `application/cbor`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAPIResources()`

```php
getAPIResources(): \Kubernetes\Client\Model\V1APIResourceList
```



get available resources

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\AuthorizationV1Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAPIResources();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizationV1Api->getAPIResources: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Kubernetes\Client\Model\V1APIResourceList**](../Model/V1APIResourceList.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`, `application/cbor`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
