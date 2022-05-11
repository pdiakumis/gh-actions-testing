# BundleToolApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBundleTools**](BundleToolApi.md#GetBundleTools) | **GET** /api/bundles/{bundleId}/tools | Retrieve a list of bundle tools.
[**GetToolsEligibleForLinkingToBundle**](BundleToolApi.md#GetToolsEligibleForLinkingToBundle) | **GET** /api/bundles/{bundleId}/tools/eligibleForLinking | Retrieve a list of tools eligible for linking to the bundle.
[**LinkToolToBundle**](BundleToolApi.md#LinkToolToBundle) | **POST** /api/bundles/{bundleId}/tools/{toolId} | Link a tool to a bundle
[**UnlinkToolFromBundle**](BundleToolApi.md#UnlinkToolFromBundle) | **DELETE** /api/bundles/{bundleId}/tools/{toolId} | Unlink a tool from this bundle.


# **GetBundleTools**
> BundleToolsList GetBundleTools(bundle.id)

Retrieve a list of bundle tools.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle to get tools from

#Retrieve a list of bundle tools.
api.instance <- BundleToolApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle to get tools from | 

### Return type

[**BundleToolsList**](BundleToolsList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of bundle tools is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetToolsEligibleForLinkingToBundle**
> CwlToolDefinitionList GetToolsEligibleForLinkingToBundle(bundle.id)

Retrieve a list of tools eligible for linking to the bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle to get the eligible tools for

#Retrieve a list of tools eligible for linking to the bundle.
api.instance <- BundleToolApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle to get the eligible tools for | 

### Return type

[**CwlToolDefinitionList**](CwlToolDefinitionList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of tools is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **LinkToolToBundle**
> LinkToolToBundle(bundle.id, tool.id)

Link a tool to a bundle

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | The ID of the bundle to link the tool to
var.tool.id <- 'tool.id_example' # character | The ID of the tool to link

#Link a tool to a bundle
api.instance <- BundleToolApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundle.id** | **character**| The ID of the bundle to link the tool to | 
 **tool.id** | **character**| The ID of the tool to link | 

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
| **204** | The tool is successfully linked to the bundle. |  -  |
| **0** | A problem occurred. |  -  |

# **UnlinkToolFromBundle**
> UnlinkToolFromBundle(bundle.id, tool.id)

Unlink a tool from this bundle.

### Example
```R
library(icar)

var.bundle.id <- 'bundle.id_example' # character | 
var.tool.id <- 'tool.id_example' # character | 

#Unlink a tool from this bundle.
api.instance <- BundleToolApi$new()
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
 **tool.id** | **character**|  | 

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
| **204** | The tool is successfully unlinked from this bundle. |  -  |
| **0** | A problem occurred. |  -  |

