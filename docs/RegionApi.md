# RegionApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetRegion**](RegionApi.md#GetRegion) | **GET** /api/regions/{regionId} | Retrieve a region. Only the regions the user has access to through his/her entitlements can be retrieved.
[**GetRegions**](RegionApi.md#GetRegions) | **GET** /api/regions | Retrieve a list of regions. Only the regions the user has access to through his/her entitlements are returned.


# **GetRegion**
> Region GetRegion(region.id)

Retrieve a region. Only the regions the user has access to through his/her entitlements can be retrieved.

### Example
```R
library(icar)

var.region.id <- 'region.id_example' # character | 

#Retrieve a region. Only the regions the user has access to through his/her entitlements can be retrieved.
api.instance <- RegionApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **region.id** | **character**|  | 

### Return type

[**Region**](Region.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The region is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetRegions**
> RegionList GetRegions()

Retrieve a list of regions. Only the regions the user has access to through his/her entitlements are returned.

### Example
```R
library(icar)


#Retrieve a list of regions. Only the regions the user has access to through his/her entitlements are returned.
api.instance <- RegionApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**RegionList**](RegionList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of regions is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

