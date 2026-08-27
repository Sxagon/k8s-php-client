# Kubernetes\Client\WellKnownApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getServiceAccountIssuerOpenIDConfiguration()**](WellKnownApi.md#getServiceAccountIssuerOpenIDConfiguration) | **GET** /.well-known/openid-configuration |  |


## `getServiceAccountIssuerOpenIDConfiguration()`

```php
getServiceAccountIssuerOpenIDConfiguration(): string
```



get service account issuer OpenID configuration, also known as the 'OIDC discovery doc'

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\WellKnownApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getServiceAccountIssuerOpenIDConfiguration();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WellKnownApi->getServiceAccountIssuerOpenIDConfiguration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**string**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
