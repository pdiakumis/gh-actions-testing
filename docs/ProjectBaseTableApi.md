# ProjectBaseTableApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBaseTables**](ProjectBaseTableApi.md#GetBaseTables) | **GET** /api/projects/{projectId}/base/tables | Retrieve a liste of base tables.
[**LoadData**](ProjectBaseTableApi.md#LoadData) | **POST** /api/projects/{projectId}/base/tables/{tableId}:loadData | Load data in a base table.


# **GetBaseTables**
> ProjectBaseTableList GetBaseTables(project.id)

Retrieve a liste of base tables.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 

#Retrieve a liste of base tables.
api.instance <- ProjectBaseTableApi$new()
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

[**ProjectBaseTableList**](ProjectBaseTableList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of base tables is successfully retrieved |  -  |
| **0** | A problem occurred. |  -  |

# **LoadData**
> BaseJob LoadData(project.id, table.id, load.data.in.base.request=var.load.data.in.base.request)

Load data in a base table.

Load data in the specified table

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.table.id <- 'table.id_example' # character | 
var.load.data.in.base.request <- LoadDataInBaseRequest$new("dataId_example", "allowJaggedRows_example", "allowQuotedNewlines_example", "delimiter_example", "UTF8", "forceLoad_example", 123, "ignoreUnknownValues_example", "includeReferences_example", "includeDataReference_example", "includeSampleReference_example", "includePipelineReference_example", "includePipelineExecutionReference_example", "includeTenantReference_example", "nullMarker_example", 123, "quote_example", "WRITEIFEMPTY") # LoadDataInBaseRequest | Load data request

#Load data in a base table.
api.instance <- ProjectBaseTableApi$new()
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
 **table.id** | **character**|  | 
 **load.data.in.base.request** | [**LoadDataInBaseRequest**](LoadDataInBaseRequest.md)| Load data request | [optional] 

### Return type

[**BaseJob**](BaseJob.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Base job to load data is created. |  -  |
| **0** | A problem occurred. |  -  |

