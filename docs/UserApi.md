# UserApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ApproveUser**](UserApi.md#ApproveUser) | **POST** /api/users/{userId}:approve | Approve a user.
[**AssignTenantAdminRightsToUser**](UserApi.md#AssignTenantAdminRightsToUser) | **POST** /api/users/{userId}:assignTenantAdministratorRights | Assign tenant administrator rights to a user.
[**GetUser**](UserApi.md#GetUser) | **GET** /api/users/{userId} | Retrieve a user.
[**GetUsers**](UserApi.md#GetUsers) | **GET** /api/users | Retrieve a list of users.
[**RevokeTenantAdminRightsToUser**](UserApi.md#RevokeTenantAdminRightsToUser) | **POST** /api/users/{userId}:revokeTenantAdministratorRights | Revoke tenant administrator rights to a user.
[**UpdateUser**](UserApi.md#UpdateUser) | **PUT** /api/users/{userId} | Update a user.


# **ApproveUser**
> ApproveUser(user.id)

Approve a user.

Endpoint for approving a user.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.user.id <- 'user.id_example' # character | 

#Approve a user.
api.instance <- UserApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user.id** | **character**|  | 

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
| **204** | The user is successfully approved. |  -  |
| **0** | A problem occurred. |  -  |

# **AssignTenantAdminRightsToUser**
> AssignTenantAdminRightsToUser(user.id)

Assign tenant administrator rights to a user.

Endpoint for assigning tenant administrator rights to a user.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.user.id <- 'user.id_example' # character | 

#Assign tenant administrator rights to a user.
api.instance <- UserApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user.id** | **character**|  | 

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
| **204** | The tenant administrator rights are successfully assigned. |  -  |
| **0** | A problem occurred. |  -  |

# **GetUser**
> User GetUser(user.id)

Retrieve a user.

### Example
```R
library(icar)

var.user.id <- 'user.id_example' # character | 

#Retrieve a user.
api.instance <- UserApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user.id** | **character**|  | 

### Return type

[**User**](User.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The user is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetUsers**
> UserList GetUsers()

Retrieve a list of users.

### Example
```R
library(icar)


#Retrieve a list of users.
api.instance <- UserApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**UserList**](UserList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of users is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **RevokeTenantAdminRightsToUser**
> RevokeTenantAdminRightsToUser(user.id)

Revoke tenant administrator rights to a user.

Endpoint for revoking tenant administrator rights to a user.This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.user.id <- 'user.id_example' # character | 

#Revoke tenant administrator rights to a user.
api.instance <- UserApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user.id** | **character**|  | 

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
| **204** | The tenant administrator rights are successfully revoked. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateUser**
> User UpdateUser(user.id, if.match=var.if.match, user=var.user)

Update a user.

Fields which can be updated: - greeting - two factor authentication - job title - first name - last name - mobile phone number - phone number - fax number - address lines - postal code - city - country - state

### Example
```R
library(icar)

var.user.id <- 'user.id_example' # character | 
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.user <- User$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "username_example", "email_example", "active_example", "tenantAdministrator_example", "emailVerified_example", "twoFactorAuthentication_example", "tenantName_example", "firstname_example", "lastname_example", "jobTitle_example", "MR", "mobilePhoneNumber_example", "phoneNumber_example", "faxNumber_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "addressLine1_example", "addressLine2_example", "addressLine3_example", "postalCode_example", "city_example", "state_example") # User | 

#Update a user.
api.instance <- UserApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user.id** | **character**|  | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **user** | [**User**](User.md)|  | [optional] 

### Return type

[**User**](User.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The user is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

