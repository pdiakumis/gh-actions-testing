# EntitledBundleApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetEntitledBundle**](EntitledBundleApi.md#GetEntitledBundle) | **GET** /api/entitledbundles/{entitledBundleId} | Retrieve an entitled bundle.
[**GetEntitledBundles**](EntitledBundleApi.md#GetEntitledBundles) | **GET** /api/entitledbundles | Retrieve a list of entitled bundles.


# **GetEntitledBundle**
> Bundle GetEntitledBundle(entitled.bundle.id)

Retrieve an entitled bundle.

### Example
```R
library(icar)

var.entitled.bundle.id <- 'entitled.bundle.id_example' # character | The ID of the entitled bundle to retrieve

#Retrieve an entitled bundle.
api.instance <- EntitledBundleApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entitled.bundle.id** | **character**| The ID of the entitled bundle to retrieve | 

### Return type

[**Bundle**](Bundle.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The entitled bundle is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetEntitledBundles**
> BundlePagedList GetEntitledBundles(search=var.search, user.tags=var.user.tags, technical.tags=var.technical.tags, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve a list of entitled bundles.

### Example
```R
library(icar)

var.search <- 'search_example' # character | Search
var.user.tags <- 'user.tags_example' # character | User tags to filter on
var.technical.tags <- 'technical.tags_example' # character | Technical tags to filter on
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - name - shortDescription

#Retrieve a list of entitled bundles.
api.instance <- EntitledBundleApi$new()
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
 **user.tags** | **character**| User tags to filter on | [optional] 
 **technical.tags** | **character**| Technical tags to filter on | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - name - shortDescription | [optional] 

### Return type

[**BundlePagedList**](BundlePagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of entitled bundles is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

