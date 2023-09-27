# AutocompleteApi

All URIs are relative to **

Method | HTTP request | Description
------------- | ------------- | -------------
[**autocompletesearch**](AutocompleteApi.md#autocompletesearch) | **GET** /api/request | 



## autocompletesearch



A simple request used to get completes the specified prefix with keyword suggestions.

### Example

```bash
gb-retailapi-client autocompletesearch X-Groupby-Customer-Id:value  identity=value  merchandiser=value  request=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xGroupbyCustomerId** | **string** | Header on incoming HTTP requests that is populated by the API gateway and indicates the customer ID. | [default to null]
 **identity** | [**Identity**](.md) |  | [default to null]
 **merchandiser** | [**Merchandiser**](.md) |  | [default to null]
 **request** | [**Request**](.md) | Object which is represent autocomplete request and encapsulate all passed parameters. | [optional] [default to null]

### Return type

[**SearchResults**](SearchResults.md)

### Authorization

[GroupByIncEmployee](../README.md#GroupByIncEmployee), [ClientKey](../README.md#ClientKey)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

