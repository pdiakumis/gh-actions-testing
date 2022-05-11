# EventCodeApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetEventCodes**](EventCodeApi.md#GetEventCodes) | **GET** /api/eventCodes | Retrieve event codes


# **GetEventCodes**
> EventCodeList GetEventCodes()

Retrieve event codes

### Example
```R
library(icar)


#Retrieve event codes
api.instance <- EventCodeApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**EventCodeList**](EventCodeList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The event codes are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

