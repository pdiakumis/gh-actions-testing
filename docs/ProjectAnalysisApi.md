# ProjectAnalysisApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AbortAnalysis**](ProjectAnalysisApi.md#AbortAnalysis) | **POST** /api/projects/{projectId}/analyses/{analysisId}:abort | Abort an analysis.
[**CreateCwlAnalysis**](ProjectAnalysisApi.md#CreateCwlAnalysis) | **POST** /api/projects/{projectId}/analysis:cwl | Create and start an analysis for a CWL pipeline.
[**CreateNextflowAnalysis**](ProjectAnalysisApi.md#CreateNextflowAnalysis) | **POST** /api/projects/{projectId}/analysis:nextflow | Create and start an analysis for a Nextflow pipeline.
[**GetAnalyses**](ProjectAnalysisApi.md#GetAnalyses) | **GET** /api/projects/{projectId}/analyses | Retrieve the list of project analyses.
[**GetAnalysis**](ProjectAnalysisApi.md#GetAnalysis) | **GET** /api/projects/{projectId}/analyses/{analysisId} | Retrieve an analysis.
[**GetAnalysisConfigurations**](ProjectAnalysisApi.md#GetAnalysisConfigurations) | **GET** /api/projects/{projectId}/analyses/{analysisId}/configurations | Retrieve the configurations of an analysis.
[**GetAnalysisInputs**](ProjectAnalysisApi.md#GetAnalysisInputs) | **GET** /api/projects/{projectId}/analyses/{analysisId}/inputs | Retrieve the inputs of an analysis.
[**GetAnalysisOutputs**](ProjectAnalysisApi.md#GetAnalysisOutputs) | **GET** /api/projects/{projectId}/analyses/{analysisId}/outputs | Retrieve the outputs of an analysis.
[**GetAnalysisSteps**](ProjectAnalysisApi.md#GetAnalysisSteps) | **GET** /api/projects/{projectId}/analyses/{analysisId}/steps | Retrieve the individual steps of an analysis.
[**HGetExecutionOutputObject**](ProjectAnalysisApi.md#HGetExecutionOutputObject) | **GET** /api/projects/{projectId}/analyses/{analysisId}/rawOutput | Retrieve the raw output of an analysis.
[**UpdateAnalysis**](ProjectAnalysisApi.md#UpdateAnalysis) | **PUT** /api/projects/{projectId}/analyses/{analysisId} | Update an analysis.


# **AbortAnalysis**
> AbortAnalysis(project.id, analysis.id)

Abort an analysis.

Endpoint for aborting an analysis. The status of the analysis is not updated immediately, only when the abortion of the analysis has actually started.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.analysis.id <- 'analysis.id_example' # character | The ID of the analysis to abort

#Abort an analysis.
api.instance <- ProjectAnalysisApi$new()
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
 **analysis.id** | **character**| The ID of the analysis to abort | 

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
| **204** | The analysis is successfully aborted. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateCwlAnalysis**
> Analysis CreateCwlAnalysis(project.id, create.cwl.analysis=var.create.cwl.analysis)

Create and start an analysis for a CWL pipeline.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.create.cwl.analysis <- CreateCwlAnalysis$new("userReference_example", "pipelineId_example", AnalysisTag$new(list("technicalTags_example"), list("userTags_example"), list("referenceTags_example")), "activationCodeDetailId_example", CwlAnalysisInput$new("STRUCTURED", list(AnalysisDataInput$new("parameterCode_example", list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example")))), "inputJson_example", list(AnalysisParameter$new("code_example", "value_example")), list(AnalysisReferenceDataParameter$new("parameterCode_example", "referenceDataId_example")), list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example"))), "analysisStorageId_example", "outputParentFolderId_example") # CreateCwlAnalysis | 

#Create and start an analysis for a CWL pipeline.
api.instance <- ProjectAnalysisApi$new()
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
 **create.cwl.analysis** | [**CreateCwlAnalysis**](CreateCwlAnalysis.md)|  | [optional] 

### Return type

[**Analysis**](Analysis.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The analysis is successfully created and scheduled. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateNextflowAnalysis**
> Analysis CreateNextflowAnalysis(project.id, create.nextflow.analysis=var.create.nextflow.analysis)

Create and start an analysis for a Nextflow pipeline.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.create.nextflow.analysis <- CreateNextflowAnalysis$new("userReference_example", "pipelineId_example", AnalysisTag$new(list("technicalTags_example"), list("userTags_example"), list("referenceTags_example")), "activationCodeDetailId_example", NextflowAnalysisInput$new(list(AnalysisDataInput$new("parameterCode_example", list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example")))), list(AnalysisParameter$new("code_example", "value_example")), list(AnalysisReferenceDataParameter$new("parameterCode_example", "referenceDataId_example"))), "analysisStorageId_example", "outputParentFolderId_example") # CreateNextflowAnalysis | 

#Create and start an analysis for a Nextflow pipeline.
api.instance <- ProjectAnalysisApi$new()
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
 **create.nextflow.analysis** | [**CreateNextflowAnalysis**](CreateNextflowAnalysis.md)|  | [optional] 

### Return type

[**Analysis**](Analysis.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The analysis is successfully created and scheduled. |  -  |
| **0** | A problem occurred. |  -  |

# **GetAnalyses**
> AnalysisPagedList GetAnalyses(project.id, reference=var.reference, userreference=var.userreference, status=var.status, usertag=var.usertag, technicaltag=var.technicaltag, referencetag=var.referencetag, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve the list of project analyses.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.reference <- 'reference_example' # character | The reference to filter on.
var.userreference <- 'userreference_example' # character | The user-reference to filter on.
var.status <- 'status_example' # character | The status to filter on.
var.usertag <- 'usertag_example' # character | The user-tags to filter on.
var.technicaltag <- 'technicaltag_example' # character | The technical-tags to filter on.
var.referencetag <- 'referencetag_example' # character | The reference-data-tags to filter on.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - reference - userReference - pipeline - status - startDate - endDate - summary 

#Retrieve the list of project analyses.
api.instance <- ProjectAnalysisApi$new()
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
 **reference** | **character**| The reference to filter on. | [optional] 
 **userreference** | **character**| The user-reference to filter on. | [optional] 
 **status** | **character**| The status to filter on. | [optional] 
 **usertag** | **character**| The user-tags to filter on. | [optional] 
 **technicaltag** | **character**| The technical-tags to filter on. | [optional] 
 **referencetag** | **character**| The reference-data-tags to filter on. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - reference - userReference - pipeline - status - startDate - endDate - summary  | [optional] 

### Return type

[**AnalysisPagedList**](AnalysisPagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of project analyses is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetAnalysis**
> Analysis GetAnalysis(project.id, analysis.id)

Retrieve an analysis.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.analysis.id <- 'analysis.id_example' # character | The ID of the analysis to retrieve

#Retrieve an analysis.
api.instance <- ProjectAnalysisApi$new()
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
 **analysis.id** | **character**| The ID of the analysis to retrieve | 

### Return type

[**Analysis**](Analysis.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The analysis is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetAnalysisConfigurations**
> ExecutionConfigurationList GetAnalysisConfigurations(project.id, analysis.id)

Retrieve the configurations of an analysis.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.analysis.id <- 'analysis.id_example' # character | The ID of the analysis to retrieve the configuration for

#Retrieve the configurations of an analysis.
api.instance <- ProjectAnalysisApi$new()
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
 **analysis.id** | **character**| The ID of the analysis to retrieve the configuration for | 

### Return type

[**ExecutionConfigurationList**](ExecutionConfigurationList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The configurations of the analysis are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetAnalysisInputs**
> AnalysisInputList GetAnalysisInputs(project.id, analysis.id)

Retrieve the inputs of an analysis.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.analysis.id <- 'analysis.id_example' # character | The ID of the analysis to retrieve the inputs for

#Retrieve the inputs of an analysis.
api.instance <- ProjectAnalysisApi$new()
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
 **analysis.id** | **character**| The ID of the analysis to retrieve the inputs for | 

### Return type

[**AnalysisInputList**](AnalysisInputList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The inputs of the analysis are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetAnalysisOutputs**
> AnalysisOutputList GetAnalysisOutputs(project.id, analysis.id)

Retrieve the outputs of an analysis.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.analysis.id <- 'analysis.id_example' # character | The ID of the analysis to retrieve the outputs for

#Retrieve the outputs of an analysis.
api.instance <- ProjectAnalysisApi$new()
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
 **analysis.id** | **character**| The ID of the analysis to retrieve the outputs for | 

### Return type

[**AnalysisOutputList**](AnalysisOutputList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The outputs of the analysis are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetAnalysisSteps**
> AnalysisStepList GetAnalysisSteps(project.id, analysis.id)

Retrieve the individual steps of an analysis.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.analysis.id <- 'analysis.id_example' # character | The ID of the analysis to retrieve the individual steps for

#Retrieve the individual steps of an analysis.
api.instance <- ProjectAnalysisApi$new()
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
 **analysis.id** | **character**| The ID of the analysis to retrieve the individual steps for | 

### Return type

[**AnalysisStepList**](AnalysisStepList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The individual steps of the analysis are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **HGetExecutionOutputObject**
> AnalysisRawOutput HGetExecutionOutputObject(project.id, analysis.id)

Retrieve the raw output of an analysis.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.analysis.id <- 'analysis.id_example' # character | The ID of the analysis for which to retrieve the raw output

#Retrieve the raw output of an analysis.
api.instance <- ProjectAnalysisApi$new()
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
 **analysis.id** | **character**| The ID of the analysis for which to retrieve the raw output | 

### Return type

[**AnalysisRawOutput**](AnalysisRawOutput.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The raw output of the analysis is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateAnalysis**
> Analysis UpdateAnalysis(project.id, analysis.id, if.match=var.if.match, analysis=var.analysis)

Update an analysis.

Attributes which can be updated:    - tags

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.analysis.id <- 'analysis.id_example' # character | 
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.analysis <- Analysis$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "reference_example", "userReference_example", Pipeline$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "description_example", "CWL", PipelineTag$new(list("technicalTags_example")), AnalysisStorage$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", "tenantName_example", "description_example"), "tenantName_example"), "REQUESTED", AnalysisTag$new(list("technicalTags_example"), list("userTags_example"), list("referenceTags_example")), "tenantName_example", "startDate_example", "endDate_example", "summary_example", AnalysisStorage$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", "tenantName_example", "description_example")) # Analysis | 

#Update an analysis.
api.instance <- ProjectAnalysisApi$new()
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
 **analysis.id** | **character**|  | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **analysis** | [**Analysis**](Analysis.md)|  | [optional] 

### Return type

[**Analysis**](Analysis.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The analysis is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

