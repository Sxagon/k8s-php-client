# V1QuobyteVolumeSource

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**group** | **string** | group to map volume access to Default is no group | [optional]
**read_only** | **bool** | readOnly here will force the Quobyte volume to be mounted with read-only permissions. Defaults to false. | [optional]
**registry** | **string** | registry represents a single or multiple Quobyte Registry services specified as a string as host:port pair (multiple entries are separated with commas) which acts as the central registry for volumes |
**tenant** | **string** | tenant owning the given Quobyte volume in the Backend Used with dynamically provisioned Quobyte volumes, value is set by the plugin | [optional]
**user** | **string** | user to map volume access to Defaults to serivceaccount user | [optional]
**volume** | **string** | volume is a string that references an already created Quobyte volume by name. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
