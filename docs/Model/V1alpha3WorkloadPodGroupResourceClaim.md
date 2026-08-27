# V1alpha3WorkloadPodGroupResourceClaim

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | name uniquely identifies this resource claim inside the group. This field is required. It must be a DNS_LABEL. |
**resource_claim_name** | **string** | resourceClaimName is the name of a ResourceClaim object in the same namespace. This field is optional. If it is not specified, no resource claim is used. If set, it must be a DNS subdomain. | [optional]
**resource_claim_template_name** | **string** | resourceClaimTemplateName is the name of a ResourceClaimTemplate object in the same namespace. This field is optional. If it is not specified, no resource claim template is used. If set, it must be a DNS subdomain. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
