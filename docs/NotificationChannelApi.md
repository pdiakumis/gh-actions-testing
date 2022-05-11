# NotificationChannelApi

All URIs are relative to */ica/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateNotificationChannel**](NotificationChannelApi.md#CreateNotificationChannel) | **POST** /api/notificationChannels | Create a notification channel
[**DeleteNotificationChannel**](NotificationChannelApi.md#DeleteNotificationChannel) | **DELETE** /api/notificationChannels/{channelId} | Delete a notification channel
[**GetNotificationChannel**](NotificationChannelApi.md#GetNotificationChannel) | **GET** /api/notificationChannels/{channelId} | Retrieve a notification channel
[**GetNotificationChannels**](NotificationChannelApi.md#GetNotificationChannels) | **GET** /api/notificationChannels | Retrieve notification channels
[**UpdateNotificationChannel**](NotificationChannelApi.md#UpdateNotificationChannel) | **PUT** /api/notificationChannels/{channelId} | Update a notification channel


# **CreateNotificationChannel**
> NotificationChannel CreateNotificationChannel(create.notification.channel=var.create.notification.channel)

Create a notification channel

### Example
```R
library(icar)

var.create.notification.channel <- CreateNotificationChannel$new("enabled_example", "MAIL", "address_example") # CreateNotificationChannel | The new channel

#Create a notification channel
api.instance <- NotificationChannelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create.notification.channel** | [**CreateNotificationChannel**](CreateNotificationChannel.md)| The new channel | [optional] 

### Return type

[**NotificationChannel**](NotificationChannel.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The notification channel is successfully created. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **DeleteNotificationChannel**
> DeleteNotificationChannel(channel.id)

Delete a notification channel

### Example
```R
library(icar)

var.channel.id <- 'channel.id_example' # character | The ID of the notification channel to delete

#Delete a notification channel
api.instance <- NotificationChannelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel.id** | **character**| The ID of the notification channel to delete | 

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
| **204** | The notification channel is successfully deleted |  -  |
| **0** | A problem occurred. |  -  |

# **GetNotificationChannel**
> NotificationChannel GetNotificationChannel(channel.id)

Retrieve a notification channel

### Example
```R
library(icar)

var.channel.id <- 'channel.id_example' # character | The ID of the notification channel to retrieve

#Retrieve a notification channel
api.instance <- NotificationChannelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel.id** | **character**| The ID of the notification channel to retrieve | 

### Return type

[**NotificationChannel**](NotificationChannel.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The notification channel is successfully retrieved. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

# **GetNotificationChannels**
> NotificationChannelList GetNotificationChannels()

Retrieve notification channels

### Example
```R
library(icar)


#Retrieve notification channels
api.instance <- NotificationChannelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**NotificationChannelList**](NotificationChannelList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The notification channels are successfully retrieved. |  -  |
| **0** | A problem occurred. |  -  |

# **UpdateNotificationChannel**
> NotificationChannel UpdateNotificationChannel(channel.id, if.match=var.if.match, notification.channel=var.notification.channel)

Update a notification channel

This will affect all subscriptions which use this address!Fields which can be updated:  - enabled  - address 

### Example
```R
library(icar)

var.channel.id <- 'channel.id_example' # character | The ID of the notification channel to update
var.if.match <- 'if.match_example' # character | Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client's most recent value of the 'ETag' response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version.
var.notification.channel <- NotificationChannel$new("id_example", "timeCreated_example", "timeModified_example", "ownerId_example", "tenantId_example", "enabled_example", "MAIL", "address_example", "tenantName_example") # NotificationChannel | The updated channel

#Update a notification channel
api.instance <- NotificationChannelApi$new()
# Configure API key authorization: ApiKeyAuth
api.instance$apiClient$apiKeys['X-API-Key'] <- 'TODO_YOUR_API_KEY';
# Configure HTTP basic authorization: JwtAuth
api.instance$apiClient$username <- 'TODO_YOUR_USERNAME';
api.instance$apiClient$password <- 'TODO_YOUR_PASSWORD';
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel.id** | **character**| The ID of the notification channel to update | 
 **if.match** | **character**| Optional header parameter to enable conflict exposure. If the client provides this header, then it must contains the client&#39;s most recent value of the &#39;ETag&#39; response header, and the server will respond with a 409 code if it detects a conflict. If the client does not provide this header, then the server will not do a conflict check, which means that as a client you can override the resource even when the server has a more recent version. | [optional] 
 **notification.channel** | [**NotificationChannel**](NotificationChannel.md)| The updated channel | [optional] 

### Return type

[**NotificationChannel**](NotificationChannel.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [JwtAuth](../README.md#JwtAuth)

### HTTP request headers

 - **Content-Type**: application/vnd.illumina.v3+json
 - **Accept**: application/problem+json, application/vnd.illumina.v3+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The notification channel is successfully updated. |  * ETag - The current version of the resource. Can be passed to the corresponding PUT endpoint to enable conflict exposure (409 response). <br>  |
| **0** | A problem occurred. |  -  |

