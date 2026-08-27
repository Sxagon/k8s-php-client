# V1alpha1StorageVersionMigrationSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**continue_token** | **string** | The token used in the list options to get the next chunk of objects to migrate. When the .status.conditions indicates the migration is \&quot;Running\&quot;, users can use this token to check the progress of the migration. | [optional]
**resource** | [**\Kubernetes\Client\Model\V1alpha1GroupVersionResource**](V1alpha1GroupVersionResource.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
