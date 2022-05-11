# icar::CreateUploadRule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **character** |  | 
**active** | **character** |  | [optional] 
**description** | **character** |  | [optional] 
**localFolder** | **character** | The local folder to monitor. Files in this folder on your local environment will be uploaded to the specified project. Only files matching the filePattern will be uploaded. | 
**filePattern** | **character** | The regular expression to match a file name. eg: to match all files use &#39;.*&#39; | 
**dataFormatId** | **character** | The format which will be assigned to the uploaded data. If not specified, an auto-detection of the format will be done. | [optional] 
**projectId** | **character** | The project to which the data will be uploaded. | 


