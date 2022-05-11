# WorkgroupApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetWorkgroup**](WorkgroupApi.md#GetWorkgroup) | **GET** /api/workgroups/{workgroupId} | Retrieve a workgroup.
[**GetWorkgroups**](WorkgroupApi.md#GetWorkgroups) | **GET** /api/workgroups | Retrieve a list of workgroups.


# **GetWorkgroup**
> Workgroup GetWorkgroup(workgroup.id)

Retrieve a workgroup.

### Example
```R
library(icar)

var.workgroup.id <- 'workgroup.id_example' # character | The ID of the workgroup to retrieve

#Retrieve a workgroup.
api.instance <- WorkgroupApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workgroup.id** | **character**| The ID of the workgroup to retrieve | 

### Return type

[**Workgroup**](Workgroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The workgroup is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetWorkgroups**
> WorkgroupList GetWorkgroups()

Retrieve a list of workgroups.

### Example
```R
library(icar)


#Retrieve a list of workgroups.
api.instance <- WorkgroupApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**WorkgroupList**](WorkgroupList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of workgroups is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

