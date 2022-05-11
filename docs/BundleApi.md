# BundleApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateBundle**](BundleApi.md#CreateBundle) | **POST** /api/bundles | Create a new bundle
[**GetBundle**](BundleApi.md#GetBundle) | **GET** /api/bundles/{bundleId} | Retrieve a bundle.
[**GetBundles**](BundleApi.md#GetBundles) | **GET** /api/bundles | Retrieve a list of bundles.
[**ReleaseBundle**](BundleApi.md#ReleaseBundle) | **POST** /api/bundles/{bundleId}:release | release a bundle


# **CreateBundle**
> Bundle CreateBundle(create.bundle=var.create.bundle)

Create a new bundle

### Example
```R
library(icar)

var.create.bundle <- CreateBundle$new("name_example", "bundleReleaseVersion_example", "regionId_example", "DRAFT", list("categories_example"), "shortDescription_example", "bundleVersionComment_example", "metadataModelId_example", Links$new(list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example")), list(Link$new("name_example", "url_example")))) # CreateBundle | 

#Create a new bundle
api.instance <- BundleApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create.bundle** | [**CreateBundle**](CreateBundle.md)|  | [optional] 

### Return type

[**Bundle**](Bundle.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The bundle is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetBundle**
> Bundle GetBundle(bundle.id)

Retrieve a bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle to retrieve

#Retrieve a bundle.
api.instance <- BundleApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle to retrieve | 

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
| **200** | The bundle is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetBundles**
> BundlePagedList GetBundles(search=var.search, user.tags=var.user.tags, technical.tags=var.technical.tags, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve a list of bundles.

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

#Retrieve a list of bundles.
api.instance <- BundleApi$new()
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
| **200** | The list of bundles is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **ReleaseBundle**
> ReleaseBundle(bundle.id)

release a bundle

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle to release

#release a bundle
api.instance <- BundleApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle to release | 

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
| **204** | The bundle is successfully released |  -  |
| **0** | A problem occurred. |  -  |

