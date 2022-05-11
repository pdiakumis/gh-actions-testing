# ConnectorApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CancelConnector**](ConnectorApi.md#CancelConnector) | **POST** /api/connectors/{connectorId}:cancel | Cancel a connector.
[**CreateConnector**](ConnectorApi.md#CreateConnector) | **POST** /api/connectors | Create a connector.
[**CreateDownloadRule**](ConnectorApi.md#CreateDownloadRule) | **POST** /api/connectors/{connectorId}/downloadRules | Create a download rule.
[**CreateUploadRule**](ConnectorApi.md#CreateUploadRule) | **POST** /api/connectors/{connectorId}/uploadRules | Create an upload rule.
[**DeleteDownloadRule**](ConnectorApi.md#DeleteDownloadRule) | **DELETE** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Delete a download rule.
[**DeleteUploadRule**](ConnectorApi.md#DeleteUploadRule) | **DELETE** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Delete an upload rule.
[**DisableConnector**](ConnectorApi.md#DisableConnector) | **POST** /api/connectors/{connectorId}:disable | Disable a connector.
[**EnableConnector**](ConnectorApi.md#EnableConnector) | **POST** /api/connectors/{connectorId}:enable | Enable a connector.
[**GetConnector**](ConnectorApi.md#GetConnector) | **GET** /api/connectors/{connectorId} | Retrieve a connector.
[**GetConnectors**](ConnectorApi.md#GetConnectors) | **GET** /api/connectors | Retrieve a list of connectors.
[**GetDownloadRule**](ConnectorApi.md#GetDownloadRule) | **GET** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Retrieve a download rule.
[**GetDownloadRules**](ConnectorApi.md#GetDownloadRules) | **GET** /api/connectors/{connectorId}/downloadRules | Retrieve a list of download rules.
[**GetUploadRule**](ConnectorApi.md#GetUploadRule) | **GET** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Retrieve an upload rule.
[**GetUploadRules**](ConnectorApi.md#GetUploadRules) | **GET** /api/connectors/{connectorId}/uploadRules | Retrieve a list of upload rules.
[**UpdateDownloadRule**](ConnectorApi.md#UpdateDownloadRule) | **PUT** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Update a download rule.
[**UpdateUploadRule**](ConnectorApi.md#UpdateUploadRule) | **PUT** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Update an upload rule.


# **CancelConnector**
> CancelConnector(connector.id)

Cancel a connector.

Endpoint for cancelling a connector. This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 

#Cancel a connector.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 

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
| **204** | The connector is successfully cancelled. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateConnector**
> Connector CreateConnector(create.connector=var.create.connector)

Create a connector.

### Example
```R
library(icar)

var.create.connector <- CreateConnector$new("code_example", "active_example", "DOWNLOAD", "WINDOWS", "countryId_example", "addressLine1_example", "addressLine2_example", "addressLine3_example", "postalCode_example", "city_example", "state_example", "description_example", 123, 123) # CreateConnector | The connector to create.

#Create a connector.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create.connector** | [**CreateConnector**](CreateConnector.md)| The connector to create. | [optional] 

### Return type

[**Connector**](Connector.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The connector is successfully created. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateDownloadRule**
> DownloadRule CreateDownloadRule(connector.id, create.download.rule=var.create.download.rule)

Create a download rule.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 
var.create.download.rule <- CreateDownloadRule$new("code_example", 123, "targetLocalFolder_example", "active_example", "description_example", "formatCode_example", "projectName_example", "fileNameExpression_example") # CreateDownloadRule | 

#Create a download rule.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 
 **create.download.rule** | [**CreateDownloadRule**](CreateDownloadRule.md)|  | [optional] 

### Return type

[**DownloadRule**](DownloadRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The download rule is successfully created. |  -  |
| **0** | A problem occurred. |  -  |

# **CreateUploadRule**
> UploadRule CreateUploadRule(connector.id, create.upload.rule=var.create.upload.rule)

Create an upload rule.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 
var.create.upload.rule <- CreateUploadRule$new("code_example", "localFolder_example", "filePattern_example", "projectId_example", "active_example", "description_example", "dataFormatId_example") # CreateUploadRule | 

#Create an upload rule.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 
 **create.upload.rule** | [**CreateUploadRule**](CreateUploadRule.md)|  | [optional] 

### Return type

[**UploadRule**](UploadRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The upload rule is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **DeleteDownloadRule**
> DeleteDownloadRule(connector.id, download.rule.id)

Delete a download rule.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 
var.download.rule.id <- 'download.rule.id_example' # character | 

#Delete a download rule.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 
 **download.rule.id** | **character**|  | 

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
| **204** | The download rule is successfully deleted. |  -  |
| **0** | A problem occurred. |  -  |

# **DeleteUploadRule**
> DeleteUploadRule(connector.id, upload.rule.id)

Delete an upload rule.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 
var.upload.rule.id <- 'upload.rule.id_example' # character | 

#Delete an upload rule.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 
 **upload.rule.id** | **character**|  | 

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
| **204** | The upload rule is successfully deleted. |  -  |
| **0** | A problem occurred. |  -  |

# **DisableConnector**
> DisableConnector(connector.id)

Disable a connector.

Endpoint for disabling a connector. This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 

#Disable a connector.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 

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
| **204** | The connector is successfully disabled. |  -  |
| **0** | A problem occurred. |  -  |

# **EnableConnector**
> EnableConnector(connector.id)

Enable a connector.

Endpoint for enabling a connector. This is a non-RESTful endpoint, as the path of this endpoint is not representing a REST resource.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 

#Enable a connector.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 

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
| **204** | The connector is successfully enabled. |  -  |
| **0** | A problem occurred. |  -  |

# **GetConnector**
> Connector GetConnector(connector.id)

Retrieve a connector.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 

#Retrieve a connector.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 

### Return type

[**Connector**](Connector.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The connector is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetConnectors**
> ConnectorList GetConnectors(active.only=var.active.only)

Retrieve a list of connectors.

### Example
```R
library(icar)

var.active.only <- 'active.only_example' # character | When true only the active connectors will be returned. When false (default value) all connectors wil be returned.

#Retrieve a list of connectors.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **active.only** | **character**| When true only the active connectors will be returned. When false (default value) all connectors wil be returned. | [optional] 

### Return type

[**ConnectorList**](ConnectorList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of connectors is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetDownloadRule**
> DownloadRule GetDownloadRule(connector.id, download.rule.id)

Retrieve a download rule.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 
var.download.rule.id <- 'download.rule.id_example' # character | 

#Retrieve a download rule.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 
 **download.rule.id** | **character**|  | 

### Return type

[**DownloadRule**](DownloadRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The download rule is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetDownloadRules**
> DownloadRuleList GetDownloadRules(connector.id)

Retrieve a list of download rules.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 

#Retrieve a list of download rules.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 

### Return type

[**DownloadRuleList**](DownloadRuleList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The download rules are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **GetUploadRule**
> UploadRule GetUploadRule(connector.id, upload.rule.id)

Retrieve an upload rule.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 
var.upload.rule.id <- 'upload.rule.id_example' # character | 

#Retrieve an upload rule.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 
 **upload.rule.id** | **character**|  | 

### Return type

[**UploadRule**](UploadRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The upload rule is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetUploadRules**
> UploadRuleList GetUploadRules(connector.id)

Retrieve a list of upload rules.

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 

#Retrieve a list of upload rules.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 

### Return type

[**UploadRuleList**](UploadRuleList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The upload rules are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateDownloadRule**
> DownloadRule UpdateDownloadRule(connector.id, download.rule.id, if.match=var.if.match, download.rule=var.download.rule)

Update a download rule.

Fields which can be updated:  - code  - active  - description  - sequence  - formatCode  - projectName  - targetLocalFolder  - protocol  - fileNameExpression  - disableHashing

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 
var.download.rule.id <- 'download.rule.id_example' # character | 
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.download.rule <- DownloadRule$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", 123, "targetLocalFolder_example", "tenantName_example", "active_example", "description_example", "formatCode_example", "projectName_example", "fileNameExpression_example") # DownloadRule | 

#Update a download rule.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 
 **download.rule.id** | **character**|  | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **download.rule** | [**DownloadRule**](DownloadRule.md)|  | [optional] 

### Return type

[**DownloadRule**](DownloadRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The download rule is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **UpdateUploadRule**
> UploadRule UpdateUploadRule(connector.id, upload.rule.id, if.match=var.if.match, upload.rule=var.upload.rule)

Update an upload rule.

Fields which can be updated:  - code  - active  - description  - localFolder  - filePattern  - dataFormat 

### Example
```R
library(icar)

var.connector.id <- 'connector.id_example' # character | 
var.upload.rule.id <- 'upload.rule.id_example' # character | 
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.upload.rule <- UploadRule$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "localFolder_example", "filePattern_example", Project$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", "active_example", Region$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "cityName_example", "tenantName_example"), "PROJECT", ProjectTag$new(list("technicalTags_example"), list("userTags_example")), "tenantName_example", "shortDescription_example", "information_example", "dataSharingEnabled_example", StorageBundle$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "bundleName_example", "entitlementName_example", Region$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "cityName_example", "tenantName_example"), "tenantName_example"), StorageConfiguration$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", "AWS_S3", "INITIALIZING", Region$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", Country$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "name_example", "region_example", "tenantName_example"), "cityName_example", "tenantName_example"), "isDefault_example", "tenantName_example", "description_example", "errorMessage_example"), MetadataModel$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "name_example", "DRAFT", "tenantName_example", "description_example", "parentModelId_example"), Application$new("id_example", "name_example", "MAIN", "displayName_example")), "tenantName_example", "active_example", "description_example", DataFormat$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "code_example", "tenantName_example", "description_example", "mimeType_example")) # UploadRule | 

#Update an upload rule.
api.instance <- ConnectorApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connector.id** | **character**|  | 
 **upload.rule.id** | **character**|  | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **upload.rule** | [**UploadRule**](UploadRule.md)|  | [optional] 

### Return type

[**UploadRule**](UploadRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The upload rule is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

