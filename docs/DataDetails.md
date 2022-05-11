# icar::DataDetails

The details of this data. This object is optional because it is possible that these details are deleted.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeCreated** | **character** |  | 
**timeModified** | **character** |  | 
**tenantId** | **character** |  | 
**tenantName** | **character** |  | [optional] 
**owningProjectId** | **character** |  | 
**name** | **character** | The name of the file/folder as it was uploaded. | 
**path** | **character** | The user friendly path of the parent of this data. | [optional] 
**fileSizeInBytes** | **integer** | The size of the file in bytes. Folders do not have a size. | [optional] 
**status** | **character** |  | 
**tags** | [**DataTag**](DataTag.md) |  | 
**format** | [**DataFormat**](DataFormat.md) |  | [optional] 
**dataType** | **character** |  | 
**objectETag** | **character** | The file&#39;s ETag, as received from the cloud provider. Not to be confused with the ETag reponse header of this API. | [optional] 
**storedForTheFirstTimeAt** | **character** | Specifies when the data object was stored for the first time | [optional] 
**region** | [**Region**](Region.md) |  | [optional] 
**willBeArchivedAt** | **character** | Specifies when the data object will be archived. | [optional] 
**willBeDeletedAt** | **character** | Specifies when the data object will be deleted. | [optional] 


