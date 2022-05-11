# ProjectCustomNotificationSubscriptionsApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateNotificationSubscription**](ProjectCustomNotificationSubscriptionsApi.md#CreateNotificationSubscription) | **POST** /api/projects/{projectId}/customNotificationSubscriptions | Create a custom notification subscription
[**DeleteNotificationSubscription**](ProjectCustomNotificationSubscriptionsApi.md#DeleteNotificationSubscription) | **DELETE** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Delete a custom notification subscription
[**GetNotificationSubscription**](ProjectCustomNotificationSubscriptionsApi.md#GetNotificationSubscription) | **GET** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Retrieve a notification subscription
[**GetNotificationSubscriptions**](ProjectCustomNotificationSubscriptionsApi.md#GetNotificationSubscriptions) | **GET** /api/projects/{projectId}/customNotificationSubscriptions | Retrieve notification subscriptions
[**UpdateNotificationSubscription**](ProjectCustomNotificationSubscriptionsApi.md#UpdateNotificationSubscription) | **PUT** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Update a notification subscription


# **CreateNotificationSubscription**
> CustomNotificationSubscription CreateNotificationSubscription(project.id, create.custom.notification.subscription=var.create.custom.notification.subscription)

Create a custom notification subscription

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.create.custom.notification.subscription <- CreateCustomNotificationSubscription$new("customEventCode_example", "enabled_example", "notificationChannelId_example", "filterExpression_example") # CreateCustomNotificationSubscription | The new subscription

#Create a custom notification subscription
api.instance <- ProjectCustomNotificationSubscriptionsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project.id** | **character**| The ID of the project | 
 **create.custom.notification.subscription** | [**CreateCustomNotificationSubscription**](CreateCustomNotificationSubscription.md)| The new subscription | [optional] 

### Return type

[**CustomNotificationSubscription**](CustomNotificationSubscription.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The custom notification subscription is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **DeleteNotificationSubscription**
> DeleteNotificationSubscription(project.id, subscription.id)

Delete a custom notification subscription

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.subscription.id <- 'subscription.id_example' # character | The ID of the custom notification subscription to delete

#Delete a custom notification subscription
api.instance <- ProjectCustomNotificationSubscriptionsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project.id** | **character**| The ID of the project | 
 **subscription.id** | **character**| The ID of the custom notification subscription to delete | 

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
| **204** | The custom notification subscription is successfully deleted |  -  |
| **0** | A problem occurred. |  -  |

# **GetNotificationSubscription**
> CustomNotificationSubscription GetNotificationSubscription(project.id, subscription.id)

Retrieve a notification subscription

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.subscription.id <- 'subscription.id_example' # character | The ID of the notification subscription

#Retrieve a notification subscription
api.instance <- ProjectCustomNotificationSubscriptionsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project.id** | **character**| The ID of the project | 
 **subscription.id** | **character**| The ID of the notification subscription | 

### Return type

[**CustomNotificationSubscription**](CustomNotificationSubscription.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The notification subscription is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetNotificationSubscriptions**
> CustomNotificationSubscriptionList GetNotificationSubscriptions(project.id)

Retrieve notification subscriptions

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project

#Retrieve notification subscriptions
api.instance <- ProjectCustomNotificationSubscriptionsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project.id** | **character**| The ID of the project | 

### Return type

[**CustomNotificationSubscriptionList**](CustomNotificationSubscriptionList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The notification subscriptions are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateNotificationSubscription**
> CustomNotificationSubscription UpdateNotificationSubscription(project.id, subscription.id, if.match=var.if.match, custom.notification.subscription=var.custom.notification.subscription)

Update a notification subscription

Fields which can be updated:  - enabled  - eventCode  - filterExpression  - notificationChannel 

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.subscription.id <- 'subscription.id_example' # character | The ID of the custom notification subscription to update
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.custom.notification.subscription <- CustomNotificationSubscription$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "customEventCode_example", "enabled_example", NotificationChannel$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "enabled_example", "MAIL", "address_example", "tenantName_example"), "tenantName_example", "filterExpression_example") # CustomNotificationSubscription | The updated subscription

#Update a notification subscription
api.instance <- ProjectCustomNotificationSubscriptionsApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project.id** | **character**| The ID of the project | 
 **subscription.id** | **character**| The ID of the custom notification subscription to update | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **custom.notification.subscription** | [**CustomNotificationSubscription**](CustomNotificationSubscription.md)| The updated subscription | [optional] 

### Return type

[**CustomNotificationSubscription**](CustomNotificationSubscription.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The notification subscription is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

