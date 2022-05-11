# AnalysisStorageApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetAnalysisStorageOptions**](AnalysisStorageApi.md#GetAnalysisStorageOptions) | **GET** /api/analysisStorages | Retrieve the list of analysis storage options.


# **GetAnalysisStorageOptions**
> AnalysisStorageList GetAnalysisStorageOptions()

Retrieve the list of analysis storage options.

### Example
```R
library(icar)


#Retrieve the list of analysis storage options.
api.instance <- AnalysisStorageApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AnalysisStorageList**](AnalysisStorageList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of analysis storage options is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

