# V1alpha3PodGroupResourceClaimStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | name uniquely identifies this resource claim inside the PodGroup. This must match the name of an entry in podgroup.spec.resourceClaims, which implies that the string must be a DNS_LABEL. |
**resource_claim_name** | **string** | resourceClaimName is the name of the ResourceClaim that was generated for the PodGroup in the namespace of the PodGroup. If this is unset, then generating a ResourceClaim was not necessary. The podgroup.spec.resourceClaims entry can be ignored in this case. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
