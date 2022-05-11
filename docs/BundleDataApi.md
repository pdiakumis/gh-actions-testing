# BundleDataApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBundleData**](BundleDataApi.md#GetBundleData) | **GET** /api/bundles/{bundleId}/data | Retrieve the list of bundle data.
[**LinkDataToBundle**](BundleDataApi.md#LinkDataToBundle) | **POST** /api/bundles/{bundleId}/data/{dataId} | Link data to this bundle.
[**UnlinkDataFromBundle**](BundleDataApi.md#UnlinkDataFromBundle) | **DELETE** /api/bundles/{bundleId}/data/{dataId} | Unlink data from this bundle.


# **GetBundleData**
> BundleDataPagedList GetBundleData(bundle.id, full.text=var.full.text, id=var.id, filename=var.filename, filename.match.mode=var.filename.match.mode, file.path=var.file.path, file.path.match.mode='STARTS_WITH_CASE_INSENSITIVE', status=var.status, format.id=var.format.id, format.code=var.format.code, type=var.type, parent.folder.id=var.parent.folder.id, parent.folder.path=var.parent.folder.path, creation.date.after=var.creation.date.after, creation.date.before=var.creation.date.before, status.date.after=var.status.date.after, status.date.before=var.status.date.before, user.tag=var.user.tag, user.tag.match.mode=var.user.tag.match.mode, run.input.tag=var.run.input.tag, run.input.tag.match.mode=var.run.input.tag.match.mode, run.output.tag=var.run.output.tag, run.output.tag.match.mode=var.run.output.tag.match.mode, connector.tag=var.connector.tag, connector.tag.match.mode=var.connector.tag.match.mode, technical.tag=var.technical.tag, technical.tag.match.mode=var.technical.tag.match.mode, not.in.run=var.not.in.run, not.linked.to.sample=var.not.linked.to.sample, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve the list of bundle data.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | 
var.full.text <- 'full.text_example' # character | To search through multiple fields of data.
var.id <- 'id_example' # character | The ids to filter on. This will always match exact.
var.filename <- 'filename_example' # character | The filenames to filter on. The filenameMatchMode-parameter determines how the filtering is done.
var.filename.match.mode <- 'filename.match.mode_example' # character | How the filenames are filtered.
var.file.path <- 'file.path_example' # character | The paths of the files to filter on.
var.file.path.match.mode <- 'STARTS_WITH_CASE_INSENSITIVE' # character | How the file paths are filtered:   - STARTS_WITH_CASE_INSENSITIVE: Filters the file path to start with the value of the 'filePath' parameter, regardless of upper/lower casing. This allows e.g. listing all data in a folder and all it's sub-folders (recursively).  - FULL_CASE_INSENSITIVE: Filters the file path to fully match the value of the 'filePath' parameter, regardless of upper/lower casing. Note that this can result in multiple results if e.g. two files exist with the same filename but different casing (abc.txt and ABC.txt).
var.status <- 'status_example' # character | The statuses to filter on.
var.format.id <- 'format.id_example' # character | The IDs of the formats to filter on.
var.format.code <- 'format.code_example' # character | The codes of the formats to filter on.
var.type <- 'type_example' # character | The type to filter on.
var.parent.folder.id <- 'parent.folder.id_example' # character | The IDs of parents folders to filter on. Lists all files and folders within the folder for the given ID, non-recursively.
var.parent.folder.path <- 'parent.folder.path_example' # character | The full path of the parent folder. Should start and end with a '/'. Lists all files and folders within the folder for the given path, non-recursively. This can be used to browse through the hierarchical tree of folders, e.g. traversing one level up can be done by removing the last part of the path.
var.creation.date.after <- 'creation.date.after_example' # character | The date after which the data is created. Format: yyyy-MM-dd'T'HH:mm:ss'Z' eg: 2021-01-30T08:30:00Z
var.creation.date.before <- 'creation.date.before_example' # character | The date before which the data is created. Format: yyyy-MM-dd'T'HH:mm:ss'Z' eg: 2021-01-30T08:30:00Z
var.status.date.after <- 'status.date.after_example' # character | The date after which the status has been updated. Format: yyyy-MM-dd'T'HH:mm:ss'Z' eg: 2021-01-30T08:30:00Z
var.status.date.before <- 'status.date.before_example' # character | The date before which the status has been updated Format: yyyy-MM-dd'T'HH:mm:ss'Z' eg: 2021-01-30T08:30:00Z
var.user.tag <- 'user.tag_example' # character | The usertags to filter on. The userTagMatchMode-parameter determines how the filtering is done.
var.user.tag.match.mode <- 'user.tag.match.mode_example' # character | How the usertags are filtered.
var.run.input.tag <- 'run.input.tag_example' # character | The runInputTags to filter on. The runInputTagMatchMode-parameter determines how the filtering is done.
var.run.input.tag.match.mode <- 'run.input.tag.match.mode_example' # character | How the runInputTags are filtered.
var.run.output.tag <- 'run.output.tag_example' # character | The runOutputTags to filter on. The runOutputTagMatchMode-parameter determines how the filtering is done.
var.run.output.tag.match.mode <- 'run.output.tag.match.mode_example' # character | How the runOutputTags are filtered.
var.connector.tag <- 'connector.tag_example' # character | The connectorTags to filter on. The connectorTagMatchMode-parameter determines how the filtering is done.
var.connector.tag.match.mode <- 'connector.tag.match.mode_example' # character | How the connectorTags are filtered.
var.technical.tag <- 'technical.tag_example' # character | The technicalTags to filter on. The techTagMatchMode-parameter determines how the filtering is done.
var.technical.tag.match.mode <- 'technical.tag.match.mode_example' # character | How the technicalTags are filtered.
var.not.in.run <- 'not.in.run_example' # character | When set to true, the data will be filtered on data which is not used in a run.
var.not.linked.to.sample <- 'not.linked.to.sample_example' # character | When set to true only date that is unlinked to a sample will be returned.  This filter implies a filter of type File.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - timeCreated - timeModified - name - path - fileSizeInBytes - status - format - dataType - willBeArchivedAt - willBeDeletedAt

#Retrieve the list of bundle data.
api.instance <- BundleDataApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**|  | 
 **full.text** | **character**| To search through multiple fields of data. | [optional] 
 **id** | **character**| The ids to filter on. This will always match exact. | [optional] 
 **filename** | **character**| The filenames to filter on. The filenameMatchMode-parameter determines how the filtering is done. | [optional] 
 **filename.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the filenames are filtered. | [optional] 
 **file.path** | **character**| The paths of the files to filter on. | [optional] 
 **file.path.match.mode** | Enum [STARTS_WITH_CASE_INSENSITIVE, FULL_CASE_INSENSITIVE] | How the file paths are filtered:   - STARTS_WITH_CASE_INSENSITIVE: Filters the file path to start with the value of the &#39;filePath&#39; parameter, regardless of upper/lower casing. This allows e.g. listing all data in a folder and all it&#39;s sub-folders (recursively).  - FULL_CASE_INSENSITIVE: Filters the file path to fully match the value of the &#39;filePath&#39; parameter, regardless of upper/lower casing. Note that this can result in multiple results if e.g. two files exist with the same filename but different casing (abc.txt and ABC.txt). | [optional] [default to &#39;STARTS_WITH_CASE_INSENSITIVE&#39;]
 **status** | Enum [PARTIAL, AVAILABLE, ARCHIVING, ARCHIVED, UNARCHIVING, DELETING] | The statuses to filter on. | [optional] 
 **format.id** | **character**| The IDs of the formats to filter on. | [optional] 
 **format.code** | **character**| The codes of the formats to filter on. | [optional] 
 **type** | Enum [FILE, FOLDER] | The type to filter on. | [optional] 
 **parent.folder.id** | **character**| The IDs of parents folders to filter on. Lists all files and folders within the folder for the given ID, non-recursively. | [optional] 
 **parent.folder.path** | **character**| The full path of the parent folder. Should start and end with a &#39;/&#39;. Lists all files and folders within the folder for the given path, non-recursively. This can be used to browse through the hierarchical tree of folders, e.g. traversing one level up can be done by removing the last part of the path. | [optional] 
 **creation.date.after** | **character**| The date after which the data is created. Format: yyyy-MM-dd&#39;T&#39;HH:mm:ss&#39;Z&#39; eg: 2021-01-30T08:30:00Z | [optional] 
 **creation.date.before** | **character**| The date before which the data is created. Format: yyyy-MM-dd&#39;T&#39;HH:mm:ss&#39;Z&#39; eg: 2021-01-30T08:30:00Z | [optional] 
 **status.date.after** | **character**| The date after which the status has been updated. Format: yyyy-MM-dd&#39;T&#39;HH:mm:ss&#39;Z&#39; eg: 2021-01-30T08:30:00Z | [optional] 
 **status.date.before** | **character**| The date before which the status has been updated Format: yyyy-MM-dd&#39;T&#39;HH:mm:ss&#39;Z&#39; eg: 2021-01-30T08:30:00Z | [optional] 
 **user.tag** | **character**| The usertags to filter on. The userTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **user.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the usertags are filtered. | [optional] 
 **run.input.tag** | **character**| The runInputTags to filter on. The runInputTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **run.input.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the runInputTags are filtered. | [optional] 
 **run.output.tag** | **character**| The runOutputTags to filter on. The runOutputTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **run.output.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the runOutputTags are filtered. | [optional] 
 **connector.tag** | **character**| The connectorTags to filter on. The connectorTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **connector.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the connectorTags are filtered. | [optional] 
 **technical.tag** | **character**| The technicalTags to filter on. The techTagMatchMode-parameter determines how the filtering is done. | [optional] 
 **technical.tag.match.mode** | Enum [EXACT, EXCLUDE, FUZZY] | How the technicalTags are filtered. | [optional] 
 **not.in.run** | **character**| When set to true, the data will be filtered on data which is not used in a run. | [optional] 
 **not.linked.to.sample** | **character**| When set to true only date that is unlinked to a sample will be returned.  This filter implies a filter of type File. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - timeCreated - timeModified - name - path - fileSizeInBytes - status - format - dataType - willBeArchivedAt - willBeDeletedAt | [optional] 

### Return type

[**BundleDataPagedList**](BundleDataPagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of bundle data is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **LinkDataToBundle**
> LinkDataToBundle(bundle.id, data.id)

Link data to this bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Link data to this bundle.
api.instance <- BundleDataApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**|  | 
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
| **204** | The data is successfully linked to this bundle. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkDataFromBundle**
> UnlinkDataFromBundle(bundle.id, data.id)

Unlink data from this bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | 
var.data.id <- 'data.id_example' # character | 

#Unlink data from this bundle.
api.instance <- BundleDataApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**|  | 
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
| **204** | The data is successfully unlinked from this bundle. |  -  |
| **0** | A problem occurred. |  -  |

