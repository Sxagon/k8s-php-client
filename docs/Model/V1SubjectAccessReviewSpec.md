# V1SubjectAccessReviewSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**extra** | **array<string,string[]>** | Extra corresponds to the user.Info.GetExtra() method from the authenticator.  Since that is input to the authorizer it needs a reflection here. | [optional]
**groups** | **string[]** | Groups is the groups you&#39;re testing for. | [optional]
**non_resource_attributes** | [**\Kubernetes\Client\Model\V1NonResourceAttributes**](V1NonResourceAttributes.md) |  | [optional]
**resource_attributes** | [**\Kubernetes\Client\Model\V1ResourceAttributes**](V1ResourceAttributes.md) |  | [optional]
**uid** | **string** | UID information about the requesting user. | [optional]
**user** | **string** | User is the user you&#39;re testing for. If you specify \&quot;User\&quot; but not \&quot;Groups\&quot;, then is it interpreted as \&quot;What if User were not a member of any groups | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
