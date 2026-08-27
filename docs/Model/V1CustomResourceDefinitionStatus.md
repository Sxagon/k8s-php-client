# V1CustomResourceDefinitionStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accepted_names** | [**\Kubernetes\Client\Model\V1CustomResourceDefinitionNames**](V1CustomResourceDefinitionNames.md) |  | [optional]
**conditions** | [**\Kubernetes\Client\Model\V1CustomResourceDefinitionCondition[]**](V1CustomResourceDefinitionCondition.md) | conditions indicate state for particular aspects of a CustomResourceDefinition | [optional]
**observed_generation** | **int** | The generation observed by the CRD controller. | [optional]
**stored_versions** | **string[]** | storedVersions lists all versions of CustomResources that were ever persisted. Tracking these versions allows a migration path for stored versions in etcd. The field is mutable so a migration controller can finish a migration to another version (ensuring no old objects are left in storage), and then remove the rest of the versions from this list. Versions may not be removed from &#x60;spec.versions&#x60; while they exist in this list. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
