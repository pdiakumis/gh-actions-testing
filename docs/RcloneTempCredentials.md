# icar::RcloneTempCredentials

In case of providing the credentialsFormat = rclone, this will contain the credentials for uploading or downloading the data in rclone format.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**config** | **map(character)** | The config in key value format. | 
**filePathPrefix** | **character** | The prefix of the file path. | 
**storageType** | **character** | The type of the object storage. | 
**expirationTime** | **character** | The timestamp when the credentials expire. | 
**uploadSessionId** | **character** | The folder upload session id which can be used after upload to complete the upload session. | [optional] 


