# V1beta1StorageVersionMigrationStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conditions** | [**\Kubernetes\Client\Model\V1Condition[]**](V1Condition.md) | The latest available observations of the migration&#39;s current state. | [optional]
**resource_version** | **string** | ResourceVersion to compare with the GC cache for performing the migration. This is the current resource version of given group, version and resource when kube-controller-manager first observes this StorageVersionMigration resource. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
