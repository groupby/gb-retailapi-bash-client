# ProductApi

All URIs are relative to **

Method | HTTP request | Description
------------- | ------------- | -------------
[**getByProductIds**](ProductApi.md#getByProductIds) | **GET** /api/search/product | Provided product search functionality



## getByProductIds

Provided product search functionality

Perform a product search against the GroupBy Retail Search API.

### Example

```bash
gb-retailapi-client getByProductIds  collection=value  productId=value X-Groupby-Customer-Id:value  Specify as:  variantIds=value1 variantIds=value2 variantIds=...
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection** | **string** | Collection name | [default to null]
 **productId** | **string** | Product ID which need to be search | [default to null]
 **xGroupbyCustomerId** | **string** | Required. This parameter will extract from header X-Groupby-Customer-Id. May contain tenant name. Used to define a
                          client by its name. | [default to null]
 **variantIds** | [**array[string]**](string.md) | Not required. If the product has variant list and the request specifies the variantIds, requested variants will be the
                          first in the response. | [optional] [default to null]

### Return type

[**ProductDto**](ProductDto.md)

### Authorization

[GroupByIncEmployee](../README.md#GroupByIncEmployee), [ClientKey](../README.md#ClientKey)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

