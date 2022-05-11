# ProjectDataTransferApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AbortDataTransfer**](ProjectDataTransferApi.md#AbortDataTransfer) | **POST** /api/projects/{projectId}/dataTransfers/{dataTransferId}:abort | Abort a data transfer.
[**GetDataTransfer**](ProjectDataTransferApi.md#GetDataTransfer) | **GET** /api/projects/{projectId}/dataTransfers/{dataTransferId} | Retrieve a data transfer.
[**GetDataTransfers**](ProjectDataTransferApi.md#GetDataTransfers) | **GET** /api/projects/{projectId}/dataTransfers | Retrieve a list of data transfers.


# **AbortDataTransfer**
> AbortDataTransfer(project.id, data.transfer.id)

Abort a data transfer.

Endpoint for aborting a data transfer.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.transfer.id <- 'data.transfer.id_example' # character | 

#Abort a data transfer.
api.instance <- ProjectDataTransferApi$new()
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
 **data.transfer.id** | **character**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | The data transfer is successfully aborted. |  -  |
| **0** | A problem occurred. |  -  |

# **GetDataTransfer**
> DataTransfer GetDataTransfer(project.id, data.transfer.id)

Retrieve a data transfer.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.transfer.id <- 'data.transfer.id_example' # character | 

#Retrieve a data transfer.
api.instance <- ProjectDataTransferApi$new()
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
 **data.transfer.id** | **character**|  | 

### Return type

[**DataTransfer**](DataTransfer.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The data transfer is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetDataTransfers**
> DataTransfers GetDataTransfers(project.id, connector=var.connector, direction=var.direction, status=var.status, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve a list of data transfers.

Retrieve a list of data transfers for the current app (session), excluding web browser transfers.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.connector <- 'connector_example' # character | The ID of the connector to filter on.
var.direction <- 'direction_example' # character | The direction to filter on.
var.status <- 'status_example' # character | The status to filter on.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - reference - direction - connector - protocol - dataTransferred - status - statusMessage - duration 

#Retrieve a list of data transfers.
api.instance <- ProjectDataTransferApi$new()
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
 **connector** | **character**| The ID of the connector to filter on. | [optional] 
 **direction** | **character**| The direction to filter on. | [optional] 
 **status** | **character**| The status to filter on. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - reference - direction - connector - protocol - dataTransferred - status - statusMessage - duration  | [optional] 

### Return type

[**DataTransfers**](DataTransfers.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of data transfers is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

