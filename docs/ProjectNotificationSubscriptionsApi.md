# ProjectNotificationSubscriptionsApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateNotificationSubscription1**](ProjectNotificationSubscriptionsApi.md#CreateNotificationSubscription1) | **POST** /api/projects/{projectId}/notificationSubscriptions | Create a notification subscription
[**DeleteNotificationSubscription1**](ProjectNotificationSubscriptionsApi.md#DeleteNotificationSubscription1) | **DELETE** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Delete a notification subscription
[**GetNotificationSubscription1**](ProjectNotificationSubscriptionsApi.md#GetNotificationSubscription1) | **GET** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Retrieve a notification subscription
[**GetNotificationSubscriptions1**](ProjectNotificationSubscriptionsApi.md#GetNotificationSubscriptions1) | **GET** /api/projects/{projectId}/notificationSubscriptions | Retrieve notification subscriptions
[**UpdateNotificationSubscription1**](ProjectNotificationSubscriptionsApi.md#UpdateNotificationSubscription1) | **PUT** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Update a notification subscription


# **CreateNotificationSubscription1**
> NotificationSubscription CreateNotificationSubscription1(project.id, create.notification.subscription=var.create.notification.subscription)

Create a notification subscription

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.create.notification.subscription <- CreateNotificationSubscription$new("eventCode_example", "enabled_example", "notificationChannelId_example", "filterExpression_example") # CreateNotificationSubscription | The new subscription

#Create a notification subscription
api.instance <- ProjectNotificationSubscriptionsApi$new()
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
 **create.notification.subscription** | [**CreateNotificationSubscription**](CreateNotificationSubscription.md)| The new subscription | [optional] 

### Return type

[**NotificationSubscription**](NotificationSubscription.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The notification subscription is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **DeleteNotificationSubscription1**
> DeleteNotificationSubscription1(project.id, subscription.id)

Delete a notification subscription

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.subscription.id <- 'subscription.id_example' # character | The ID of the notification subscription to delete

#Delete a notification subscription
api.instance <- ProjectNotificationSubscriptionsApi$new()
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
 **subscription.id** | **character**| The ID of the notification subscription to delete | 

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
| **204** | The notification subscription is successfully deleted |  -  |
| **0** | A problem occurred. |  -  |

# **GetNotificationSubscription1**
> NotificationSubscription GetNotificationSubscription1(project.id, subscription.id)

Retrieve a notification subscription

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.subscription.id <- 'subscription.id_example' # character | The ID of the notification subscription

#Retrieve a notification subscription
api.instance <- ProjectNotificationSubscriptionsApi$new()
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

[**NotificationSubscription**](NotificationSubscription.md)

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

# **GetNotificationSubscriptions1**
> NotificationSubscriptionList GetNotificationSubscriptions1(project.id)

Retrieve notification subscriptions

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project

#Retrieve notification subscriptions
api.instance <- ProjectNotificationSubscriptionsApi$new()
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

[**NotificationSubscriptionList**](NotificationSubscriptionList.md)

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

# **UpdateNotificationSubscription1**
> NotificationSubscription UpdateNotificationSubscription1(project.id, subscription.id, if.match=var.if.match, notification.subscription=var.notification.subscription)

Update a notification subscription

Fields which can be updated:  - enabled  - eventCode  - filterExpression  - notificationChannel 

### Example
```R
library(icar)

var.project.id <- 'project.id_example' # character | The ID of the project
var.subscription.id <- 'subscription.id_example' # character | The ID of the notification subscription to update
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.notification.subscription <- NotificationSubscription$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "eventCode_example", "enabled_example", NotificationChannel$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "enabled_example", "MAIL", "address_example", "tenantName_example"), "tenantName_example", "filterExpression_example") # NotificationSubscription | The updated subscription

#Update a notification subscription
api.instance <- ProjectNotificationSubscriptionsApi$new()
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
 **subscription.id** | **character**| The ID of the notification subscription to update | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **notification.subscription** | [**NotificationSubscription**](NotificationSubscription.md)| The updated subscription | [optional] 

### Return type

[**NotificationSubscription**](NotificationSubscription.md)

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

