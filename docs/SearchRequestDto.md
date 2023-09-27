# SearchRequestDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **string** |  | [optional] [default to null]
**area** | **string** |  | [optional] [default to Production]
**collection** | **string** |  | [optional] [default to default]
**visitorId** | **string** |  | [optional] [default to null]
**refinements** | [**array[SelectedRefinementDto]**](SelectedRefinementDto.md) |  | [default to null]
**pageSize** | **integer** |  | [optional] [default to 10]
**skip** | **integer** |  | [optional] [default to 0]
**biasingProfile** | **string** |  | [optional] [default to null]
**biasing** | [**BiasingProfileDto**](BiasingProfileDto.md) |  | [default to null]
**customUrlParams** | [**array[CustomParameterDto]**](CustomParameterDto.md) |  | [default to null]
**sorts** | [**array[SortDto]**](SortDto.md) |  | [default to null]
**includedNavigations** | **array[string]** |  | [optional] [default to null]
**excludedNavigations** | **array[string]** |  | [optional] [default to null]
**dynamicFacet** | **boolean** |  | [optional] [default to null]
**variantRollupKeys** | **array[string]** |  | [optional] [default to null]
**preFilter** | **string** |  | [optional] [default to null]
**site** | **string** |  | [optional] [default to null]
**responseMask** | **array[string]** |  | [optional] [default to null]
**pageCategories** | **array[string]** |  | [optional] [default to null]
**spellCorrectionMode** | [**SpellCorrectionMode**](SpellCorrectionMode.md) |  | [optional] [default to null]
**includeExpandedResults** | **boolean** |  | [optional] [default to null]
**pinUnexpandedResults** | **boolean** |  | [optional] [default to null]
**debug** | **boolean** |  | [optional] [default to null]
**facetLimit** | **integer** |  | [optional] [default to null]
**loginId** | **string** |  | [optional] [default to null]
**overwrites** | [**SearchRequestDtoOverwrites**](SearchRequestDtoOverwrites.md) |  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


