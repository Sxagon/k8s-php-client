# Kubernetes\Client\ApisApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAPIVersions()**](ApisApi.md#getAPIVersions) | **GET** /apis/ |  |


## `getAPIVersions()`

```php
getAPIVersions(): \Kubernetes\Client\Model\V1APIGroupList
```



get available API versions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\ApisApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAPIVersions();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApisApi->getAPIVersions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Kubernetes\Client\Model\V1APIGroupList**](../Model/V1APIGroupList.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`, `application/cbor`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
