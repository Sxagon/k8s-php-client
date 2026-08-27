# V1IPBlock

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cidr** | **string** | cidr is a string representing the IPBlock Valid examples are \&quot;192.168.1.0/24\&quot; or \&quot;2001:db8::/64\&quot; |
**except** | **string[]** | except is a slice of CIDRs that should not be included within an IPBlock Valid examples are \&quot;192.168.1.0/24\&quot; or \&quot;2001:db8::/64\&quot; Except values will be rejected if they are outside the cidr range | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
