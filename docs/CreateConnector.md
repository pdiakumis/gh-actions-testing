# icar::CreateConnector


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **character** |  | 
**active** | **character** |  | 
**countryId** | **character** | ID of the country. If not provided then the country of the tenant will be used. | [optional] 
**addressLine1** | **character** |  | [optional] 
**addressLine2** | **character** |  | [optional] 
**addressLine3** | **character** |  | [optional] 
**postalCode** | **character** |  | [optional] 
**city** | **character** |  | [optional] 
**state** | **character** |  | [optional] 
**description** | **character** | The general description of the connector instance including its purpose. | [optional] 
**mode** | **character** | The mode the connector runs in. | 
**maxBandwidth** | **numeric** | The maximum bandwidth defined in MB per second. | [optional] 
**maxConcurrentTransfers** | **integer** | The maximum amount of concurrent transfers that this connector can execute. | [optional] [default to 2]
**os** | **character** | The target OS of the original connector installer. | 


