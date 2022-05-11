# ProjectCustomEventsApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateCustomEvent**](ProjectCustomEventsApi.md#CreateCustomEvent) | **POST** /api/projects/{projectId}/customEvents | Create a new custom event.


# **CreateCustomEvent**
> CreateCustomEvent(project.id, create.custom.event)

Create a new custom event.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.create.custom.event <- CreateCustomEvent$new("code_example", 123) # CreateCustomEvent | 

#Create a new custom event.
api.instance <- ProjectCustomEventsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project.id** | **character**|  | 
 **create.custom.event** | [**CreateCustomEvent**](CreateCustomEvent.md)|  | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | The event is successfully created. |  -  |
| **0** | A problem occurred. |  -  |

