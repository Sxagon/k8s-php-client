# Kubernetes\Client\CustomObjectsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createClusterCustomObject()**](CustomObjectsApi.md#createClusterCustomObject) | **POST** /apis/{group}/{version}/{plural} |  |
| [**createNamespacedCustomObject()**](CustomObjectsApi.md#createNamespacedCustomObject) | **POST** /apis/{group}/{version}/namespaces/{namespace}/{plural} |  |
| [**deleteClusterCustomObject()**](CustomObjectsApi.md#deleteClusterCustomObject) | **DELETE** /apis/{group}/{version}/{plural}/{name} |  |
| [**deleteCollectionClusterCustomObject()**](CustomObjectsApi.md#deleteCollectionClusterCustomObject) | **DELETE** /apis/{group}/{version}/{plural} |  |
| [**deleteCollectionNamespacedCustomObject()**](CustomObjectsApi.md#deleteCollectionNamespacedCustomObject) | **DELETE** /apis/{group}/{version}/namespaces/{namespace}/{plural} |  |
| [**deleteNamespacedCustomObject()**](CustomObjectsApi.md#deleteNamespacedCustomObject) | **DELETE** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name} |  |
| [**getAPIResources()**](CustomObjectsApi.md#getAPIResources) | **GET** /apis/{group}/{version} |  |
| [**getClusterCustomObject()**](CustomObjectsApi.md#getClusterCustomObject) | **GET** /apis/{group}/{version}/{plural}/{name} |  |
| [**getClusterCustomObjectScale()**](CustomObjectsApi.md#getClusterCustomObjectScale) | **GET** /apis/{group}/{version}/{plural}/{name}/scale |  |
| [**getClusterCustomObjectStatus()**](CustomObjectsApi.md#getClusterCustomObjectStatus) | **GET** /apis/{group}/{version}/{plural}/{name}/status |  |
| [**getNamespacedCustomObject()**](CustomObjectsApi.md#getNamespacedCustomObject) | **GET** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name} |  |
| [**getNamespacedCustomObjectScale()**](CustomObjectsApi.md#getNamespacedCustomObjectScale) | **GET** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name}/scale |  |
| [**getNamespacedCustomObjectStatus()**](CustomObjectsApi.md#getNamespacedCustomObjectStatus) | **GET** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name}/status |  |
| [**listClusterCustomObject()**](CustomObjectsApi.md#listClusterCustomObject) | **GET** /apis/{group}/{version}/{plural} |  |
| [**listCustomObjectForAllNamespaces()**](CustomObjectsApi.md#listCustomObjectForAllNamespaces) | **GET** /apis/{group}/{version}/{resource_plural} |  |
| [**listNamespacedCustomObject()**](CustomObjectsApi.md#listNamespacedCustomObject) | **GET** /apis/{group}/{version}/namespaces/{namespace}/{plural} |  |
| [**patchClusterCustomObject()**](CustomObjectsApi.md#patchClusterCustomObject) | **PATCH** /apis/{group}/{version}/{plural}/{name} |  |
| [**patchClusterCustomObjectScale()**](CustomObjectsApi.md#patchClusterCustomObjectScale) | **PATCH** /apis/{group}/{version}/{plural}/{name}/scale |  |
| [**patchClusterCustomObjectStatus()**](CustomObjectsApi.md#patchClusterCustomObjectStatus) | **PATCH** /apis/{group}/{version}/{plural}/{name}/status |  |
| [**patchNamespacedCustomObject()**](CustomObjectsApi.md#patchNamespacedCustomObject) | **PATCH** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name} |  |
| [**patchNamespacedCustomObjectScale()**](CustomObjectsApi.md#patchNamespacedCustomObjectScale) | **PATCH** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name}/scale |  |
| [**patchNamespacedCustomObjectStatus()**](CustomObjectsApi.md#patchNamespacedCustomObjectStatus) | **PATCH** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name}/status |  |
| [**replaceClusterCustomObject()**](CustomObjectsApi.md#replaceClusterCustomObject) | **PUT** /apis/{group}/{version}/{plural}/{name} |  |
| [**replaceClusterCustomObjectScale()**](CustomObjectsApi.md#replaceClusterCustomObjectScale) | **PUT** /apis/{group}/{version}/{plural}/{name}/scale |  |
| [**replaceClusterCustomObjectStatus()**](CustomObjectsApi.md#replaceClusterCustomObjectStatus) | **PUT** /apis/{group}/{version}/{plural}/{name}/status |  |
| [**replaceNamespacedCustomObject()**](CustomObjectsApi.md#replaceNamespacedCustomObject) | **PUT** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name} |  |
| [**replaceNamespacedCustomObjectScale()**](CustomObjectsApi.md#replaceNamespacedCustomObjectScale) | **PUT** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name}/scale |  |
| [**replaceNamespacedCustomObjectStatus()**](CustomObjectsApi.md#replaceNamespacedCustomObjectStatus) | **PUT** /apis/{group}/{version}/namespaces/{namespace}/{plural}/{name}/status |  |


## `createClusterCustomObject()`

```php
createClusterCustomObject($group, $version, $plural, $body, $pretty, $dry_run, $field_manager, $field_validation): object
```



Creates a cluster scoped Custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | The custom resource's group name
$version = 'version_example'; // string | The custom resource's version
$plural = 'plural_example'; // string | The custom resource's plural name. For TPRs this would be lowercase plural kind.
$body = array('key' => new \stdClass); // object | The JSON schema of the Resource to create.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch).
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)

try {
    $result = $apiInstance->createClusterCustomObject($group, $version, $plural, $body, $pretty, $dry_run, $field_manager, $field_validation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->createClusterCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| The custom resource&#39;s group name | |
| **version** | **string**| The custom resource&#39;s version | |
| **plural** | **string**| The custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **body** | **object**| The JSON schema of the Resource to create. | |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. | [optional] |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch). | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createNamespacedCustomObject()`

```php
createNamespacedCustomObject($group, $version, $namespace, $plural, $body, $pretty, $dry_run, $field_manager, $field_validation): object
```



Creates a namespace scoped Custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | The custom resource's group name
$version = 'version_example'; // string | The custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | The custom resource's plural name. For TPRs this would be lowercase plural kind.
$body = array('key' => new \stdClass); // object | The JSON schema of the Resource to create.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)

try {
    $result = $apiInstance->createNamespacedCustomObject($group, $version, $namespace, $plural, $body, $pretty, $dry_run, $field_manager, $field_validation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->createNamespacedCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| The custom resource&#39;s group name | |
| **version** | **string**| The custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| The custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **body** | **object**| The JSON schema of the Resource to create. | |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. | [optional] |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteClusterCustomObject()`

```php
deleteClusterCustomObject($group, $version, $plural, $name, $grace_period_seconds, $orphan_dependents, $propagation_policy, $dry_run, $body): object
```



Deletes the specified cluster scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom object's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$grace_period_seconds = 56; // int | The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.
$orphan_dependents = True; // bool | Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \"orphan\" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.
$propagation_policy = 'propagation_policy_example'; // string | Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$body = new \Kubernetes\Client\Model\V1DeleteOptions(); // \Kubernetes\Client\Model\V1DeleteOptions

try {
    $result = $apiInstance->deleteClusterCustomObject($group, $version, $plural, $name, $grace_period_seconds, $orphan_dependents, $propagation_policy, $dry_run, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->deleteClusterCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom object&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **grace_period_seconds** | **int**| The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately. | [optional] |
| **orphan_dependents** | **bool**| Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \&quot;orphan\&quot; finalizer will be added to/removed from the object&#39;s finalizers list. Either this field or PropagationPolicy may be set, but not both. | [optional] |
| **propagation_policy** | **string**| Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. | [optional] |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **body** | [**\Kubernetes\Client\Model\V1DeleteOptions**](../Model/V1DeleteOptions.md)|  | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCollectionClusterCustomObject()`

```php
deleteCollectionClusterCustomObject($group, $version, $plural, $pretty, $label_selector, $grace_period_seconds, $orphan_dependents, $propagation_policy, $dry_run, $body): object
```



Delete collection of cluster scoped custom objects

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | The custom resource's group name
$version = 'version_example'; // string | The custom resource's version
$plural = 'plural_example'; // string | The custom resource's plural name. For TPRs this would be lowercase plural kind.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed.
$label_selector = 'label_selector_example'; // string | A selector to restrict the list of returned objects by their labels. Defaults to everything.
$grace_period_seconds = 56; // int | The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.
$orphan_dependents = True; // bool | Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \"orphan\" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.
$propagation_policy = 'propagation_policy_example'; // string | Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$body = new \Kubernetes\Client\Model\V1DeleteOptions(); // \Kubernetes\Client\Model\V1DeleteOptions

try {
    $result = $apiInstance->deleteCollectionClusterCustomObject($group, $version, $plural, $pretty, $label_selector, $grace_period_seconds, $orphan_dependents, $propagation_policy, $dry_run, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->deleteCollectionClusterCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| The custom resource&#39;s group name | |
| **version** | **string**| The custom resource&#39;s version | |
| **plural** | **string**| The custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. | [optional] |
| **label_selector** | **string**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] |
| **grace_period_seconds** | **int**| The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately. | [optional] |
| **orphan_dependents** | **bool**| Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \&quot;orphan\&quot; finalizer will be added to/removed from the object&#39;s finalizers list. Either this field or PropagationPolicy may be set, but not both. | [optional] |
| **propagation_policy** | **string**| Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. | [optional] |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **body** | [**\Kubernetes\Client\Model\V1DeleteOptions**](../Model/V1DeleteOptions.md)|  | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCollectionNamespacedCustomObject()`

```php
deleteCollectionNamespacedCustomObject($group, $version, $namespace, $plural, $pretty, $label_selector, $grace_period_seconds, $orphan_dependents, $propagation_policy, $dry_run, $field_selector, $body): object
```



Delete collection of namespace scoped custom objects

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | The custom resource's group name
$version = 'version_example'; // string | The custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | The custom resource's plural name. For TPRs this would be lowercase plural kind.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed.
$label_selector = 'label_selector_example'; // string | A selector to restrict the list of returned objects by their labels. Defaults to everything.
$grace_period_seconds = 56; // int | The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.
$orphan_dependents = True; // bool | Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \"orphan\" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.
$propagation_policy = 'propagation_policy_example'; // string | Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_selector = 'field_selector_example'; // string | A selector to restrict the list of returned objects by their fields. Defaults to everything.
$body = new \Kubernetes\Client\Model\V1DeleteOptions(); // \Kubernetes\Client\Model\V1DeleteOptions

try {
    $result = $apiInstance->deleteCollectionNamespacedCustomObject($group, $version, $namespace, $plural, $pretty, $label_selector, $grace_period_seconds, $orphan_dependents, $propagation_policy, $dry_run, $field_selector, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->deleteCollectionNamespacedCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| The custom resource&#39;s group name | |
| **version** | **string**| The custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| The custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. | [optional] |
| **label_selector** | **string**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] |
| **grace_period_seconds** | **int**| The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately. | [optional] |
| **orphan_dependents** | **bool**| Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \&quot;orphan\&quot; finalizer will be added to/removed from the object&#39;s finalizers list. Either this field or PropagationPolicy may be set, but not both. | [optional] |
| **propagation_policy** | **string**| Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. | [optional] |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_selector** | **string**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] |
| **body** | [**\Kubernetes\Client\Model\V1DeleteOptions**](../Model/V1DeleteOptions.md)|  | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteNamespacedCustomObject()`

```php
deleteNamespacedCustomObject($group, $version, $namespace, $plural, $name, $grace_period_seconds, $orphan_dependents, $propagation_policy, $dry_run, $body): object
```



Deletes the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$grace_period_seconds = 56; // int | The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.
$orphan_dependents = True; // bool | Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \"orphan\" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.
$propagation_policy = 'propagation_policy_example'; // string | Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$body = new \Kubernetes\Client\Model\V1DeleteOptions(); // \Kubernetes\Client\Model\V1DeleteOptions

try {
    $result = $apiInstance->deleteNamespacedCustomObject($group, $version, $namespace, $plural, $name, $grace_period_seconds, $orphan_dependents, $propagation_policy, $dry_run, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->deleteNamespacedCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **grace_period_seconds** | **int**| The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately. | [optional] |
| **orphan_dependents** | **bool**| Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the \&quot;orphan\&quot; finalizer will be added to/removed from the object&#39;s finalizers list. Either this field or PropagationPolicy may be set, but not both. | [optional] |
| **propagation_policy** | **string**| Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. | [optional] |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **body** | [**\Kubernetes\Client\Model\V1DeleteOptions**](../Model/V1DeleteOptions.md)|  | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAPIResources()`

```php
getAPIResources($group, $version): \Kubernetes\Client\Model\V1APIResourceList
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


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | The custom resource's group name
$version = 'version_example'; // string | The custom resource's version

try {
    $result = $apiInstance->getAPIResources($group, $version);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->getAPIResources: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| The custom resource&#39;s group name | |
| **version** | **string**| The custom resource&#39;s version | |

### Return type

[**\Kubernetes\Client\Model\V1APIResourceList**](../Model/V1APIResourceList.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getClusterCustomObject()`

```php
getClusterCustomObject($group, $version, $plural, $name): object
```



Returns a cluster scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom object's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name

try {
    $result = $apiInstance->getClusterCustomObject($group, $version, $plural, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->getClusterCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom object&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getClusterCustomObjectScale()`

```php
getClusterCustomObjectScale($group, $version, $plural, $name): object
```



read scale of the specified custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name

try {
    $result = $apiInstance->getClusterCustomObjectScale($group, $version, $plural, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->getClusterCustomObjectScale: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getClusterCustomObjectStatus()`

```php
getClusterCustomObjectStatus($group, $version, $plural, $name): object
```



read status of the specified cluster scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name

try {
    $result = $apiInstance->getClusterCustomObjectStatus($group, $version, $plural, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->getClusterCustomObjectStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getNamespacedCustomObject()`

```php
getNamespacedCustomObject($group, $version, $namespace, $plural, $name): object
```



Returns a namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name

try {
    $result = $apiInstance->getNamespacedCustomObject($group, $version, $namespace, $plural, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->getNamespacedCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getNamespacedCustomObjectScale()`

```php
getNamespacedCustomObjectScale($group, $version, $namespace, $plural, $name): object
```



read scale of the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name

try {
    $result = $apiInstance->getNamespacedCustomObjectScale($group, $version, $namespace, $plural, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->getNamespacedCustomObjectScale: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getNamespacedCustomObjectStatus()`

```php
getNamespacedCustomObjectStatus($group, $version, $namespace, $plural, $name): object
```



read status of the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name

try {
    $result = $apiInstance->getNamespacedCustomObjectStatus($group, $version, $namespace, $plural, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->getNamespacedCustomObjectStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listClusterCustomObject()`

```php
listClusterCustomObject($group, $version, $plural, $pretty, $allow_watch_bookmarks, $continue, $field_selector, $label_selector, $limit, $resource_version, $resource_version_match, $timeout_seconds, $watch): object
```



list or watch cluster scoped custom objects

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | The custom resource's group name
$version = 'version_example'; // string | The custom resource's version
$plural = 'plural_example'; // string | The custom resource's plural name. For TPRs this would be lowercase plural kind.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed.
$allow_watch_bookmarks = True; // bool | allowWatchBookmarks requests watch events with type \"BOOKMARK\". Servers that do not implement bookmarks may ignore this flag and bookmarks are sent at the server's discretion. Clients should not assume bookmarks are returned at any specific interval, nor may they assume the server will send any BOOKMARK event during a session. If this is not a watch, this field is ignored. If the feature gate WatchBookmarks is not enabled in apiserver, this field is ignored.
$continue = 'continue_example'; // string | The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \"next key\".  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.
$field_selector = 'field_selector_example'; // string | A selector to restrict the list of returned objects by their fields. Defaults to everything.
$label_selector = 'label_selector_example'; // string | A selector to restrict the list of returned objects by their labels. Defaults to everything.
$limit = 56; // int | limit is a maximum number of responses to return for a list call. If more items exist, the server will set the `continue` field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.
$resource_version = 'resource_version_example'; // string | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.
$resource_version_match = 'resource_version_match_example'; // string | resourceVersionMatch determines how resourceVersion is applied to list calls. It is highly recommended that resourceVersionMatch be set for list calls where resourceVersion is set See https://kubernetes.io/docs/reference/using-api/api-concepts/#resource-versions for details.  Defaults to unset
$timeout_seconds = 56; // int | Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.
$watch = True; // bool | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications.

try {
    $result = $apiInstance->listClusterCustomObject($group, $version, $plural, $pretty, $allow_watch_bookmarks, $continue, $field_selector, $label_selector, $limit, $resource_version, $resource_version_match, $timeout_seconds, $watch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->listClusterCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| The custom resource&#39;s group name | |
| **version** | **string**| The custom resource&#39;s version | |
| **plural** | **string**| The custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. | [optional] |
| **allow_watch_bookmarks** | **bool**| allowWatchBookmarks requests watch events with type \&quot;BOOKMARK\&quot;. Servers that do not implement bookmarks may ignore this flag and bookmarks are sent at the server&#39;s discretion. Clients should not assume bookmarks are returned at any specific interval, nor may they assume the server will send any BOOKMARK event during a session. If this is not a watch, this field is ignored. If the feature gate WatchBookmarks is not enabled in apiserver, this field is ignored. | [optional] |
| **continue** | **string**| The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \&quot;next key\&quot;.  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications. | [optional] |
| **field_selector** | **string**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] |
| **label_selector** | **string**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] |
| **limit** | **int**| limit is a maximum number of responses to return for a list call. If more items exist, the server will set the &#x60;continue&#x60; field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned. | [optional] |
| **resource_version** | **string**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it&#39;s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv. | [optional] |
| **resource_version_match** | **string**| resourceVersionMatch determines how resourceVersion is applied to list calls. It is highly recommended that resourceVersionMatch be set for list calls where resourceVersion is set See https://kubernetes.io/docs/reference/using-api/api-concepts/#resource-versions for details.  Defaults to unset | [optional] |
| **timeout_seconds** | **int**| Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity. | [optional] |
| **watch** | **bool**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/json;stream=watch`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCustomObjectForAllNamespaces()`

```php
listCustomObjectForAllNamespaces($group, $version, $resource_plural, $pretty, $allow_watch_bookmarks, $continue, $field_selector, $label_selector, $limit, $resource_version, $resource_version_match, $timeout_seconds, $watch): object
```



list or watch namespace scoped custom objects

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | The custom resource's group name
$version = 'version_example'; // string | The custom resource's version
$resource_plural = 'resource_plural_example'; // string | The custom resource's plural name. For TPRs this would be lowercase plural kind.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed.
$allow_watch_bookmarks = True; // bool | allowWatchBookmarks requests watch events with type \"BOOKMARK\". Servers that do not implement bookmarks may ignore this flag and bookmarks are sent at the server's discretion. Clients should not assume bookmarks are returned at any specific interval, nor may they assume the server will send any BOOKMARK event during a session. If this is not a watch, this field is ignored. If the feature gate WatchBookmarks is not enabled in apiserver, this field is ignored.
$continue = 'continue_example'; // string | The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \"next key\".  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.
$field_selector = 'field_selector_example'; // string | A selector to restrict the list of returned objects by their fields. Defaults to everything.
$label_selector = 'label_selector_example'; // string | A selector to restrict the list of returned objects by their labels. Defaults to everything.
$limit = 56; // int | limit is a maximum number of responses to return for a list call. If more items exist, the server will set the `continue` field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.
$resource_version = 'resource_version_example'; // string | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.
$resource_version_match = 'resource_version_match_example'; // string | resourceVersionMatch determines how resourceVersion is applied to list calls. It is highly recommended that resourceVersionMatch be set for list calls where resourceVersion is set See https://kubernetes.io/docs/reference/using-api/api-concepts/#resource-versions for details.  Defaults to unset
$timeout_seconds = 56; // int | Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.
$watch = True; // bool | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications.

try {
    $result = $apiInstance->listCustomObjectForAllNamespaces($group, $version, $resource_plural, $pretty, $allow_watch_bookmarks, $continue, $field_selector, $label_selector, $limit, $resource_version, $resource_version_match, $timeout_seconds, $watch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->listCustomObjectForAllNamespaces: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| The custom resource&#39;s group name | |
| **version** | **string**| The custom resource&#39;s version | |
| **resource_plural** | **string**| The custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. | [optional] |
| **allow_watch_bookmarks** | **bool**| allowWatchBookmarks requests watch events with type \&quot;BOOKMARK\&quot;. Servers that do not implement bookmarks may ignore this flag and bookmarks are sent at the server&#39;s discretion. Clients should not assume bookmarks are returned at any specific interval, nor may they assume the server will send any BOOKMARK event during a session. If this is not a watch, this field is ignored. If the feature gate WatchBookmarks is not enabled in apiserver, this field is ignored. | [optional] |
| **continue** | **string**| The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \&quot;next key\&quot;.  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications. | [optional] |
| **field_selector** | **string**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] |
| **label_selector** | **string**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] |
| **limit** | **int**| limit is a maximum number of responses to return for a list call. If more items exist, the server will set the &#x60;continue&#x60; field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned. | [optional] |
| **resource_version** | **string**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it&#39;s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv. | [optional] |
| **resource_version_match** | **string**| resourceVersionMatch determines how resourceVersion is applied to list calls. It is highly recommended that resourceVersionMatch be set for list calls where resourceVersion is set See https://kubernetes.io/docs/reference/using-api/api-concepts/#resource-versions for details.  Defaults to unset | [optional] |
| **timeout_seconds** | **int**| Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity. | [optional] |
| **watch** | **bool**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/json;stream=watch`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listNamespacedCustomObject()`

```php
listNamespacedCustomObject($group, $version, $namespace, $plural, $pretty, $allow_watch_bookmarks, $continue, $field_selector, $label_selector, $limit, $resource_version, $resource_version_match, $timeout_seconds, $watch): object
```



list or watch namespace scoped custom objects

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | The custom resource's group name
$version = 'version_example'; // string | The custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | The custom resource's plural name. For TPRs this would be lowercase plural kind.
$pretty = 'pretty_example'; // string | If 'true', then the output is pretty printed.
$allow_watch_bookmarks = True; // bool | allowWatchBookmarks requests watch events with type \"BOOKMARK\". Servers that do not implement bookmarks may ignore this flag and bookmarks are sent at the server's discretion. Clients should not assume bookmarks are returned at any specific interval, nor may they assume the server will send any BOOKMARK event during a session. If this is not a watch, this field is ignored. If the feature gate WatchBookmarks is not enabled in apiserver, this field is ignored.
$continue = 'continue_example'; // string | The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \"next key\".  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.
$field_selector = 'field_selector_example'; // string | A selector to restrict the list of returned objects by their fields. Defaults to everything.
$label_selector = 'label_selector_example'; // string | A selector to restrict the list of returned objects by their labels. Defaults to everything.
$limit = 56; // int | limit is a maximum number of responses to return for a list call. If more items exist, the server will set the `continue` field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.
$resource_version = 'resource_version_example'; // string | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.
$resource_version_match = 'resource_version_match_example'; // string | resourceVersionMatch determines how resourceVersion is applied to list calls. It is highly recommended that resourceVersionMatch be set for list calls where resourceVersion is set See https://kubernetes.io/docs/reference/using-api/api-concepts/#resource-versions for details.  Defaults to unset
$timeout_seconds = 56; // int | Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.
$watch = True; // bool | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications.

try {
    $result = $apiInstance->listNamespacedCustomObject($group, $version, $namespace, $plural, $pretty, $allow_watch_bookmarks, $continue, $field_selector, $label_selector, $limit, $resource_version, $resource_version_match, $timeout_seconds, $watch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->listNamespacedCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| The custom resource&#39;s group name | |
| **version** | **string**| The custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| The custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **pretty** | **string**| If &#39;true&#39;, then the output is pretty printed. | [optional] |
| **allow_watch_bookmarks** | **bool**| allowWatchBookmarks requests watch events with type \&quot;BOOKMARK\&quot;. Servers that do not implement bookmarks may ignore this flag and bookmarks are sent at the server&#39;s discretion. Clients should not assume bookmarks are returned at any specific interval, nor may they assume the server will send any BOOKMARK event during a session. If this is not a watch, this field is ignored. If the feature gate WatchBookmarks is not enabled in apiserver, this field is ignored. | [optional] |
| **continue** | **string**| The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error together with a continue token. If the client needs a consistent list, it must restart their list without the continue field. Otherwise, the client may send another list request with the token received with the 410 error, the server will respond with a list starting from the next key, but from the latest snapshot, which is inconsistent from the previous list results - objects that are created, modified, or deleted after the first list request will be included in the response, as long as their keys are after the \&quot;next key\&quot;.  This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications. | [optional] |
| **field_selector** | **string**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] |
| **label_selector** | **string**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] |
| **limit** | **int**| limit is a maximum number of responses to return for a list call. If more items exist, the server will set the &#x60;continue&#x60; field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.  The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned. | [optional] |
| **resource_version** | **string**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it&#39;s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv. | [optional] |
| **resource_version_match** | **string**| resourceVersionMatch determines how resourceVersion is applied to list calls. It is highly recommended that resourceVersionMatch be set for list calls where resourceVersion is set See https://kubernetes.io/docs/reference/using-api/api-concepts/#resource-versions for details.  Defaults to unset | [optional] |
| **timeout_seconds** | **int**| Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity. | [optional] |
| **watch** | **bool**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/json;stream=watch`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchClusterCustomObject()`

```php
patchClusterCustomObject($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force): object
```



patch the specified cluster scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom object's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object | The JSON schema of the Resource to patch.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch).
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)
$force = True; // bool | Force is going to \"force\" Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests.

try {
    $result = $apiInstance->patchClusterCustomObject($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->patchClusterCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom object&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**| The JSON schema of the Resource to patch. | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch). | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |
| **force** | **bool**| Force is going to \&quot;force\&quot; Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/merge-patch+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchClusterCustomObjectScale()`

```php
patchClusterCustomObjectScale($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force): object
```



partially update scale of the specified cluster scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch).
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)
$force = True; // bool | Force is going to \"force\" Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests.

try {
    $result = $apiInstance->patchClusterCustomObjectScale($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->patchClusterCustomObjectScale: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch). | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |
| **force** | **bool**| Force is going to \&quot;force\&quot; Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/merge-patch+json`
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchClusterCustomObjectStatus()`

```php
patchClusterCustomObjectStatus($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force): object
```



partially update status of the specified cluster scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch).
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)
$force = True; // bool | Force is going to \"force\" Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests.

try {
    $result = $apiInstance->patchClusterCustomObjectStatus($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->patchClusterCustomObjectStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch). | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |
| **force** | **bool**| Force is going to \&quot;force\&quot; Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/merge-patch+json`
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchNamespacedCustomObject()`

```php
patchNamespacedCustomObject($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force): object
```



patch the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object | The JSON schema of the Resource to patch.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch).
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)
$force = True; // bool | Force is going to \"force\" Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests.

try {
    $result = $apiInstance->patchNamespacedCustomObject($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->patchNamespacedCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**| The JSON schema of the Resource to patch. | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch). | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |
| **force** | **bool**| Force is going to \&quot;force\&quot; Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/merge-patch+json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchNamespacedCustomObjectScale()`

```php
patchNamespacedCustomObjectScale($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force): object
```



partially update scale of the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch).
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)
$force = True; // bool | Force is going to \"force\" Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests.

try {
    $result = $apiInstance->patchNamespacedCustomObjectScale($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->patchNamespacedCustomObjectScale: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch). | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |
| **force** | **bool**| Force is going to \&quot;force\&quot; Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/merge-patch+json`, `application/apply-patch+yaml`
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchNamespacedCustomObjectStatus()`

```php
patchNamespacedCustomObjectStatus($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force): object
```



partially update status of the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch).
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)
$force = True; // bool | Force is going to \"force\" Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests.

try {
    $result = $apiInstance->patchNamespacedCustomObjectStatus($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation, $force);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->patchNamespacedCustomObjectStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. This field is required for apply requests (application/apply-patch) but optional for non-apply patch types (JsonPatch, MergePatch, StrategicMergePatch). | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |
| **force** | **bool**| Force is going to \&quot;force\&quot; Apply requests. It means user will re-acquire conflicting fields owned by other people. Force flag must be unset for non-apply patch requests. | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/merge-patch+json`, `application/apply-patch+yaml`
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replaceClusterCustomObject()`

```php
replaceClusterCustomObject($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation): object
```



replace the specified cluster scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom object's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object | The JSON schema of the Resource to replace.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)

try {
    $result = $apiInstance->replaceClusterCustomObject($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->replaceClusterCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom object&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**| The JSON schema of the Resource to replace. | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replaceClusterCustomObjectScale()`

```php
replaceClusterCustomObjectScale($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation): object
```



replace scale of the specified cluster scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)

try {
    $result = $apiInstance->replaceClusterCustomObjectScale($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->replaceClusterCustomObjectScale: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replaceClusterCustomObjectStatus()`

```php
replaceClusterCustomObjectStatus($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation): object
```



replace status of the cluster scoped specified custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)

try {
    $result = $apiInstance->replaceClusterCustomObjectStatus($group, $version, $plural, $name, $body, $dry_run, $field_manager, $field_validation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->replaceClusterCustomObjectStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replaceNamespacedCustomObject()`

```php
replaceNamespacedCustomObject($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation): object
```



replace the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object | The JSON schema of the Resource to replace.
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)

try {
    $result = $apiInstance->replaceNamespacedCustomObject($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->replaceNamespacedCustomObject: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**| The JSON schema of the Resource to replace. | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replaceNamespacedCustomObjectScale()`

```php
replaceNamespacedCustomObjectScale($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation): object
```



replace scale of the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)

try {
    $result = $apiInstance->replaceNamespacedCustomObjectScale($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->replaceNamespacedCustomObjectScale: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replaceNamespacedCustomObjectStatus()`

```php
replaceNamespacedCustomObjectStatus($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation): object
```



replace status of the specified namespace scoped custom object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerToken
$config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Kubernetes\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');


$apiInstance = new Kubernetes\Client\Api\CustomObjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 'group_example'; // string | the custom resource's group
$version = 'version_example'; // string | the custom resource's version
$namespace = 'namespace_example'; // string | The custom resource's namespace
$plural = 'plural_example'; // string | the custom resource's plural name. For TPRs this would be lowercase plural kind.
$name = 'name_example'; // string | the custom object's name
$body = array('key' => new \stdClass); // object
$dry_run = 'dry_run_example'; // string | When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed
$field_manager = 'field_manager_example'; // string | fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.
$field_validation = 'field_validation_example'; // string | fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional)

try {
    $result = $apiInstance->replaceNamespacedCustomObjectStatus($group, $version, $namespace, $plural, $name, $body, $dry_run, $field_manager, $field_validation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomObjectsApi->replaceNamespacedCustomObjectStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| the custom resource&#39;s group | |
| **version** | **string**| the custom resource&#39;s version | |
| **namespace** | **string**| The custom resource&#39;s namespace | |
| **plural** | **string**| the custom resource&#39;s plural name. For TPRs this would be lowercase plural kind. | |
| **name** | **string**| the custom object&#39;s name | |
| **body** | **object**|  | |
| **dry_run** | **string**| When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed | [optional] |
| **field_manager** | **string**| fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint. | [optional] |
| **field_validation** | **string**| fieldValidation instructs the server on how to handle objects in the request (POST/PUT/PATCH) containing unknown or duplicate fields. Valid values are: - Ignore: This will ignore any unknown fields that are silently dropped from the object, and will ignore all but the last duplicate field that the decoder encounters. This is the default behavior prior to v1.23. - Warn: This will send a warning via the standard warning response header for each unknown field that is dropped from the object, and for each duplicate field that is encountered. The request will still succeed if there are no other errors, and will only persist the last of any duplicate fields. This is the default in v1.23+ - Strict: This will fail the request with a BadRequest error if any unknown fields would be dropped from the object, or if any duplicate fields are present. The error returned from the server will contain all unknown and duplicate fields encountered. (optional) | [optional] |

### Return type

**object**

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/yaml`, `application/vnd.kubernetes.protobuf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
