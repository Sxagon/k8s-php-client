# V1alpha1ServerStorageVersion

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_server_id** | **string** | apiServerID is the ID of the reporting API server. |
**decodable_versions** | **string[]** | decodableVersions are the encoding versions the API server can handle to decode. The API server can decode objects encoded in these versions. The encodingVersion must be included in the decodableVersions. |
**encoding_version** | **string** | encodingVersion the API server encodes the object to when persisting it in the backend (e.g., etcd). |
**served_versions** | **string[]** | servedVersions lists all versions the API server can serve. DecodableVersions must include all ServedVersions. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
