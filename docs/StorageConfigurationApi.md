# StorageConfigurationApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateStorageConfiguration**](StorageConfigurationApi.md#CreateStorageConfiguration) | **POST** /api/storageConfigurations | Create a new storage configuration
[**GetStorageConfiguration**](StorageConfigurationApi.md#GetStorageConfiguration) | **GET** /api/storageConfigurations/{storageConfigurationId} | Retrieve a storage configuration.
[**GetStorageConfigurationDetails**](StorageConfigurationApi.md#GetStorageConfigurationDetails) | **GET** /api/storageConfigurations/{storageConfigurationId}/details | Retrieve a storage configuration detail.
[**GetStorageConfigurations**](StorageConfigurationApi.md#GetStorageConfigurations) | **GET** /api/storageConfigurations | Retrieve a list of storage configurations.
[**ShareStorageConfiguration**](StorageConfigurationApi.md#ShareStorageConfiguration) | **POST** /api/storageConfigurations/{storageConfigurationId}:share | Share your own storage configuration with tenant.


# **CreateStorageConfiguration**
> StorageConfiguration CreateStorageConfiguration(create.storage.configuration=var.create.storage.configuration)

Create a new storage configuration

### Example
```R
library(icar)

var.create.storage.configuration <- CreateStorageConfiguration$new("name_example", "storageCredentialId_example", "AWS_S3", "regionId_example", "description_example", AWSDetails$new("bucketName_example", "keyPrefix_example", "serverSideEncryptionAlgorithm_example", "serverSideEncryptionKey_example")) # CreateStorageConfiguration | 

#Create a new storage configuration
api.instance <- StorageConfigurationApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create.storage.configuration** | [**CreateStorageConfiguration**](CreateStorageConfiguration.md)|  | [optional] 

### Return type

[**StorageConfiguration**](StorageConfiguration.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The storage configuration is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetStorageConfiguration**
> StorageConfiguration GetStorageConfiguration(storage.configuration.id)

Retrieve a storage configuration.

### Example
```R
library(icar)

var.storage.configuration.id <- 'storage.configuration.id_example' # character | The ID of the storage configuration to retrieve

#Retrieve a storage configuration.
api.instance <- StorageConfigurationApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storage.configuration.id** | **character**| The ID of the storage configuration to retrieve | 

### Return type

[**StorageConfiguration**](StorageConfiguration.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The storage configuration is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetStorageConfigurationDetails**
> StorageConfigurationDetails GetStorageConfigurationDetails(storage.configuration.id)

Retrieve a storage configuration detail.

### Example
```R
library(icar)

var.storage.configuration.id <- 'storage.configuration.id_example' # character | The ID of the storage configuration to retrieve

#Retrieve a storage configuration detail.
api.instance <- StorageConfigurationApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storage.configuration.id** | **character**| The ID of the storage configuration to retrieve | 

### Return type

[**StorageConfigurationDetails**](StorageConfigurationDetails.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The storage configuration detail is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetStorageConfigurations**
> StorageConfigurationWithDetailsList GetStorageConfigurations()

Retrieve a list of storage configurations.

### Example
```R
library(icar)


#Retrieve a list of storage configurations.
api.instance <- StorageConfigurationApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**StorageConfigurationWithDetailsList**](StorageConfigurationWithDetailsList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of storage configurations is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **ShareStorageConfiguration**
> ShareStorageConfiguration(storage.configuration.id)

Share your own storage configuration with tenant.

Here you share your own storage configuration with all the other users in your tenant.

### Example
```R
library(icar)

var.storage.configuration.id <- 'storage.configuration.id_example' # character | The ID of the storage configuration to share

#Share your own storage configuration with tenant.
api.instance <- StorageConfigurationApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storage.configuration.id** | **character**| The ID of the storage configuration to share | 

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
| **204** | The storage configuration is successfully shared. |  -  |
| **0** | A problem occurred. |  -  |

