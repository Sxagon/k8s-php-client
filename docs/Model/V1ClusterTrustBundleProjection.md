# V1ClusterTrustBundleProjection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label_selector** | [**\Kubernetes\Client\Model\V1LabelSelector**](V1LabelSelector.md) |  | [optional]
**name** | **string** | Select a single ClusterTrustBundle by object name.  Mutually-exclusive with signerName and labelSelector. | [optional]
**optional** | **bool** | If true, don&#39;t block pod startup if the referenced ClusterTrustBundle(s) aren&#39;t available.  If using name, then the named ClusterTrustBundle is allowed not to exist.  If using signerName, then the combination of signerName and labelSelector is allowed to match zero ClusterTrustBundles. | [optional]
**path** | **string** | Relative path from the volume root to write the bundle. |
**signer_name** | **string** | Select all ClusterTrustBundles that match this signer name. Mutually-exclusive with name.  The contents of all selected ClusterTrustBundles will be unified and deduplicated. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
