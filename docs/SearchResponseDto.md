# SearchResponseDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to null]
**area** | **string** |  | [optional] [default to null]
**query** | **string** |  | [optional] [default to null]
**correctedQuery** | **string** |  | [optional] [default to null]
**biasingProfile** | **string** |  | [optional] [default to null]
**biasingProfileAppliedId** | **integer** |  | [optional] [default to null]
**filter** | **string** |  | [default to null]
**originalRequest** | [**SearchRequestDto**](SearchRequestDto.md) |  | [default to null]
**records** | [**array[RecordDto]**](RecordDto.md) |  | [optional] [default to null]
**totalRecordCount** | **integer** |  | [optional] [default to null]
**metadata** | [**SearchMetadataDto**](SearchMetadataDto.md) |  | [default to null]
**pageInfo** | [**PageInfoDto**](PageInfoDto.md) |  | [default to null]
**availableNavigation** | [**array[NavigationDto]**](NavigationDto.md) |  | [default to null]
**selectedNavigation** | [**array[NavigationDto]**](NavigationDto.md) |  | [default to null]
**redirect** | **string** |  | [optional] [default to null]
**experiments** | [**array[Experiment]**](Experiment.md) |  | [default to null]
**template** | [**TemplateDto**](TemplateDto.md) |  | [default to null]
**empty** | **boolean** |  | [optional] [default to null]
**siteParams** | [**array[Metadata]**](Metadata.md) |  | [default to null]
**debug** | [**DebugDto**](DebugDto.md) |  | [default to null]
**warnings** | **array[string]** |  | [optional] [default to null]
**includeExpandedResults** | **boolean** |  | [optional] [default to null]
**facetLimit** | **integer** |  | [optional] [default to null]
**redirectMetadata** | [**array[Metadata]**](Metadata.md) |  | [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


