# PipelineApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetPipeline**](PipelineApi.md#GetPipeline) | **GET** /api/pipelines/{pipelineId} | Retrieve a pipeline.
[**GetPipelineInputParameters**](PipelineApi.md#GetPipelineInputParameters) | **GET** /api/pipelines/{pipelineId}/inputParameters | Retrieve input parameters for a pipeline.
[**GetPipelineReferenceSets**](PipelineApi.md#GetPipelineReferenceSets) | **GET** /api/pipelines/{pipelineId}/referenceSets | Retrieve the reference sets of a pipeline.
[**GetPipelines**](PipelineApi.md#GetPipelines) | **GET** /api/pipelines | Retrieve a list of pipelines.


# **GetPipeline**
> Pipeline GetPipeline(pipeline.id)

Retrieve a pipeline.

### Example
```R
library(icar)

var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline to retrieve

#Retrieve a pipeline.
api.instance <- PipelineApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pipeline.id** | **character**| The ID of the pipeline to retrieve | 

### Return type

[**Pipeline**](Pipeline.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The pipeline is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetPipelineInputParameters**
> InputParameterList GetPipelineInputParameters(pipeline.id)

Retrieve input parameters for a pipeline.

### Example
```R
library(icar)

var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline to retrieve input parameters for

#Retrieve input parameters for a pipeline.
api.instance <- PipelineApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pipeline.id** | **character**| The ID of the pipeline to retrieve input parameters for | 

### Return type

[**InputParameterList**](InputParameterList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The input parameters is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetPipelineReferenceSets**
> ReferenceSetList GetPipelineReferenceSets(pipeline.id)

Retrieve the reference sets of a pipeline.

### Example
```R
library(icar)

var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline to retrieve reference sets for

#Retrieve the reference sets of a pipeline.
api.instance <- PipelineApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pipeline.id** | **character**| The ID of the pipeline to retrieve reference sets for | 

### Return type

[**ReferenceSetList**](ReferenceSetList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of reference sets is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetPipelines**
> PipelineList GetPipelines()

Retrieve a list of pipelines.

### Example
```R
library(icar)


#Retrieve a list of pipelines.
api.instance <- PipelineApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PipelineList**](PipelineList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of pipelines is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

