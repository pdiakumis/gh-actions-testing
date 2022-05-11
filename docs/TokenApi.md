# TokenApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateJwtToken**](TokenApi.md#CreateJwtToken) | **POST** /api/tokens | Generate a JWT using an API-key, Basic Authentication or a psToken.
[**RefreshJwtToken**](TokenApi.md#RefreshJwtToken) | **POST** /api/tokens:refresh | Refresh a JWT using a not yet expired, still valid JWT.


# **CreateJwtToken**
> Token CreateJwtToken(tenant=var.tenant)

Generate a JWT using an API-key, Basic Authentication or a psToken.

Generate a JWT using an API-key, Basic Authentication or a psToken. When using Basic Authentication, and you are member of several tenants, also provide the tenant request parameter to indicate for which tenant you want to authenticate. Note that Basic Authentication will not work for SSO (Single Sign On) enabled authentication.

### Example
```R
library(icar)

var.tenant <- 'tenant_example' # character | The name of your tenant in case you have access to multiple tenants.

#Generate a JWT using an API-key, Basic Authentication or a psToken.
api.instance <- TokenApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: BasicAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
# Configure HTTP basic authorization: PsTokenAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tenant** | **character**| The name of your tenant in case you have access to multiple tenants. | [optional] 

### Return type

[**Token**](Token.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [PsTokenAuth](../README.md#PsTokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The JWT is successfully generated. |  -  |
| **0** | A problem occurred. |  -  |

# **RefreshJwtToken**
> Token RefreshJwtToken()

Refresh a JWT using a not yet expired, still valid JWT.

When still having a valid JWT, this endpoint can be used to extend the validity.

### Example
```R
library(icar)


#Refresh a JWT using a not yet expired, still valid JWT.
api.instance <- TokenApi$new()
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Token**](Token.md)

### Authorization

[JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The JWT is successfully refreshed. |  -  |
| **0** | A problem occurred. |  -  |

