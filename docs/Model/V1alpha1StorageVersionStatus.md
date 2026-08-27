# V1alpha1StorageVersionStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**common_encoding_version** | **string** | commonEncodingVersion is set to an encoding storage version if all API server instances share that same version. If they don&#39;t share one storage version, this field is left empty. API servers should finish updating its storageVersionStatus entry before serving write operations, so that this field will be in sync with the reality. | [optional]
**conditions** | [**\Kubernetes\Client\Model\V1alpha1StorageVersionCondition[]**](V1alpha1StorageVersionCondition.md) | conditions lists the latest available observations of the storageVersion&#39;s state. | [optional]
**storage_versions** | [**\Kubernetes\Client\Model\V1alpha1ServerStorageVersion[]**](V1alpha1ServerStorageVersion.md) | storageVersions lists the reported versions per API server instance. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
