# V1AppArmorProfile

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**localhost_profile** | **string** | localhostProfile indicates a profile loaded on the node that should be used. The profile must be preconfigured on the node to work. Must match the loaded name of the profile. Must be set if and only if type is \&quot;Localhost\&quot;. | [optional]
**type** | **string** | type indicates which kind of AppArmor profile will be applied. Valid options are:   Localhost - a profile pre-loaded on the node.   RuntimeDefault - the container runtime&#39;s default profile.   Unconfined - no AppArmor enforcement. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
