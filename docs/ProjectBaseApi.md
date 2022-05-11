# ProjectBaseApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateBaseConnectionDetails**](ProjectBaseApi.md#CreateBaseConnectionDetails) | **POST** /api/projects/{projectId}/base:connectionDetails | Creates the connection details to snowflake instance.


# **CreateBaseConnectionDetails**
> BaseConnection CreateBaseConnectionDetails(project.id)

Creates the connection details to snowflake instance.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project

#Creates the connection details to snowflake instance.
api.instance <- ProjectBaseApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project.id** | **character**| The ID of the project | 

### Return type

[**BaseConnection**](BaseConnection.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The base connection details are created. |  -  |
| **0** | A problem occurred. |  -  |

