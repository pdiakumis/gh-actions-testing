# icar::Connector


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
**active** | **character** |  | 
**connected** | **character** | Indicates if the connector is connected or not. This is cached so even when the connector is no longer connected, for a short time this still may return true. | 
**technicalCode** | **character** | Technical code to be used for processing. | 
**initializationKey** | **character** | The key provided via other channels to initialize the installation. | [optional] 
**country** | [**Country**](Country.md) |  | [optional] 
**addressLine1** | **character** |  | [optional] 
**addressLine2** | **character** |  | [optional] 
**addressLine3** | **character** |  | [optional] 
**postalCode** | **character** |  | [optional] 
**city** | **character** |  | [optional] 
**state** | **character** |  | [optional] 
**description** | **character** | The general description of the connector instance including its purpose. | [optional] 
**mode** | **character** | The mode the connector runs in. | 
**maxBandwidth** | **numeric** | The maximum bandwidth defined in MB per second. | [optional] 
**maxConcurrentTransfers** | **integer** | The maximum amount of concurrent transfers that this connector can execute. | [optional] 
**os** | **character** | The target OS of the original connector installer. | 
**installationStatus** | **character** |  | 
**newConnectorVersionAvailable** | **character** |  | 


