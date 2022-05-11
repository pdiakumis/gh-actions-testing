# EventLogApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetEventLogs**](EventLogApi.md#GetEventLogs) | **GET** /api/eventLog | Retrieve a list of event logs.


# **GetEventLogs**
> EventLogList GetEventLogs(code=var.code, code.filter.type=var.code.filter.type, category=var.category, date.from=var.date.from, date.until=var.date.until, rows=250)

Retrieve a list of event logs.

### Example
```R
library(icar)

var.code <- 'code_example' # character | Code
var.code.filter.type <- 'code.filter.type_example' # character | Code filter type
var.category <- 'category_example' # character | Category
var.date.from <- 'date.from_example' # character | Date from
var.date.until <- 'date.until_example' # character | Date until
var.rows <- 250 # integer | Amount of rows to fetch. Maximum 250. Defaults to 250

#Retrieve a list of event logs.
api.instance <- EventLogApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **character**| Code | [optional] 
 **code.filter.type** | Enum [STARTS_WITH, ENDS_WITH, EQUALS] | Code filter type | [optional] 
 **category** | Enum [ERROR, WARN, INFO] | Category | [optional] 
 **date.from** | **character**| Date from | [optional] 
 **date.until** | **character**| Date until | [optional] 
 **rows** | **integer**| Amount of rows to fetch. Maximum 250. Defaults to 250 | [optional] [default to 250]

### Return type

[**EventLogList**](EventLogList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of event logs is successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

