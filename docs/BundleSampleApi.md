# BundleSampleApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBundleSamples**](BundleSampleApi.md#GetBundleSamples) | **GET** /api/bundles/{bundleId}/samples | Retrieve a list of bundle samples.
[**LinkSampleToBundle**](BundleSampleApi.md#LinkSampleToBundle) | **POST** /api/bundles/{bundleId}/samples/{sampleId} | Link a sample to a bundle.
[**UnlinkSampleFromBundle**](BundleSampleApi.md#UnlinkSampleFromBundle) | **DELETE** /api/bundles/{bundleId}/samples/{sampleId} | Unlink a sample from a bundle.


# **GetBundleSamples**
> BundleSamplePagedList GetBundleSamples(bundle.id, search=var.search, user.tags=var.user.tags, technical.tags=var.technical.tags, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve a list of bundle samples.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle to get bundle samples from
var.search <- 'search_example' # character | To search through multiple fields of data.
var.user.tags <- 'user.tags_example' # character | The user tags to filter on.
var.technical.tags <- 'technical.tags_example' # character | The technical tags to filter on.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\" The attributes for which sorting is supported: - timeCreated - timeModified - name - description - metadataValid - status

#Retrieve a list of bundle samples.
api.instance <- BundleSampleApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle to get bundle samples from | 
 **search** | **character**| To search through multiple fields of data. | [optional] 
 **user.tags** | **character**| The user tags to filter on. | [optional] 
 **technical.tags** | **character**| The technical tags to filter on. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot; The attributes for which sorting is supported: - timeCreated - timeModified - name - description - metadataValid - status | [optional] 

### Return type

[**BundleSamplePagedList**](BundleSamplePagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of bundle samples are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **LinkSampleToBundle**
> LinkSampleToBundle(bundle.id, sample.id)

Link a sample to a bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | 

#Link a sample to a bundle.
api.instance <- BundleSampleApi$new()
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
 **sample.id** | **character**|  | 

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
| **204** | The sample is successfully linked to the bundle. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkSampleFromBundle**
> UnlinkSampleFromBundle(bundle.id, sample.id)

Unlink a sample from a bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | 
var.sample.id <- 'sample.id_example' # character | 

#Unlink a sample from a bundle.
api.instance <- BundleSampleApi$new()
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
 **sample.id** | **character**|  | 

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
| **204** | The sample is successfully unlinked from the bundle. |  -  |
| **0** | A problem occurred. |  -  |

