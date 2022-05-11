# BundlePipelineApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBundlePipelines**](BundlePipelineApi.md#GetBundlePipelines) | **GET** /api/bundles/{bundleId}/pipelines | Retrieve a list of bundle pipelines.
[**LinkPipelineToBundle**](BundlePipelineApi.md#LinkPipelineToBundle) | **POST** /api/bundles/{bundleId}/pipelines/{pipelineId} | Link a pipeline to a bundle.
[**UnlinkPipelineFromBundle**](BundlePipelineApi.md#UnlinkPipelineFromBundle) | **DELETE** /api/bundles/{bundleId}/pipelines/{pipelineId} | Unlink a pipeline from a bundle.


# **GetBundlePipelines**
> BundlePipelineList GetBundlePipelines(bundle.id)

Retrieve a list of bundle pipelines.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle to retrieve pipelines for

#Retrieve a list of bundle pipelines.
api.instance <- BundlePipelineApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle to retrieve pipelines for | 

### Return type

[**BundlePipelineList**](BundlePipelineList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of bundle pipelines is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **LinkPipelineToBundle**
> LinkPipelineToBundle(bundle.id, pipeline.id)

Link a pipeline to a bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle
var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline

#Link a pipeline to a bundle.
api.instance <- BundlePipelineApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle | 
 **pipeline.id** | **character**| The ID of the pipeline | 

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
| **204** | The pipeline is successfully linked to the bundle. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkPipelineFromBundle**
> UnlinkPipelineFromBundle(bundle.id, pipeline.id)

Unlink a pipeline from a bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle
var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline

#Unlink a pipeline from a bundle.
api.instance <- BundlePipelineApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle | 
 **pipeline.id** | **character**| The ID of the pipeline | 

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
| **204** | The pipeline is successfully unlinked from the bundle. |  -  |
| **0** | A problem occurred. |  -  |

