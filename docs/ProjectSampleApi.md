# ProjectSampleApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddMetadataModelToSample**](ProjectSampleApi.md#AddMetadataModelToSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/metadata/{metadataModelId} | Add a metadata model to a sample.
[**CompleteProjectSample**](ProjectSampleApi.md#CompleteProjectSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:complete | Completes the sample after data has been linked to it.
[**CreateSampleInProject**](ProjectSampleApi.md#CreateSampleInProject) | **POST** /api/projects/{projectId}/samples | Create a new sample in this project
[**DeepDeleteSample**](ProjectSampleApi.md#DeepDeleteSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteDeep | Delete a sample together with all of its data.
[**DeleteAndUnlinkSample**](ProjectSampleApi.md#DeleteAndUnlinkSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteUnlink | Delete a sample and unlink its data.
[**DeleteSampleWithInput**](ProjectSampleApi.md#DeleteSampleWithInput) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteWithInput | Delete a sample as well as its input data.
[**GetProjectSample**](ProjectSampleApi.md#GetProjectSample) | **GET** /api/projects/{projectId}/samples/{sampleId} | Retrieve a project sample.
[**GetProjectSamples**](ProjectSampleApi.md#GetProjectSamples) | **POST** /api/projects/{projectId}/samples:search | Retrieve project samples.
[**GetProjectsForSample**](ProjectSampleApi.md#GetProjectsForSample) | **GET** /api/projects/{projectId}/samples/{sampleId}/projects | Retrieve a list of projects for this sample.
[**GetSampleDataList**](ProjectSampleApi.md#GetSampleDataList) | **GET** /api/projects/{projectId}/samples/{sampleId}/data | Retrieve the list of sample data.
[**GetSampleHistory**](ProjectSampleApi.md#GetSampleHistory) | **GET** /api/projects/{projectId}/samples/{sampleId}/history | Retrieve sample history.
[**GetSampleMetadataField**](ProjectSampleApi.md#GetSampleMetadataField) | **GET** /api/projects/{projectId}/samples/{sampleId}/metadata/field/{fieldId} | Retrieve a metadata field.
[**GetSampleMetadataFieldCount**](ProjectSampleApi.md#GetSampleMetadataFieldCount) | **GET** /api/projects/{projectId}/samples/{sampleId}/metadata/{fieldId}/fieldCount | Retrieves the number of occurrences of a given field.
[**LinkDataToSample**](ProjectSampleApi.md#LinkDataToSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/data/{dataId} | Link data to a sample.
[**LinkSampleToProject**](ProjectSampleApi.md#LinkSampleToProject) | **POST** /api/projects/{projectId}/samples/{sampleId} | Link a sample to a project.
[**MarkSampleDeleted**](ProjectSampleApi.md#MarkSampleDeleted) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteMark | Mark a sample deleted.
[**UnlinkDataFromSample**](ProjectSampleApi.md#UnlinkDataFromSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/data/{dataId}:unlink | Unlink data from a sample.
[**UnlinkSampleFromProject**](ProjectSampleApi.md#UnlinkSampleFromProject) | **POST** /api/projects/{projectId}/samples/{sampleId}:unlink | Unlink a sample from a project.
[**UpdateProjectSample**](ProjectSampleApi.md#UpdateProjectSample) | **PUT** /api/projects/{projectId}/samples/{sampleId} | Update a project sample.
[**UpdateSampleMetadataFields**](ProjectSampleApi.md#UpdateSampleMetadataFields) | **POST** /api/projects/{projectId}/samples/{sampleId}/metadata:updateFields | Update metadata fields.


# **AddMetadataModelToSample**
> AddMetadataModelToSample(project.id, sample.id, metadata.model.id)

Add a metadata model to a sample.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample
var.metadata.model.id <- 'metadata.model.id_example' # character | The ID of the metadata model

#Add a metadata model to a sample.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 
 **metadata.model.id** | **character**| The ID of the metadata model | 

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
| **204** | The metadata model is successfully added to the sample. |  -  |
| **0** | A problem occurred. |  -  |

# **CompleteProjectSample**
> CompleteProjectSample(project.id, sample.id)

Completes the sample after data has been linked to it.

Completes the sample after data has been linked to it. The sample status will be set to 'Available' and a sample completed event will be triggered as well.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | 

#Completes the sample after data has been linked to it.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**|  | 

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
| **204** | The sample is successfully completed. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateSampleInProject**
> ProjectSample CreateSampleInProject(project.id, create.sample=var.create.sample)

Create a new sample in this project

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.create.sample <- CreateSample$new("name_example", "description_example", SampleTag$new(list("technicalTags_example"), list("userTags_example"), list("connectorTags_example"), list("runInTags_example"))) # CreateSample | 

#Create a new sample in this project
api.instance <- ProjectSampleApi$new()
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
 **create.sample** | [**CreateSample**](CreateSample.md)|  | [optional] 

### Return type

[**ProjectSample**](ProjectSample.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The sample is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **DeepDeleteSample**
> DeepDeleteSample(project.id, sample.id)

Delete a sample together with all of its data.

Endpoint deleting a sample together with all of its data.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample

#Delete a sample together with all of its data.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 

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
| **200** | The sample and all of its data are successfully deleted. |  -  |
| **0** | A problem occurred. |  -  |

# **DeleteAndUnlinkSample**
> DeleteAndUnlinkSample(project.id, sample.id)

Delete a sample and unlink its data.

Endpoint for deleting a sample while unlinking its data.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample

#Delete a sample and unlink its data.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 

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
| **200** | The sample is successfully deleted and the its data is successfully unlinked. |  -  |
| **0** | A problem occurred. |  -  |

# **DeleteSampleWithInput**
> DeleteSampleWithInput(project.id, sample.id)

Delete a sample as well as its input data.

Endpoint for deleting a sample as well as its input data.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample

#Delete a sample as well as its input data.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 

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
| **200** | The sample and its input data are successfully deleted. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjectSample**
> ProjectSample GetProjectSample(project.id, sample.id)

Retrieve a project sample.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample

#Retrieve a project sample.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 

### Return type

[**ProjectSample**](ProjectSample.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project sample is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetProjectSamples**
> ProjectSamplePagedList GetProjectSamples(project.id, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort, find.project.samples=var.find.project.samples)

Retrieve project samples.

Endpoint for retrieving project samples. This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\" The attributes for which sorting is supported: - timeCreated - timeModified - name - description - metadataValid - status
var.find.project.samples <- FindProjectSamples$new(list(FindSampleCondition$new(list("values_example"), FieldId$new("id_example"), "field_example", "EXACT")), list(FindSampleDateCondition$new(FieldId$new("id_example"), "field_example", "beforeDate_example", "afterDate_example")), list(FindSampleNumberCondition$new(FieldId$new("id_example"), "field_example", "lowerBound_example", "upperBound_example")), list(FindSampleBooleanCondition$new(Field$new("id_example", "name_example", "description_example", "TEXT", "required_example", "multivalued_example", "filledByPipeline_example", list(Field$new("id_example", "name_example", "description_example", "TEXT", "required_example", "multivalued_example", "filledByPipeline_example", list(...), list("enumerationValues_example"))), list("enumerationValues_example")), "field_example", "value_example")), "fullTextSearchString_example", "includeDeleted_example", list("userTags_example"), "EXACT", list("runInputTags_example"), "EXACT", list("connectorTags_example"), "EXACT", list("techTags_example"), "EXACT") # FindProjectSamples | 

#Retrieve project samples.
api.instance <- ProjectSampleApi$new()
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
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot; The attributes for which sorting is supported: - timeCreated - timeModified - name - description - metadataValid - status | [optional] 
 **find.project.samples** | [**FindProjectSamples**](FindProjectSamples.md)|  | [optional] 

### Return type

[**ProjectSamplePagedList**](ProjectSamplePagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project samples are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjectsForSample**
> ProjectList GetProjectsForSample(project.id, sample.id)

Retrieve a list of projects for this sample.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample

#Retrieve a list of projects for this sample.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 

### Return type

[**ProjectList**](ProjectList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of projects is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetSampleDataList**
> DataList GetSampleDataList(project.id, sample.id, full.text=var.full.text, id=var.id, filename=var.filename, filename.match.mode=var.filename.match.mode, file.path=var.file.path, file.path.match.mode='STARTS_WITH_CASE_INSENSITIVE', status=var.status, format.id=var.format.id, format.code=var.format.code, type=var.type, parent.folder.id=var.parent.folder.id, parent.folder.path=var.parent.folder.path, creation.date.after=var.creation.date.after, creation.date.before=var.creation.date.before, status.date.after=var.status.date.after, status.date.before=var.status.date.before, user.tag=var.user.tag, user.tag.match.mode=var.user.tag.match.mode, run.input.tag=var.run.input.tag, run.input.tag.match.mode=var.run.input.tag.match.mode, run.output.tag=var.run.output.tag, run.output.tag.match.mode=var.run.output.tag.match.mode, connector.tag=var.connector.tag, connector.tag.match.mode=var.connector.tag.match.mode, technical.tag=var.technical.tag, technical.tag.match.mode=var.technical.tag.match.mode, not.in.run=var.not.in.run, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve the list of sample data.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample to retrieve data for
var.full.text <- 'full.text_example' # character | To search through multiple fields of data.
var.id <- list("inner_example") # array[character] | The ids to filter on. This will always match exact.
var.filename <- list("inner_example") # array[character] | The filenames to filter on. The filenameMatchMode-parameter determines how the filtering is done.
var.filename.match.mode <- 'filename.match.mode_example' # character | How the filenames are filtered. 
var.file.path <- list("inner_example") # array[character] | The paths of the files to filter on.
var.file.path.match.mode <- 'STARTS_WITH_CASE_INSENSITIVE' # character | How the file paths are filtered:   - STARTS_WITH_CASE_INSENSITIVE: Filters the file path to start with the value of the 'filePath' parameter, regardless of upper/lower casing. This allows e.g. listing all data in a folder and all it's sub-folders (recursively).  - FULL_CASE_INSENSITIVE: Filters the file path to fully match the value of the 'filePath' parameter, regardless of upper/lower casing. Note that this can result in multiple results if e.g. two files exist with the same filename but different casing (abc.txt and ABC.txt).
var.status <- list("PARTIAL") # array[character] | The statuses to filter on.
var.format.id <- list("inner_example") # array[character] | The IDs of the formats to filter on.
var.format.code <- list("inner_example") # array[character] | The codes of the formats to filter on.
var.type <- 'type_example' # character | The type to filter on.
var.parent.folder.id <- list("inner_example") # array[character] | The IDs of parents folders to filter on. Lists all files and folders within the folder for the given ID, non-recursively.
var.parent.folder.path <- 'parent.folder.path_example' # character | The full path of the parent folder. Should start and end with a '/'. Lists all files and folders within the folder for the given path, non-recursively. This can be used to browse through the hierarchical tree of folders, e.g. traversing one level up can be done by removing the last part of the path.
var.creation.date.after <- 'creation.date.after_example' # character | The date after which the data is created. Format: yyyy-MM-dd'T'HH:mm:ss'Z' eg: 2021-01-30T08:30:00Z
var.creation.date.before <- 'creation.date.before_example' # character | The date before which the data is created. Format: yyyy-MM-dd'T'HH:mm:ss'Z' eg: 2021-01-30T08:30:00Z
var.status.date.after <- 'status.date.after_example' # character | The date after which the status has been updated. Format: yyyy-MM-dd'T'HH:mm:ss'Z' eg: 2021-01-30T08:30:00Z
var.status.date.before <- 'status.date.before_example' # character | The date before which the status has been updated. Format: yyyy-MM-dd'T'HH:mm:ss'Z' eg: 2021-01-30T08:30:00Z
var.user.tag <- list("inner_example") # array[character] | The usertags to filter on. The userTagMatchMode-parameter determines how the filtering is done.
var.user.tag.match.mode <- 'user.tag.match.mode_example' # character | How the usertags are filtered. 
var.run.input.tag <- list("inner_example") # array[character] | The runInputTags to filter on. The runInputTagMatchMode-parameter determines how the filtering is done.
var.run.input.tag.match.mode <- 'run.input.tag.match.mode_example' # character | How the runInputTags are filtered. 
var.run.output.tag <- list("inner_example") # array[character] | The runOutputTags to filter on. The runOutputTagMatchMode-parameter determines how the filtering is done.
var.run.output.tag.match.mode <- 'run.output.tag.match.mode_example' # character | How the runOutputTags are filtered. 
var.connector.tag <- list("inner_example") # array[character] | The connectorTags to filter on. The connectorTagMatchMode-parameter determines how the filtering is done.
var.connector.tag.match.mode <- 'connector.tag.match.mode_example' # character | How the connectorTags are filtered. 
var.technical.tag <- list("inner_example") # array[character] | The technicalTags to filter on. The techTagMatchMode-parameter determines how the filtering is done.
var.technical.tag.match.mode <- 'technical.tag.match.mode_example' # character | How the technicalTags are filtered. 
var.not.in.run <- 'not.in.run_example' # character | When set to true, the data will be filtered on data which is not used in a run.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - timeCreated - timeModified - name - path - fileSizeInBytes - status - format - dataType - willBeArchivedAt - willBeDeletedAt

#Retrieve the list of sample data.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample to retrieve data for | 
 **full.text** | **character**| To search through multiple fields of data. | [optional] 
 **id** | list( **character** )| The ids to filter on. This will always match exact. | [optional] 
 **filename** | list( **character** )| The filenames to filter on. The filenameMatchMode-parameter determines how the filtering is done. | [optional] 
 **filename.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the filenames are filtered.  | [optional] 
 **file.path** | list( **character** )| The paths of the files to filter on. | [optional] 
 **file.path.match.mode** | Enum [STARTS_WITH_CASE_INSENSITIVE, FULL_CASE_INSENSITIVE] | How the file paths are filtered:   - STARTS_WITH_CASE_INSENSITIVE: Filters the file path to start with the value of the &#39;filePath&#39; parameter, regardless of upper/lower casing. This allows e.g. listing all data in a folder and all it&#39;s sub-folders (recursively).  - FULL_CASE_INSENSITIVE: Filters the file path to fully match the value of the &#39;filePath&#39; parameter, regardless of upper/lower casing. Note that this can result in multiple results if e.g. two files exist with the same filename but different casing (abc.txt and ABC.txt). | [optional] [default to &#39;STARTS_WITH_CASE_INSENSITIVE&#39;]
 **status** | Enum [PARTIAL, AVAILABLE, ARCHIVING, ARCHIVED, UNARCHIVING, DELETING] | The statuses to filter on. | [optional] 
 **format.id** | list( **character** )| The IDs of the formats to filter on. | [optional] 
 **format.code** | list( **character** )| The codes of the formats to filter on. | [optional] 
 **type** | Enum [FILE, FOLDER] | The type to filter on. | [optional] 
 **parent.folder.id** | list( **character** )| The IDs of parents folders to filter on. Lists all files and folders within the folder for the given ID, non-recursively. | [optional] 
 **parent.folder.path** | **character**| The full path of the parent folder. Should start and end with a &#39;/&#39;. Lists all files and folders within the folder for the given path, non-recursively. This can be used to browse through the hierarchical tree of folders, e.g. traversing one level up can be done by removing the last part of the path. | [optional] 
 **creation.date.after** | **character**| The date after which the data is created. Format: yyyy-MM-dd&#39;T&#39;HH:mm:ss&#39;Z&#39; eg: 2021-01-30T08:30:00Z | [optional] 
 **creation.date.before** | **character**| The date before which the data is created. Format: yyyy-MM-dd&#39;T&#39;HH:mm:ss&#39;Z&#39; eg: 2021-01-30T08:30:00Z | [optional] 
 **status.date.after** | **character**| The date after which the status has been updated. Format: yyyy-MM-dd&#39;T&#39;HH:mm:ss&#39;Z&#39; eg: 2021-01-30T08:30:00Z | [optional] 
 **status.date.before** | **character**| The date before which the status has been updated. Format: yyyy-MM-dd&#39;T&#39;HH:mm:ss&#39;Z&#39; eg: 2021-01-30T08:30:00Z | [optional] 
 **user.tag** | list( **character** )| The usertags to filter on. The userTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **user.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the usertags are filtered.  | [optional] 
 **run.input.tag** | list( **character** )| The runInputTags to filter on. The runInputTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **run.input.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the runInputTags are filtered.  | [optional] 
 **run.output.tag** | list( **character** )| The runOutputTags to filter on. The runOutputTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **run.output.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the runOutputTags are filtered.  | [optional] 
 **connector.tag** | list( **character** )| The connectorTags to filter on. The connectorTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **connector.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the connectorTags are filtered.  | [optional] 
 **technical.tag** | list( **character** )| The technicalTags to filter on. The techTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **technical.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the technicalTags are filtered.  | [optional] 
 **not.in.run** | **character**| When set to true, the data will be filtered on data which is not used in a run. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - timeCreated - timeModified - name - path - fileSizeInBytes - status - format - dataType - willBeArchivedAt - willBeDeletedAt | [optional] 

### Return type

[**DataList**](DataList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of sample data is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetSampleHistory**
> SampleHistoryList GetSampleHistory(project.id, sample.id)

Retrieve sample history.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample

#Retrieve sample history.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 

### Return type

[**SampleHistoryList**](SampleHistoryList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The sample history is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetSampleMetadataField**
> Field GetSampleMetadataField(project.id, sample.id, field.id)

Retrieve a metadata field.

Returns a list of values for the field with identifier fieldId belonging to the sample with identifier sampleId. If the field is a group field that can occur more than once or belongs to a group field that can occur more than once the return value will have one entry in the list for each occurrence. If not the return value will be a single value list

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample
var.field.id <- 'field.id_example' # character | The ID of the field

#Retrieve a metadata field.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 
 **field.id** | **character**| The ID of the field | 

### Return type

[**Field**](Field.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The metadata field is successfully retrieved.  |  -  |
| **0** | A problem occurred. |  -  |

# **GetSampleMetadataFieldCount**
> Field GetSampleMetadataFieldCount(project.id, sample.id, field.id)

Retrieves the number of occurrences of a given field.

Returns a list of values for the field with identifier fieldId belonging to the sample with identifier sampleId. If the field is a group field that can occur more than once or belongs to a group field that can occur more than once the return value will have one entry in the list for each occurrence. If not the return value will be a single value list

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample
var.field.id <- 'field.id_example' # character | The ID of the field

#Retrieves the number of occurrences of a given field.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 
 **field.id** | **character**| The ID of the field | 

### Return type

[**Field**](Field.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The number of occurrences is successfully retrieved.  |  -  |
| **0** | A problem occurred. |  -  |

# **LinkDataToSample**
> LinkDataToSample(project.id, sample.id, data.id)

Link data to a sample.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample
var.data.id <- 'data.id_example' # character | The ID of the data to link

#Link data to a sample.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 
 **data.id** | **character**| The ID of the data to link | 

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
| **204** | The data is successfully linked to the sample. |  -  |
| **0** | A problem occurred. |  -  |

# **LinkSampleToProject**
> ProjectSample LinkSampleToProject(project.id, sample.id)

Link a sample to a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | 

#Link a sample to a project.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**|  | 

### Return type

[**ProjectSample**](ProjectSample.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The sample is successfully linked to the project. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **MarkSampleDeleted**
> MarkSampleDeleted(project.id, sample.id)

Mark a sample deleted.

Endpoint for marking a sample as deleted.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample

#Mark a sample deleted.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 

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
| **200** | The sample is successfully marked as deleted. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkDataFromSample**
> UnlinkDataFromSample(project.id, sample.id, data.id)

Unlink data from a sample.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | The ID of the sample
var.data.id <- 'data.id_example' # character | The ID of the data to unlink

#Unlink data from a sample.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**| The ID of the sample | 
 **data.id** | **character**| The ID of the data to unlink | 

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
| **204** | The data is successfully unlinked from the sample. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkSampleFromProject**
> UnlinkSampleFromProject(project.id, sample.id)

Unlink a sample from a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | 

#Unlink a sample from a project.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**|  | 

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
| **204** | The sample is successfully unlinked from the project. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateProjectSample**
> ProjectSample UpdateProjectSample(project.id, sample.id, if.match=var.if.match, project.sample=var.project.sample)

Update a project sample.

Fields which can be updated: - sample.name - sample.description - sample.status - sample.tags

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | 
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.project.sample <- ProjectSample$new(Sample$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", SampleTag$new(list("technicalTags_example"), list("userTags_example"), list("connectorTags_example"), list("runInTags_example")), Region$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "cityName_example", "tenantName_example"), "DELETED", "metadataValid_example", list(MetadataField$new("id_example", 123, "name_example", "TEXT", list("values_example"), list(MetadataField$new("id_example", 123, "name_example", "TEXT", list("values_example"), list(...))))), "tenantName_example", "description_example"), "projectId_example") # ProjectSample | 

#Update a project sample.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**|  | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **project.sample** | [**ProjectSample**](ProjectSample.md)|  | [optional] 

### Return type

[**ProjectSample**](ProjectSample.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The sample is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **UpdateSampleMetadataFields**
> Sample UpdateSampleMetadataFields(project.id, sample.id, update.metadata=var.update.metadata)

Update metadata fields.

Endpoint for updating metadata fields.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | 
var.update.metadata <- UpdateMetadata$new(list(UpdateSingleMetadataField$new(FieldId$new("id_example"), "fieldName_example", list("values_example"))), list(UpdateMetadataFieldGroup$new(123, list(UpdateSingleMetadataField$new(FieldId$new("id_example"), "fieldName_example", list("values_example"))), FieldId$new("id_example"), "fieldName_example"))) # UpdateMetadata | 

#Update metadata fields.
api.instance <- ProjectSampleApi$new()
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
 **sample.id** | **character**|  | 
 **update.metadata** | [**UpdateMetadata**](UpdateMetadata.md)|  | [optional] 

### Return type

[**Sample**](Sample.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The metadata is successfully updated. |  -  |
| **0** | A problem occurred. |  -  |

