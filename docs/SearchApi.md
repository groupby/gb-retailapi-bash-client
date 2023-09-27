# SearchApi

All URIs are relative to **

Method | HTTP request | Description
------------- | ------------- | -------------
[**facetSearch**](SearchApi.md#facetSearch) | **POST** /api/search/facet | Provided search functionality
[**search**](SearchApi.md#search) | **POST** /api/search | Provided search functionality



## facetSearch

Provided search functionality

Perform a facet search against the GroupBy Retail Search API.

### Example

```bash
gb-retailapi-client facetSearch X-Groupby-Customer-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xGroupbyCustomerId** | **string** | Custom HTTP header which may contain tenant name. Used to define a client by its name. | [default to null]
 **facetSearchRequestDto** | [**FacetSearchRequestDto**](FacetSearchRequestDto.md) | Request that should be populated to configure a search API call, made by the client on behalf of a shopper. Contains original request and information about facet for which extra keys requested. |

### Return type

[**FacetSearchResponseDto**](FacetSearchResponseDto.md)

### Authorization

[GroupByIncEmployee](../README.md#GroupByIncEmployee), [ClientKey](../README.md#ClientKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search

Provided search functionality

Perform a search against the GroupBy Retail Search API.

### Example

```bash
gb-retailapi-client search X-Groupby-Customer-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xGroupbyCustomerId** | **string** | Custom HTTP header which may contain tenant name. Used to define a client by its name. | [default to null]
 **searchRequestDto** | [**SearchRequestDto**](SearchRequestDto.md) | Request that should be populated to configure a search API call, made by the client on behalf of a shopper. |

### Return type

[**SearchResponseDto**](SearchResponseDto.md)

### Authorization

[GroupByIncEmployee](../README.md#GroupByIncEmployee), [ClientKey](../README.md#ClientKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

