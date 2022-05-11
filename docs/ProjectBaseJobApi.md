# ProjectBaseJobApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBaseJob**](ProjectBaseJobApi.md#GetBaseJob) | **GET** /api/projects/{projectId}/base/jobs/{baseJobId} | Retrieve a base job.
[**GetBaseJobs**](ProjectBaseJobApi.md#GetBaseJobs) | **GET** /api/projects/{projectId}/base/jobs | Retrieve a list of base jobs


# **GetBaseJob**
> BaseJob GetBaseJob(project.id, base.job.id)

Retrieve a base job.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.base.job.id <- 'base.job.id_example' # character | 

#Retrieve a base job.
api.instance <- ProjectBaseJobApi$new()
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
 **base.job.id** | **character**|  | 

### Return type

[**BaseJob**](BaseJob.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The base job is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetBaseJobs**
> BaseJobList GetBaseJobs(project.id)

Retrieve a list of base jobs

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 

#Retrieve a list of base jobs
api.instance <- ProjectBaseJobApi$new()
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

### Return type

[**BaseJobList**](BaseJobList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of base jobs is successfully retrieved |  -  |
| **0** | A problem occurred. |  -  |

