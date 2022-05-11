# ProjectPermissionApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateProjectPermission**](ProjectPermissionApi.md#CreateProjectPermission) | **POST** /api/projects/{projectId}/permissions | Create a project permission.
[**GetProjectPermission**](ProjectPermissionApi.md#GetProjectPermission) | **GET** /api/projects/{projectId}/permissions/{permissionId} | Retrieve a project permission.
[**GetProjectPermissions**](ProjectPermissionApi.md#GetProjectPermissions) | **GET** /api/projects/{projectId}/permissions | Retrieve a list of project permissions.
[**UpdateProjectPermission**](ProjectPermissionApi.md#UpdateProjectPermission) | **PUT** /api/projects/{projectId}/permissions/{permissionId} | Update a project permission.


# **CreateProjectPermission**
> ProjectPermission CreateProjectPermission(project.id, create.project.permission=var.create.project.permission)

Create a project permission.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.create.project.permission <- CreateProjectPermission$new("NONE", "NONE", "NONE", "NONE", "USER", "uploadAllowed_example", "downloadAllowed_example", "userId_example", "emailAddress_example", "workgroupId_example") # CreateProjectPermission | 

#Create a project permission.
api.instance <- ProjectPermissionApi$new()
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
 **create.project.permission** | [**CreateProjectPermission**](CreateProjectPermission.md)|  | [optional] 

### Return type

[**ProjectPermission**](ProjectPermission.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The project permission is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetProjectPermission**
> ProjectPermission GetProjectPermission(project.id, permission.id)

Retrieve a project permission.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.permission.id <- 'permission.id_example' # character | 

#Retrieve a project permission.
api.instance <- ProjectPermissionApi$new()
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
 **permission.id** | **character**|  | 

### Return type

[**ProjectPermission**](ProjectPermission.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project permission is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetProjectPermissions**
> ProjectPermissionList GetProjectPermissions(project.id)

Retrieve a list of project permissions.

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 

#Retrieve a list of project permissions.
api.instance <- ProjectPermissionApi$new()
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

[**ProjectPermissionList**](ProjectPermissionList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of project permissions is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateProjectPermission**
> ProjectPermission UpdateProjectPermission(project.id, permission.id, if.match=var.if.match, project.permission=var.project.permission)

Update a project permission.

Fields which can be updated: - uploadAllowed - downloadAllowed - roleProject - roleFlow - roleBase - roleBench

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | 
var.permission.id <- 'permission.id_example' # character | 
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.project.permission <- ProjectPermission$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "NONE", "NONE", "NONE", "NONE", "USER", "uploadAllowed_example", "downloadAllowed_example", "tenantName_example", User$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "username_example", "email_example", "active_example", "tenantAdministrator_example", "emailVerified_example", "twoFactorAuthentication_example", "tenantName_example", "firstname_example", "lastname_example", "jobTitle_example", "MR", "mobilePhoneNumber_example", "phoneNumber_example", "faxNumber_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "addressLine1_example", "addressLine2_example", "addressLine3_example", "postalCode_example", "city_example", "state_example"), "emailAddress_example", Workgroup$new("id_example", "name_example", "description_example"), "invitationAccepted_example", "invitationRejected_example") # ProjectPermission | 

#Update a project permission.
api.instance <- ProjectPermissionApi$new()
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
 **permission.id** | **character**|  | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **project.permission** | [**ProjectPermission**](ProjectPermission.md)|  | [optional] 

### Return type

[**ProjectPermission**](ProjectPermission.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The project permission is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

