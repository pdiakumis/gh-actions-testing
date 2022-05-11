# ProjectDataApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddSecondaryData**](ProjectDataApi.md#AddSecondaryData) | **POST** /api/projects/{projectId}/data/{dataId}/secondaryData/{secondaryDataId} | Add secondary data to data.
[**ArchiveData**](ProjectDataApi.md#ArchiveData) | **POST** /api/projects/{projectId}/data/{dataId}:archive | Schedule this data for archival.
[**CompleteFolderUploadSession**](ProjectDataApi.md#CompleteFolderUploadSession) | **POST** /api/projects/{projectId}/data/{dataId}/folderUploadSessions/{folderUploadSessionId}:complete | Complete a trackable folder upload session.
[**CreateDataInProject**](ProjectDataApi.md#CreateDataInProject) | **POST** /api/projects/{projectId}/data | Create data in this project.
[**CreateDownloadUrlForData**](ProjectDataApi.md#CreateDownloadUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createDownloadUrl | Retrieve a download URL for this data.
[**CreateFolderUploadSession**](ProjectDataApi.md#CreateFolderUploadSession) | **POST** /api/projects/{projectId}/data/{dataId}/folderUploadSessions | Create a trackable folder upload session.
[**CreateInlineViewUrlForData**](ProjectDataApi.md#CreateInlineViewUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createInlineViewUrl | Retrieve an URL for this data to use for inline view in a browser.
[**CreateTemporaryCredentialsForData**](ProjectDataApi.md#CreateTemporaryCredentialsForData) | **POST** /api/projects/{projectId}/data/{dataId}:createTemporaryCredentials | Retrieve temporary credentials for this data.
[**CreateUploadUrlForData**](ProjectDataApi.md#CreateUploadUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createUploadUrl | Retrieve an upload URL for this data.
[**DeleteData**](ProjectDataApi.md#DeleteData) | **POST** /api/projects/{projectId}/data/{dataId}:delete | Schedule this data for deletion.
[**GetDataEligibleForLinking**](ProjectDataApi.md#GetDataEligibleForLinking) | **GET** /api/projects/{projectId}/data/eligibleForLinking | Retrieve a list of data eligible for linking to the current project.
[**GetFolderUploadSession**](ProjectDataApi.md#GetFolderUploadSession) | **GET** /api/projects/{projectId}/data/{dataId}/folderUploadSessions/{folderUploadSessionId} | Retrieve folder upload session details.
[**GetNonSampleProjectData**](ProjectDataApi.md#GetNonSampleProjectData) | **GET** /api/projects/{projectId}/data/nonSampleData | Retrieve a list of project data not linked to a sample.
[**GetProjectData**](ProjectDataApi.md#GetProjectData) | **GET** /api/projects/{projectId}/data/{dataId} | Retrieve a project data.
[**GetProjectDataChildren**](ProjectDataApi.md#GetProjectDataChildren) | **GET** /api/projects/{projectId}/data/{dataId}/children | Retrieve the children of this data.
[**GetProjectDataList**](ProjectDataApi.md#GetProjectDataList) | **GET** /api/projects/{projectId}/data | Retrieve the list of project data.
[**GetProjectsLinkedToData**](ProjectDataApi.md#GetProjectsLinkedToData) | **GET** /api/projects/{projectId}/data/{dataId}/linkedProjects | Retrieve a list of projects to which this data is linked.
[**GetSecondaryData**](ProjectDataApi.md#GetSecondaryData) | **GET** /api/projects/{projectId}/data/{dataId}/secondaryData | Retrieve a list of secondary data for data.
[**LinkDataToProject**](ProjectDataApi.md#LinkDataToProject) | **POST** /api/projects/{projectId}/data/{dataId} | Link data to this project.
[**RemoveSecondaryData**](ProjectDataApi.md#RemoveSecondaryData) | **DELETE** /api/projects/{projectId}/data/{dataId}/secondaryData/{secondaryDataId} | Remove secondary data from data.
[**ScheduleDownloadForData**](ProjectDataApi.md#ScheduleDownloadForData) | **POST** /api/projects/{projectId}/data/{dataId}:scheduleDownload | Schedule a download.
[**UnarchiveData**](ProjectDataApi.md#UnarchiveData) | **POST** /api/projects/{projectId}/data/{dataId}:unarchive | Schedule this data for unarchival.
[**UnlinkDataFromProject**](ProjectDataApi.md#UnlinkDataFromProject) | **POST** /api/projects/{projectId}/data/{dataId}:unlink | Unlink data from this project.
[**UpdateProjectData**](ProjectDataApi.md#UpdateProjectData) | **PUT** /api/projects/{projectId}/data/{dataId} | Update this project data.


# **AddSecondaryData**
> AddSecondaryData(project.id, data.id, secondary.data.id)

Add secondary data to data.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.secondary.data.id <- 'secondary.data.id_example' # character | 

#Add secondary data to data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **secondary.data.id** | **character**|  | 

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
| **204** | The secondary data is successfully added. |  -  |
| **0** | A problem occurred. |  -  |

# **ArchiveData**
> ArchiveData(project.id, data.id)

Schedule this data for archival.

Endpoint for scheduling this data for archival. This will also archive all files and directories below that data.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Schedule this data for archival.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

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
| **204** | The data is successfully scheduled for archival. |  -  |
| **0** | A problem occurred. |  -  |

# **CompleteFolderUploadSession**
> FolderUploadSession CompleteFolderUploadSession(project.id, data.id, folder.upload.session.id, complete.folder.upload.session=var.complete.folder.upload.session)

Complete a trackable folder upload session.

Complete a trackable folder upload session. By completing the folder upload session, and specifying how many files you have uploaded, ICA can ensure that all uploaded files are accounted for.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.folder.upload.session.id <- 'folder.upload.session.id_example' # character | 
var.complete.folder.upload.session <- CompleteFolderUploadSession$new(123) # CompleteFolderUploadSession | The info required to complete the folder upload session.

#Complete a trackable folder upload session.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **folder.upload.session.id** | **character**|  | 
 **complete.folder.upload.session** | [**CompleteFolderUploadSession**](CompleteFolderUploadSession.md)| The info required to complete the folder upload session. | [optional] 

### Return type

[**FolderUploadSession**](FolderUploadSession.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The folder upload session is successfully completed. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateDataInProject**
> ProjectData CreateDataInProject(project.id, create.data=var.create.data)

Create data in this project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.create.data <- CreateData$new("name_example", "FILE", "folderId_example", "folderPath_example", "formatCode_example") # CreateData | The data to create.

#Create data in this project.
api.instance <- ProjectDataApi$new()
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
 **create.data** | [**CreateData**](CreateData.md)| The data to create. | [optional] 

### Return type

[**ProjectData**](ProjectData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The data is successfully created in this project. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **CreateDownloadUrlForData**
> Download CreateDownloadUrlForData(project.id, data.id)

Retrieve a download URL for this data.

Can be used to download a file directly from the region where it is located, no connector is needed.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Retrieve a download URL for this data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

### Return type

[**Download**](Download.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The download URL is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateFolderUploadSession**
> FolderUploadSession CreateFolderUploadSession(project.id, data.id, create.temporary.credentials=var.create.temporary.credentials)

Create a trackable folder upload session.

This endpoint can be used to ensure that all uploaded files within the requested session are accounted for. This call has to be used together with the :complete endpoint once upload is done.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.create.temporary.credentials <- CreateTemporaryCredentials$new("RCLONE") # CreateTemporaryCredentials | Temporary credentials request options.

#Create a trackable folder upload session.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **create.temporary.credentials** | [**CreateTemporaryCredentials**](CreateTemporaryCredentials.md)| Temporary credentials request options. | [optional] 

### Return type

[**FolderUploadSession**](FolderUploadSession.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The folder upload session is successfully created. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateInlineViewUrlForData**
> InlineView CreateInlineViewUrlForData(project.id, data.id)

Retrieve an URL for this data to use for inline view in a browser.

Can be used to view a file directly from the region where it is located, no connector is needed. Only small files can be viewed, otherwise a response with status 400 will be returned if the file is too big.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Retrieve an URL for this data to use for inline view in a browser.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

### Return type

[**InlineView**](InlineView.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The inline view URL is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateTemporaryCredentialsForData**
> TempCredentials CreateTemporaryCredentialsForData(project.id, data.id, create.temporary.credentials=var.create.temporary.credentials)

Retrieve temporary credentials for this data.

Can be used to upload or download a file directly from the region where it is located, no connector is needed.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.create.temporary.credentials <- CreateTemporaryCredentials$new("RCLONE") # CreateTemporaryCredentials | Temporary credentials request options.

#Retrieve temporary credentials for this data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **create.temporary.credentials** | [**CreateTemporaryCredentials**](CreateTemporaryCredentials.md)| Temporary credentials request options. | [optional] 

### Return type

[**TempCredentials**](TempCredentials.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The temporary credentials are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateUploadUrlForData**
> Upload CreateUploadUrlForData(project.id, data.id, file.type=var.file.type, hash=var.hash)

Retrieve an upload URL for this data.

Can be used to upload a file directly from the region where it is located, no connector is needed. Only small files can be uploaded, otherwise a response with status 400 will be returned if the file is too big.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.file.type <- 'file.type_example' # character | 
var.hash <- 'hash_example' # character | 

#Retrieve an upload URL for this data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **file.type** | **character**|  | [optional] 
 **hash** | **character**|  | [optional] 

### Return type

[**Upload**](Upload.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The upload URL is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **DeleteData**
> DeleteData(project.id, data.id)

Schedule this data for deletion.

Endpoint for scheduling this data for deletion. This will also delete all files and directories below that data.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Schedule this data for deletion.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

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
| **204** | The data is successfully scheduled for deletion. |  -  |
| **0** | A problem occurred. |  -  |

# **GetDataEligibleForLinking**
> DataPagedList GetDataEligibleForLinking(project.id, full.text=var.full.text, id=var.id, filename=var.filename, filename.match.mode=var.filename.match.mode, file.path=var.file.path, file.path.match.mode='STARTS_WITH_CASE_INSENSITIVE', status=var.status, format.id=var.format.id, format.code=var.format.code, type=var.type, parent.folder.id=var.parent.folder.id, parent.folder.path=var.parent.folder.path, creation.date.after=var.creation.date.after, creation.date.before=var.creation.date.before, status.date.after=var.status.date.after, status.date.before=var.status.date.before, user.tag=var.user.tag, user.tag.match.mode=var.user.tag.match.mode, run.input.tag=var.run.input.tag, run.input.tag.match.mode=var.run.input.tag.match.mode, run.output.tag=var.run.output.tag, run.output.tag.match.mode=var.run.output.tag.match.mode, connector.tag=var.connector.tag, connector.tag.match.mode=var.connector.tag.match.mode, technical.tag=var.technical.tag, technical.tag.match.mode=var.technical.tag.match.mode, not.in.run=var.not.in.run, not.linked.to.sample=var.not.linked.to.sample, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve a list of data eligible for linking to the current project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
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
var.not.linked.to.sample <- 'not.linked.to.sample_example' # character | When set to true only data that is unlinked to a sample will be returned. This filter implies a filter of type File.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - timeCreated - timeModified - name - path - fileSizeInBytes - status - format - dataType - willBeArchivedAt - willBeDeletedAt

#Retrieve a list of data eligible for linking to the current project.
api.instance <- ProjectDataApi$new()
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
 **not.linked.to.sample** | **character**| When set to true only data that is unlinked to a sample will be returned. This filter implies a filter of type File. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - timeCreated - timeModified - name - path - fileSizeInBytes - status - format - dataType - willBeArchivedAt - willBeDeletedAt | [optional] 

### Return type

[**DataPagedList**](DataPagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of data is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetFolderUploadSession**
> FolderUploadSession GetFolderUploadSession(project.id, data.id, folder.upload.session.id)

Retrieve folder upload session details.

Retrieve folder upload session details, including the current status of your upload session.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.folder.upload.session.id <- 'folder.upload.session.id_example' # character | 

#Retrieve folder upload session details.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **folder.upload.session.id** | **character**|  | 

### Return type

[**FolderUploadSession**](FolderUploadSession.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The folder upload session details are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetNonSampleProjectData**
> ProjectDataPagedList GetNonSampleProjectData(project.id, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size)

Retrieve a list of project data not linked to a sample.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.

#Retrieve a list of project data not linked to a sample.
api.instance <- ProjectDataApi$new()
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

### Return type

[**ProjectDataPagedList**](ProjectDataPagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of project data is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjectData**
> ProjectData GetProjectData(project.id, data.id)

Retrieve a project data.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Retrieve a project data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

### Return type

[**ProjectData**](ProjectData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project data is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetProjectDataChildren**
> DataList GetProjectDataChildren(project.id, data.id)

Retrieve the children of this data.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Retrieve the children of this data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

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
| **200** | The list of data children is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjectDataList**
> ProjectDataPagedList GetProjectDataList(project.id, full.text=var.full.text, id=var.id, filename=var.filename, filename.match.mode=var.filename.match.mode, file.path=var.file.path, file.path.match.mode='STARTS_WITH_CASE_INSENSITIVE', status=var.status, format.id=var.format.id, format.code=var.format.code, type=var.type, parent.folder.id=var.parent.folder.id, parent.folder.path=var.parent.folder.path, creation.date.after=var.creation.date.after, creation.date.before=var.creation.date.before, status.date.after=var.status.date.after, status.date.before=var.status.date.before, user.tag=var.user.tag, user.tag.match.mode=var.user.tag.match.mode, run.input.tag=var.run.input.tag, run.input.tag.match.mode=var.run.input.tag.match.mode, run.output.tag=var.run.output.tag, run.output.tag.match.mode=var.run.output.tag.match.mode, connector.tag=var.connector.tag, connector.tag.match.mode=var.connector.tag.match.mode, technical.tag=var.technical.tag, technical.tag.match.mode=var.technical.tag.match.mode, not.in.run=var.not.in.run, not.linked.to.sample=var.not.linked.to.sample, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve the list of project data.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
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
var.not.linked.to.sample <- 'not.linked.to.sample_example' # character | When set to true only data that is unlinked to a sample will be returned.  This filter implies a filter of type File.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - timeCreated - timeModified - name - path - fileSizeInBytes - status - format - dataType - willBeArchivedAt - willBeDeletedAt

#Retrieve the list of project data.
api.instance <- ProjectDataApi$new()
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
 **not.linked.to.sample** | **character**| When set to true only data that is unlinked to a sample will be returned.  This filter implies a filter of type File. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - timeCreated - timeModified - name - path - fileSizeInBytes - status - format - dataType - willBeArchivedAt - willBeDeletedAt | [optional] 

### Return type

[**ProjectDataPagedList**](ProjectDataPagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of project data is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjectsLinkedToData**
> ProjectList GetProjectsLinkedToData(project.id, data.id)

Retrieve a list of projects to which this data is linked.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Retrieve a list of projects to which this data is linked.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

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

# **GetSecondaryData**
> DataList GetSecondaryData(project.id, data.id)

Retrieve a list of secondary data for data.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Retrieve a list of secondary data for data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

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
| **200** | The list of secondary data is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **LinkDataToProject**
> ProjectData LinkDataToProject(project.id, data.id)

Link data to this project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Link data to this project.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

### Return type

[**ProjectData**](ProjectData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The data is successfully linked to the project. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **RemoveSecondaryData**
> RemoveSecondaryData(project.id, data.id, secondary.data.id)

Remove secondary data from data.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.secondary.data.id <- 'secondary.data.id_example' # character | 

#Remove secondary data from data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **secondary.data.id** | **character**|  | 

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
| **204** | The secondary data is successfully removed. |  -  |
| **0** | A problem occurred. |  -  |

# **ScheduleDownloadForData**
> DataTransfer ScheduleDownloadForData(project.id, data.id, schedule.download)

Schedule a download.

Endpoint for scheduling a download for the data specified by the ID to a connector. This download will only start when the connector is running. This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.schedule.download <- ScheduleDownload$new("connectorId_example", "HTTPS", "localPath_example", "disableHashing_example") # ScheduleDownload | 

#Schedule a download.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **schedule.download** | [**ScheduleDownload**](ScheduleDownload.md)|  | 

### Return type

[**DataTransfer**](DataTransfer.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **0** | The datatransfer which is scheduled. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |

# **UnarchiveData**
> UnarchiveData(project.id, data.id)

Schedule this data for unarchival.

Endpoint for scheduling this data for unarchival. This will also unarchive all files and directories below that data. This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Schedule this data for unarchival.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

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
| **204** | The data is successfully scheduled for unarchival. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkDataFromProject**
> UnlinkDataFromProject(project.id, data.id)

Unlink data from this project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Unlink data from this project.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 

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
| **204** | The data is successfully unlinked from this project. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateProjectData**
> ProjectData UpdateProjectData(project.id, data.id, project.data=var.project.data)

Update this project data.

Fields which can be updated for files:  - data.willBeArchivedAt  - data.willBeDeletedAt  - data.format  - data.tags  Fields which can be updated for folders:  - data.tags  

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.data.id <- 'data.id_example' # character | 
var.project.data <- ProjectData$new(Data$new("id_example", DataDetails$new("timeCreated_example", "timeModified_example", "tenantId_example", "owningProjectId_example", "name_example", "PARTIAL", DataTag$new(list("technicalTags_example"), list("userTags_example"), list("connectorTags_example"), list("runInTags_example"), list("runOutTags_example"), list("referenceTags_example")), "FILE", "tenantName_example", "path_example", 123, DataFormat$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "tenantName_example", "description_example", "mimeType_example"), "objectETag_example", "storedForTheFirstTimeAt_example", Region$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "cityName_example", "tenantName_example"), "willBeArchivedAt_example", "willBeDeletedAt_example")), "projectId_example") # ProjectData | The updated project data.

#Update this project data.
api.instance <- ProjectDataApi$new()
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
 **data.id** | **character**|  | 
 **project.data** | [**ProjectData**](ProjectData.md)| The updated project data. | [optional] 

### Return type

[**ProjectData**](ProjectData.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project data is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

