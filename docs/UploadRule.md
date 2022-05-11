# icar::UploadRule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **character** |  | 
**timeCreated** | **character** |  | 
**timeModified** | **character** |  | 
**ownerId** | **character** |  | 
**tenantId** | **character** |  | 
**tenantName** | **character** |  | [optional] 
**code** | **character** |  | 
**active** | **character** |  | [optional] 
**description** | **character** |  | [optional] 
**localFolder** | **character** | The local folder to monitor. Files in this folder on your local environment will be uploaded to the specified project. Only files matching the filePattern will be uploaded. | 
**filePattern** | **character** | The regular expression to match a file name. eg: to match all files use &#39;.*&#39; | 
**dataFormat** | [**DataFormat**](DataFormat.md) |  | [optional] 
**project** | [**Project**](Project.md) |  | 


