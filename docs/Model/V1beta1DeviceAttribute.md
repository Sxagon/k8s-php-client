# V1beta1DeviceAttribute

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bool** | **bool** | BoolValue is a true/false value. | [optional]
**bools** | **bool[]** | BoolValues is a non-empty list of true/false values. | [optional]
**int** | **int** | IntValue is a number. | [optional]
**ints** | **int[]** | IntValues is a non-empty list of numbers.  This is an alpha field and requires enabling the DRAListTypeAttributes feature gate. | [optional]
**string** | **string** | StringValue is a string. Must not be longer than 64 characters. | [optional]
**strings** | **string[]** | StringValues is a non-empty list of strings. Each string must not be longer than 64 characters.  This is an alpha field and requires enabling the DRAListTypeAttributes feature gate. | [optional]
**version** | **string** | VersionValue is a semantic version according to semver.org spec 2.0.0. Must not be longer than 64 characters. | [optional]
**versions** | **string[]** | VersionValues is a non-empty list of semantic versions according to semver.org spec 2.0.0. Each version string must not be longer than 64 characters.  This is an alpha field and requires enabling the DRAListTypeAttributes feature gate. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
