# EntitlementDetailApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**FindAllMatchingActivationCodesForCwl**](EntitlementDetailApi.md#FindAllMatchingActivationCodesForCwl) | **POST** /api/activationCodes:findAllMatchingForCwl | Search all matching activation code details for a Cwl pipeline.
[**FindAllMatchingActivationCodesForNextflow**](EntitlementDetailApi.md#FindAllMatchingActivationCodesForNextflow) | **POST** /api/activationCodes:findAllMatchingForNextflow | Search all matching activation code details for a Nextflow pipeline.
[**FindBestMatchingActivationCodeForCwl**](EntitlementDetailApi.md#FindBestMatchingActivationCodeForCwl) | **POST** /api/activationCodes:findBestMatchingForCwl | Search the best matching activation code detail for Cwl pipeline.
[**FindBestMatchingActivationCodesForNextflow**](EntitlementDetailApi.md#FindBestMatchingActivationCodesForNextflow) | **POST** /api/activationCodes:findBestMatchingForNextflow | Search the best matching activation code details for Nextflow pipeline.


# **FindAllMatchingActivationCodesForCwl**
> ActivationCodeDetailList FindAllMatchingActivationCodesForCwl(search.matching.activation.codes.for.cwl.analysis=var.search.matching.activation.codes.for.cwl.analysis)

Search all matching activation code details for a Cwl pipeline.

Endpoint for searching all matching activation code details for a project and an analysis from a Cwl pipeline.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.search.matching.activation.codes.for.cwl.analysis <- SearchMatchingActivationCodesForCwlAnalysis$new("projectId_example", "pipelineId_example", CwlAnalysisInput$new("STRUCTURED", list(AnalysisDataInput$new("parameterCode_example", list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example")))), "inputJson_example", list(AnalysisParameter$new("code_example", "value_example")), list(AnalysisReferenceDataParameter$new("parameterCode_example", "referenceDataId_example")), list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example")))) # SearchMatchingActivationCodesForCwlAnalysis | 

#Search all matching activation code details for a Cwl pipeline.
api.instance <- EntitlementDetailApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search.matching.activation.codes.for.cwl.analysis** | [**SearchMatchingActivationCodesForCwlAnalysis**](SearchMatchingActivationCodesForCwlAnalysis.md)|  | [optional] 

### Return type

[**ActivationCodeDetailList**](ActivationCodeDetailList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The matching activation code details are successfully searched. |  -  |
| **0** | A problem occurred. |  -  |

# **FindAllMatchingActivationCodesForNextflow**
> ActivationCodeDetailList FindAllMatchingActivationCodesForNextflow(search.matching.activation.codes.for.nextflow.analysis=var.search.matching.activation.codes.for.nextflow.analysis)

Search all matching activation code details for a Nextflow pipeline.

Endpoint for searching all matching activation code details for a project and an analysis from a Nextflow pipeline.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.search.matching.activation.codes.for.nextflow.analysis <- SearchMatchingActivationCodesForNextflowAnalysis$new("projectId_example", "pipelineId_example", NextflowAnalysisInput$new(list(AnalysisDataInput$new("parameterCode_example", list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example")))), list(AnalysisParameter$new("code_example", "value_example")), list(AnalysisReferenceDataParameter$new("parameterCode_example", "referenceDataId_example")))) # SearchMatchingActivationCodesForNextflowAnalysis | 

#Search all matching activation code details for a Nextflow pipeline.
api.instance <- EntitlementDetailApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search.matching.activation.codes.for.nextflow.analysis** | [**SearchMatchingActivationCodesForNextflowAnalysis**](SearchMatchingActivationCodesForNextflowAnalysis.md)|  | [optional] 

### Return type

[**ActivationCodeDetailList**](ActivationCodeDetailList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The matching activation code details are successfully searched. |  -  |
| **0** | A problem occurred. |  -  |

# **FindBestMatchingActivationCodeForCwl**
> ActivationCodeDetail FindBestMatchingActivationCodeForCwl(search.matching.activation.codes.for.cwl.analysis=var.search.matching.activation.codes.for.cwl.analysis)

Search the best matching activation code detail for Cwl pipeline.

Endpoint for searching the best activation code detail for a project and an analysis from a Cwl pipeline.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.search.matching.activation.codes.for.cwl.analysis <- SearchMatchingActivationCodesForCwlAnalysis$new("projectId_example", "pipelineId_example", CwlAnalysisInput$new("STRUCTURED", list(AnalysisDataInput$new("parameterCode_example", list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example")))), "inputJson_example", list(AnalysisParameter$new("code_example", "value_example")), list(AnalysisReferenceDataParameter$new("parameterCode_example", "referenceDataId_example")), list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example")))) # SearchMatchingActivationCodesForCwlAnalysis | 

#Search the best matching activation code detail for Cwl pipeline.
api.instance <- EntitlementDetailApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search.matching.activation.codes.for.cwl.analysis** | [**SearchMatchingActivationCodesForCwlAnalysis**](SearchMatchingActivationCodesForCwlAnalysis.md)|  | [optional] 

### Return type

[**ActivationCodeDetail**](ActivationCodeDetail.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The best matching activation code details are successfully searched. |  -  |
| **0** | A problem occurred. |  -  |

# **FindBestMatchingActivationCodesForNextflow**
> ActivationCodeDetail FindBestMatchingActivationCodesForNextflow(search.matching.activation.codes.for.nextflow.analysis=var.search.matching.activation.codes.for.nextflow.analysis)

Search the best matching activation code details for Nextflow pipeline.

Endpoint for searching the best activation code details for a project and an analysis for a Nextflow pipeline.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.search.matching.activation.codes.for.nextflow.analysis <- SearchMatchingActivationCodesForNextflowAnalysis$new("projectId_example", "pipelineId_example", NextflowAnalysisInput$new(list(AnalysisDataInput$new("parameterCode_example", list("dataIds_example"), list(AnalysisInputDataMount$new("dataId_example", "mountPath_example")))), list(AnalysisParameter$new("code_example", "value_example")), list(AnalysisReferenceDataParameter$new("parameterCode_example", "referenceDataId_example")))) # SearchMatchingActivationCodesForNextflowAnalysis | 

#Search the best matching activation code details for Nextflow pipeline.
api.instance <- EntitlementDetailApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search.matching.activation.codes.for.nextflow.analysis** | [**SearchMatchingActivationCodesForNextflowAnalysis**](SearchMatchingActivationCodesForNextflowAnalysis.md)|  | [optional] 

### Return type

[**ActivationCodeDetail**](ActivationCodeDetail.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The best matching activation code details are successfully searched. |  -  |
| **0** | A problem occurred. |  -  |

