# ProjectApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateProject**](ProjectApi.md#CreateProject) | **POST** /api/projects | Create a new project.
[**GetProject**](ProjectApi.md#GetProject) | **GET** /api/projects/{projectId} | Retrieve a project.
[**GetProjectBundle**](ProjectApi.md#GetProjectBundle) | **GET** /api/projects/{projectId}/bundles/{bundleId} | Retrieve a project bundle.
[**GetProjectBundles**](ProjectApi.md#GetProjectBundles) | **GET** /api/projects/{projectId}/bundles | Retrieve project bundles.
[**GetProjects**](ProjectApi.md#GetProjects) | **GET** /api/projects | Retrieve a list of projects.
[**LinkProjectBundle**](ProjectApi.md#LinkProjectBundle) | **POST** /api/projects/{projectId}/bundles/{bundleId} | Link a bundle to a project.
[**UnlinkProjectBundle**](ProjectApi.md#UnlinkProjectBundle) | **DELETE** /api/projects/{projectId}/bundles/{bundleId} | Unlink a bundle from a project.
[**UpdateProject**](ProjectApi.md#UpdateProject) | **PUT** /api/projects/{projectId} | Update a project.


# **CreateProject**
> Project CreateProject(create.project=var.create.project)

Create a new project.

### Example
```R
library(icar)

var.create.project <- CreateProject$new("name_example", "regionId_example", "PROJECT", "dataSharingEnabled_example", "storageBundleId_example", "shortDescription_example", "information_example", "projectOwnerId_example", ProjectTag$new(list("technicalTags_example"), list("userTags_example")), "metadataModelId_example", "storageConfigurationId_example", "storageConfigurationSubfolder_example") # CreateProject | 

#Create a new project.
api.instance <- ProjectApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create.project** | [**CreateProject**](CreateProject.md)|  | [optional] 

### Return type

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The project is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetProject**
> Project GetProject(project.id)

Retrieve a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 

#Retrieve a project.
api.instance <- ProjectApi$new()
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

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetProjectBundle**
> ProjectBundle GetProjectBundle(project.id, bundle.id)

Retrieve a project bundle.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.bundle.id <- 'bundle.id_example' # character | 

#Retrieve a project bundle.
api.instance <- ProjectApi$new()
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
 **bundle.id** | **character**|  | 

### Return type

[**ProjectBundle**](ProjectBundle.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project bundle is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjectBundles**
> ProjectBundleList GetProjectBundles(project.id)

Retrieve project bundles.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 

#Retrieve project bundles.
api.instance <- ProjectApi$new()
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

[**ProjectBundleList**](ProjectBundleList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project bundles are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetProjects**
> ProjectPagedList GetProjects(search=var.search, user.tags=var.user.tags, technical.tags=var.technical.tags, include.hidden.projects=FALSE, region=var.region, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve a list of projects.

### Example
```R
library(icar)

var.search <- 'search_example' # character | Search
var.user.tags <- list("inner_example") # array[character] | User tags to filter on
var.technical.tags <- list("inner_example") # array[character] | Technical tags to filter on
var.include.hidden.projects <- FALSE # character | Include hidden projects.
var.region <- 'region_example' # character | The ID of the region to filter on.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - name - shortDescription - information

#Retrieve a list of projects.
api.instance <- ProjectApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search** | **character**| Search | [optional] 
 **user.tags** | list( **character** )| User tags to filter on | [optional] 
 **technical.tags** | list( **character** )| Technical tags to filter on | [optional] 
 **include.hidden.projects** | **character**| Include hidden projects. | [optional] [default to FALSE]
 **region** | **character**| The ID of the region to filter on. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - name - shortDescription - information | [optional] 

### Return type

[**ProjectPagedList**](ProjectPagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of projects is successfully retrieved |  -  |
| **0** | A problem occurred. |  -  |

# **LinkProjectBundle**
> ProjectBundle LinkProjectBundle(project.id, bundle.id)

Link a bundle to a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.bundle.id <- 'bundle.id_example' # character | 

#Link a bundle to a project.
api.instance <- ProjectApi$new()
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
 **bundle.id** | **character**|  | 

### Return type

[**ProjectBundle**](ProjectBundle.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The bundle is successfully linked to the project. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkProjectBundle**
> UnlinkProjectBundle(project.id, bundle.id)

Unlink a bundle from a project.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.bundle.id <- 'bundle.id_example' # character | 

#Unlink a bundle from a project.
api.instance <- ProjectApi$new()
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
 **bundle.id** | **character**|  | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The bundle is successfully unlinked from the project. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateProject**
> Project UpdateProject(project.id, if.match=var.if.match, project=var.project)

Update a project.

Fields which can be updated: - shortDescription - projectInformation - billingMode - dataSharingEnabled - tags - storageBundle - metaDataModel

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.project <- Project$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", "active_example", Region$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "cityName_example", "tenantName_example"), "PROJECT", ProjectTag$new(list("technicalTags_example"), list("userTags_example")), "tenantName_example", "shortDescription_example", "information_example", "dataSharingEnabled_example", StorageBundle$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "bundleName_example", "entitlementName_example", Region$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "cityName_example", "tenantName_example"), "tenantName_example"), StorageConfiguration$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", "AWS_S3", "INITIALIZING", Region$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "cityName_example", "tenantName_example"), "isDefault_example", "tenantName_example", "description_example", "errorMessage_example"), MetadataModel$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", "DRAFT", "tenantName_example", "description_example", "parentModelId_example"), Application$new("id_example", "name_example", "MAIN", "displayName_example")) # Project | 

#Update a project.
api.instance <- ProjectApi$new()
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
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **project** | [**Project**](Project.md)|  | [optional] 

### Return type

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project is successfully update. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

