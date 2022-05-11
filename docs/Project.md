# icar::Project


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **character** |  | 
**timeCreated** | **character** |  | 
**timeModified** | **character** |  | 
**ownerId** | **character** |  | 
**tenantId** | **character** |  | 
**tenantName** | **character** |  | [optional] 
**name** | **character** |  | 
**active** | **character** | Indicates whether the project is active or hidden. | 
**shortDescription** | **character** |  | [optional] 
**information** | **character** | Information about the project. Note that the value of this field can be arbitrary large. | [optional] 
**region** | [**Region**](Region.md) |  | 
**billingMode** | **character** | The billing mode of the project. It determines who pays for the costs linked to the project. | 
**dataSharingEnabled** | **character** | Indicates whether the Data and Samples created in this Project can be linked to other Projects. | [optional] 
**tags** | [**ProjectTag**](ProjectTag.md) |  | 
**storageBundle** | [**StorageBundle**](StorageBundle.md) |  | [optional] 
**selfManagedStorageConfiguration** | [**StorageConfiguration**](StorageConfiguration.md) |  | [optional] 
**metadataModel** | [**MetadataModel**](MetadataModel.md) |  | [optional] 
**application** | [**Application**](Application.md) |  | [optional] 


