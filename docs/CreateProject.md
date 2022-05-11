# icar::CreateProject


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **character** |  | 
**shortDescription** | **character** |  | [optional] 
**information** | **character** | Information about the project. Note that the value of this field can be arbitrary large. | [optional] 
**projectOwnerId** | **character** | Owner of the project. Defaults to the current user. | [optional] 
**regionId** | **character** | The region of the project. All data and pipeline executions will reside in this region. | 
**billingMode** | **character** | The billing mode of the project. It determines who pays for the costs linked to the project. | 
**dataSharingEnabled** | **character** | Indicates whether the Data and Samples created in this Project can be linked to other Projects. | 
**tags** | [**ProjectTag**](ProjectTag.md) |  | [optional] 
**storageBundleId** | **character** |  | 
**metadataModelId** | **character** |  | [optional] 
**storageConfigurationId** | **character** | An optional storage configuration id to have self managed storage. | [optional] 
**storageConfigurationSubfolder** | **character** | Required when specifying a storageConfigurationId. The subfolder determines the object prefix of your self managed storage. | [optional] 


