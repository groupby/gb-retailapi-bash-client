# RecommendationsAPIApi

All URIs are relative to **

Method | HTTP request | Description
------------- | ------------- | -------------
[**predict**](RecommendationsAPIApi.md#predict) | **POST** /api/predict | Provide Recommendations AI functionality.
[**predictV2**](RecommendationsAPIApi.md#predictV2) | **POST** /api/recommendation | Provide Recommendations AI functionality.



## predict

Provide Recommendations AI functionality.

Perform a recommendation request against the GroupBy Retail Recommendations API.

### Example

```bash
gb-retailapi-client predict X-Groupby-Customer-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xGroupbyCustomerId** | **string** | Custom HTTP header which may contain tenant name. Used to define a client by its name. | [default to null]
 **recommendationsRequest** | [**RecommendationsRequest**](RecommendationsRequest.md) | Request that should be populated to configure a recommendations API call made by the client. |

### Return type

[**PredictResults**](PredictResults.md)

### Authorization

[GroupByIncEmployee](../README.md#GroupByIncEmployee), [ClientKey](../README.md#ClientKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## predictV2

Provide Recommendations AI functionality.

Perform a recommendation request against the GroupBy Retail Recommendations API.

### Example

```bash
gb-retailapi-client predictV2 X-Groupby-Customer-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xGroupbyCustomerId** | **string** | Custom HTTP header which may contain tenant name. Used to define a client by its name. | [default to null]
 **recommendationsRequest** | [**RecommendationsRequest**](RecommendationsRequest.md) | Request that should be populated to configure a recommendations API call made by the client. |

### Return type

[**PredictResults**](PredictResults.md)

### Authorization

[GroupByIncEmployee](../README.md#GroupByIncEmployee), [ClientKey](../README.md#ClientKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

