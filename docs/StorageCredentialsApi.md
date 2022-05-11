# StorageCredentialsApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateStorageCredential**](StorageCredentialsApi.md#CreateStorageCredential) | **POST** /api/storageCredentials | Create a new storage credential
[**GetStorageCredential**](StorageCredentialsApi.md#GetStorageCredential) | **GET** /api/storageCredentials/{storageCredentialId} | Retrieve a storage credential.
[**GetStorageCredentials**](StorageCredentialsApi.md#GetStorageCredentials) | **GET** /api/storageCredentials | Retrieve a list of storage credentials.
[**ShareStorageCredential**](StorageCredentialsApi.md#ShareStorageCredential) | **POST** /api/storageCredentials/{storageCredentialId}:share | Share your own storage credentials with tenant.
[**UpdateStorageCredentialSecrets**](StorageCredentialsApi.md#UpdateStorageCredentialSecrets) | **POST** /api/storageCredentials/{storageCredentialId}:updateSecrets | Update a storage credential&#39;s secrets.


# **CreateStorageCredential**
> StorageCredential CreateStorageCredential(create.storage.credential=var.create.storage.credential)

Create a new storage credential

### Example
```R
library(icar)

var.create.storage.credential <- CreateStorageCredential$new("name_example", "AWS_USER", AwsCredentials$new("accessKeyId_example", "secretAccessKey_example")) # CreateStorageCredential | 

#Create a new storage credential
api.instance <- StorageCredentialsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create.storage.credential** | [**CreateStorageCredential**](CreateStorageCredential.md)|  | [optional] 

### Return type

[**StorageCredential**](StorageCredential.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The storage credential is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetStorageCredential**
> StorageCredential GetStorageCredential(storage.credential.id)

Retrieve a storage credential.

### Example
```R
library(icar)

var.storage.credential.id <- 'storage.credential.id_example' # character | The ID of the storage credential to retrieve

#Retrieve a storage credential.
api.instance <- StorageCredentialsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storage.credential.id** | **character**| The ID of the storage credential to retrieve | 

### Return type

[**StorageCredential**](StorageCredential.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The storage credential is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetStorageCredentials**
> StorageCredentialList GetStorageCredentials()

Retrieve a list of storage credentials.

### Example
```R
library(icar)


#Retrieve a list of storage credentials.
api.instance <- StorageCredentialsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**StorageCredentialList**](StorageCredentialList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of storage credentials is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **ShareStorageCredential**
> ShareStorageCredential(storage.credential.id)

Share your own storage credentials with tenant.

Here you share your own storage credentials with all the other users in your tenant.

### Example
```R
library(icar)

var.storage.credential.id <- 'storage.credential.id_example' # character | The ID of the storage credential to share

#Share your own storage credentials with tenant.
api.instance <- StorageCredentialsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storage.credential.id** | **character**| The ID of the storage credential to share | 

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
| **204** | The storage credential is successfully shared. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateStorageCredentialSecrets**
> UpdateStorageCredentialSecrets(storage.credential.id, update.storage.credential.secrets=var.update.storage.credential.secrets)

Update a storage credential's secrets.

When your storage credentials change or get updated due to security reasons you need to update them here.

### Example
```R
library(icar)

var.storage.credential.id <- 'storage.credential.id_example' # character | 
var.update.storage.credential.secrets <- UpdateStorageCredentialSecrets$new(AwsCredentials$new("accessKeyId_example", "secretAccessKey_example")) # UpdateStorageCredentialSecrets | 

#Update a storage credential's secrets.
api.instance <- StorageCredentialsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storage.credential.id** | **character**|  | 
 **update.storage.credential.secrets** | [**UpdateStorageCredentialSecrets**](UpdateStorageCredentialSecrets.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | The storage credential secrets are successfully updated. |  -  |
| **0** | A problem occurred. |  -  |

