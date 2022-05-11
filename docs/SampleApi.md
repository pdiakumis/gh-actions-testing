# SampleApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetSamples**](SampleApi.md#GetSamples) | **GET** /api/samples | Retrieve a list of samples.


# **GetSamples**
> SamplePagedList GetSamples(region, search=var.search, user.tags=var.user.tags, technical.tags=var.technical.tags, page.offset=var.page.offset, page.token=var.page.token, page.size=var.page.size, sort=var.sort)

Retrieve a list of samples.

### Example
```R
library(icar)

var.region <- 'region_example' # character | The ID of the region to filter on. This parameter is required.
var.search <- 'search_example' # character | To search through multiple fields of data.
var.user.tags <- 'user.tags_example' # character | The user tags to filter on.
var.technical.tags <- 'technical.tags_example' # character | The technical tags to filter on.
var.page.offset <- 'page.offset_example' # character | The amount of rows to skip in the result. Ideally this is a multiple of the size parameter.
var.page.token <- 'page.token_example' # character | The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination.
var.page.size <- 'page.size_example' # character | The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results.
var.sort <- 'sort_example' # character | Which field to order the results by. The default order is ascending, suffix with ' desc' to sort descending (suffix ' asc' also works for ascending). Multiple values should be separated with commas. An example: \"?sort=dateCreated, lastName desc\"  The attributes for which sorting is supported: - timeCreated - timeModified - name - description - metadataValid - status

#Retrieve a list of samples.
api.instance <- SampleApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **region** | **character**| The ID of the region to filter on. This parameter is required. | 
 **search** | **character**| To search through multiple fields of data. | [optional] 
 **user.tags** | **character**| The user tags to filter on. | [optional] 
 **technical.tags** | **character**| The technical tags to filter on. | [optional] 
 **page.offset** | **character**| The amount of rows to skip in the result. Ideally this is a multiple of the size parameter. | [optional] 
 **page.token** | **character**| The cursor to get subsequent results. The value to use is returned in the result when using cursor-based pagination. | [optional] 
 **page.size** | **character**| The amount of rows to return. Use in combination with the offset or cursor parameter to get subsequent results. | [optional] 
 **sort** | **character**| Which field to order the results by. The default order is ascending, suffix with &#39; desc&#39; to sort descending (suffix &#39; asc&#39; also works for ascending). Multiple values should be separated with commas. An example: \&quot;?sort&#x3D;dateCreated, lastName desc\&quot;  The attributes for which sorting is supported: - timeCreated - timeModified - name - description - metadataValid - status | [optional] 

### Return type

[**SamplePagedList**](SamplePagedList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of samples is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

