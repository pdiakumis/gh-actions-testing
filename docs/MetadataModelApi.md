# MetadataModelApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetMetadataModel**](MetadataModelApi.md#GetMetadataModel) | **GET** /api/metadataModels/{metadataModelId} | Retrieve a metadata model. Only metadata models that the user has access to can be retrieved.
[**GetMetadataModelFields**](MetadataModelApi.md#GetMetadataModelFields) | **GET** /api/metadataModels/{metadataModelId}/fields | Retrieve the fields of a metadata model. Only metadata models that the user has access to can be retrieved.
[**GetMetadataModels**](MetadataModelApi.md#GetMetadataModels) | **GET** /api/metadataModels | Retrieve the metadata models for the tenant associated to the security context.
[**GetTenantModel**](MetadataModelApi.md#GetTenantModel) | **GET** /api/metadataModels/tenantModel | Retrieve the tenant model for the tenant associated to the security context.


# **GetMetadataModel**
> MetadataModel GetMetadataModel(metadata.model.id)

Retrieve a metadata model. Only metadata models that the user has access to can be retrieved.

### Example
```R
library(icar)

var.metadata.model.id <- 'metadata.model.id_example' # character | 

#Retrieve a metadata model. Only metadata models that the user has access to can be retrieved.
api.instance <- MetadataModelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **metadata.model.id** | **character**|  | 

### Return type

[**MetadataModel**](MetadataModel.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The metadata model is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetMetadataModelFields**
> FieldList GetMetadataModelFields(metadata.model.id)

Retrieve the fields of a metadata model. Only metadata models that the user has access to can be retrieved.

### Example
```R
library(icar)

var.metadata.model.id <- 'metadata.model.id_example' # character | 

#Retrieve the fields of a metadata model. Only metadata models that the user has access to can be retrieved.
api.instance <- MetadataModelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **metadata.model.id** | **character**|  | 

### Return type

[**FieldList**](FieldList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The metadata model fields are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetMetadataModels**
> MetadataModelList GetMetadataModels()

Retrieve the metadata models for the tenant associated to the security context.

Retrieve the metadata models for the tenant associated to the security context. This call returns a list of metadata models for the tenant in a non-hierarchical way. Instead of a model having a list of child models all models except the root model have a parent model identifier. This can be used to reconstruct the hierarchy.

### Example
```R
library(icar)


#Retrieve the metadata models for the tenant associated to the security context.
api.instance <- MetadataModelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**MetadataModelList**](MetadataModelList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The metadata models are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetTenantModel**
> Model GetTenantModel()

Retrieve the tenant model for the tenant associated to the security context.

Retrieve the tenant model for the tenant associated to the security context. The tenant model is a hierarchical structure where the top level tenant holds a list of child models (which in turn can hold child models).

### Example
```R
library(icar)


#Retrieve the tenant model for the tenant associated to the security context.
api.instance <- MetadataModelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Model**](Model.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tenant model is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

