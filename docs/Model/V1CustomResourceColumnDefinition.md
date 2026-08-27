# V1CustomResourceColumnDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **string** | description is a human readable description of this column. | [optional]
**format** | **string** | format is an optional OpenAPI type definition for this column. The &#39;name&#39; format is applied to the primary identifier column to assist in clients identifying column is the resource name. See https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md#data-types for details. | [optional]
**json_path** | **string** | jsonPath is a simple JSON path (i.e. with array notation) which is evaluated against each custom resource to produce the value for this column. |
**name** | **string** | name is a human readable name for the column. |
**priority** | **int** | priority is an integer defining the relative importance of this column compared to others. Lower numbers are considered higher priority. Columns that may be omitted in limited space scenarios should be given a priority greater than 0. | [optional]
**type** | **string** | type is an OpenAPI type definition for this column. See https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md#data-types for details. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
