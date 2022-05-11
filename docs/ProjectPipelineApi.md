# ProjectPipelineApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateCwlPipeline**](ProjectPipelineApi.md#CreateCwlPipeline) | **POST** /api/projects/{projectId}/pipelines:createCwlPipeline | Create a CWL pipeline within a project.
[**CreateNextflowPipeline**](ProjectPipelineApi.md#CreateNextflowPipeline) | **POST** /api/projects/{projectId}/pipelines:createNextflowPipeline | Create a Nextflow pipeline within a project.
[**GetProjectPipeline**](ProjectPipelineApi.md#GetProjectPipeline) | **GET** /api/projects/{projectId}/pipelines/{pipelineId} | Retrieve a project pipeline.
[**GetProjectPipelineInputParameters**](ProjectPipelineApi.md#GetProjectPipelineInputParameters) | **GET** /api/projects/{projectId}/pipelines/{pipelineId}/inputParameters | Retrieve input parameters for a project pipeline.
[**GetProjectPipelineReferenceSets**](ProjectPipelineApi.md#GetProjectPipelineReferenceSets) | **GET** /api/projects/{projectId}/pipelines/{pipelineId}/referenceSets | Retrieve the reference sets of a project pipeline.
[**GetProjectPipelines**](ProjectPipelineApi.md#GetProjectPipelines) | **GET** /api/projects/{projectId}/pipelines | Retrieve a list of project pipelines.
[**LinkPipelineToProject**](ProjectPipelineApi.md#LinkPipelineToProject) | **POST** /api/projects/{projectId}/pipelines/{pipelineId} | Link a pipeline to a project.
[**ReleasePipeline**](ProjectPipelineApi.md#ReleasePipeline) | **POST** /api/projects/{projectId}/pipelines/{pipelineId}:release | Release a pipeline.
[**UnlinkPipelineFromProject**](ProjectPipelineApi.md#UnlinkPipelineFromProject) | **DELETE** /api/projects/{projectId}/pipelines/{pipelineId} | Unlink a pipeline from a project.


# **CreateCwlPipeline**
> ProjectPipeline CreateCwlPipeline(project.id, code, description, workflow.cwl.file, parameters.xml.file, analysis.storage.id, tool.cwl.files=var.tool.cwl.files, metadata.model.file=var.metadata.model.file, links=var.links, version.comment=var.version.comment, categories=var.categories, html.documentation=var.html.documentation)

Create a CWL pipeline within a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.code <- 'code_example' # character | The code of the CWL pipeline
var.description <- 'description_example' # character | The description of the CWL pipeline
var.workflow.cwl.file <- File.new('/path/to/file') # data.frame | The CWL workflow file.
var.parameters.xml.file <- File.new('/path/to/file') # data.frame | 
var.analysis.storage.id <- 'analysis.storage.id_example' # character | The id of the storage to use for the pipeline.
var.tool.cwl.files <- list(123) # array[data.frame] | 
var.metadata.model.file <- File.new('/path/to/file') # data.frame | The metadata model json file(contents can be retrieved from the controlplane).
var.links <- Links$new(list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example"))) # Links | 
var.version.comment <- 'version.comment_example' # character | 
var.categories <- list("inner_example") # array[character] | 
var.html.documentation <- 'html.documentation_example' # character | 

#Create a CWL pipeline within a project.
api.instance <- ProjectPipelineApi$new()
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
 **code** | **character**| The code of the CWL pipeline | 
 **description** | **character**| The description of the CWL pipeline | 
 **workflow.cwl.file** | **data.frame**| The CWL workflow file. | 
 **parameters.xml.file** | **data.frame**|  | 
 **analysis.storage.id** | **character**| The id of the storage to use for the pipeline. | 
 **tool.cwl.files** | list( **data.frame** )|  | [optional] 
 **metadata.model.file** | **data.frame**| The metadata model json file(contents can be retrieved from the controlplane). | [optional] 
 **links** | [**Links**](Links.md)|  | [optional] 
 **version.comment** | **character**|  | [optional] 
 **categories** | list( **character** )|  | [optional] 
 **html.documentation** | **character**|  | [optional] 

### Return type

[**ProjectPipeline**](ProjectPipeline.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The CWL pipeline is successfully created. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateNextflowPipeline**
> ProjectPipeline CreateNextflowPipeline(project.id, code, description, main.nextflow.file, parameters.xml.file, analysis.storage.id, other.nextflow.files=var.other.nextflow.files, metadata.model.file=var.metadata.model.file, links=var.links, version.comment=var.version.comment, categories=var.categories, html.documentation=var.html.documentation)

Create a Nextflow pipeline within a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.code <- 'code_example' # character | The code of the pipeline
var.description <- 'description_example' # character | The description of the pipeline
var.main.nextflow.file <- File.new('/path/to/file') # data.frame | The main Nextflow file.
var.parameters.xml.file <- File.new('/path/to/file') # data.frame | 
var.analysis.storage.id <- 'analysis.storage.id_example' # character | The id of the storage to use for the pipeline.
var.other.nextflow.files <- list(123) # array[data.frame] | 
var.metadata.model.file <- File.new('/path/to/file') # data.frame | The metadata model json file(contents can be retrieved from the controlplane).
var.links <- Links$new(list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example"))) # Links | 
var.version.comment <- 'version.comment_example' # character | 
var.categories <- list("inner_example") # array[character] | 
var.html.documentation <- 'html.documentation_example' # character | 

#Create a Nextflow pipeline within a project.
api.instance <- ProjectPipelineApi$new()
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
 **code** | **character**| The code of the pipeline | 
 **description** | **character**| The description of the pipeline | 
 **main.nextflow.file** | **data.frame**| The main Nextflow file. | 
 **parameters.xml.file** | **data.frame**|  | 
 **analysis.storage.id** | **character**| The id of the storage to use for the pipeline. | 
 **other.nextflow.files** | list( **data.frame** )|  | [optional] 
 **metadata.model.file** | **data.frame**| The metadata model json file(contents can be retrieved from the controlplane). | [optional] 
 **links** | [**Links**](Links.md)|  | [optional] 
 **version.comment** | **character**|  | [optional] 
 **categories** | list( **character** )|  | [optional] 
 **html.documentation** | **character**|  | [optional] 

### Return type

[**ProjectPipeline**](ProjectPipeline.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The Nextflow pipeline is successfully created. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjectPipeline**
> ProjectPipeline GetProjectPipeline(project.id, pipeline.id)

Retrieve a project pipeline.

Retrieve a project pipeline. This can be a pipeline from a linked bundle.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.pipeline.id <- 'pipeline.id_example' # character | The ID of the project pipeline to retrieve

#Retrieve a project pipeline.
api.instance <- ProjectPipelineApi$new()
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
 **pipeline.id** | **character**| The ID of the project pipeline to retrieve | 

### Return type

[**ProjectPipeline**](ProjectPipeline.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project pipeline is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetProjectPipelineInputParameters**
> InputParameterList GetProjectPipelineInputParameters(project.id, pipeline.id)

Retrieve input parameters for a project pipeline.

Retrieve input parameters for a project pipeline. This can be a pipeline from a linked bundle.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.pipeline.id <- 'pipeline.id_example' # character | The ID of the project pipeline to retrieve input parameters for

#Retrieve input parameters for a project pipeline.
api.instance <- ProjectPipelineApi$new()
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
 **pipeline.id** | **character**| The ID of the project pipeline to retrieve input parameters for | 

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
| **200** | The input parameters are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjectPipelineReferenceSets**
> ReferenceSetList GetProjectPipelineReferenceSets(project.id, pipeline.id)

Retrieve the reference sets of a project pipeline.

Retrieve the reference sets of a project pipeline. This can be a pipeline from a linked bundle.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline to retrieve reference sets for

#Retrieve the reference sets of a project pipeline.
api.instance <- ProjectPipelineApi$new()
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

# **GetProjectPipelines**
> ProjectPipelineList GetProjectPipelines(project.id)

Retrieve a list of project pipelines.

Retrieve a list of project pipelines. This includes pipelines from linked bundles.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project to retrieve pipelines for

#Retrieve a list of project pipelines.
api.instance <- ProjectPipelineApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project.id** | **character**| The ID of the project to retrieve pipelines for | 

### Return type

[**ProjectPipelineList**](ProjectPipelineList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of project pipelines is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **LinkPipelineToProject**
> LinkPipelineToProject(project.id, pipeline.id)

Link a pipeline to a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline

#Link a pipeline to a project.
api.instance <- ProjectPipelineApi$new()
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
| **204** | The pipeline is successfully linked to the project. |  -  |
| **0** | A problem occurred. |  -  |

# **ReleasePipeline**
> ReleasePipeline(project.id, pipeline.id)

Release a pipeline.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline

#Release a pipeline.
api.instance <- ProjectPipelineApi$new()
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
| **204** | The pipeline is successfully released. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkPipelineFromProject**
> UnlinkPipelineFromProject(project.id, pipeline.id)

Unlink a pipeline from a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.pipeline.id <- 'pipeline.id_example' # character | The ID of the pipeline

#Unlink a pipeline from a project.
api.instance <- ProjectPipelineApi$new()
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
| **204** | The pipeline is successfully unlinked from the project. |  -  |
| **0** | A problem occurred. |  -  |

