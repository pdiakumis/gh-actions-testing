# icar::CreateData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **character** | The name of the file/folder as how it will be created. | 
**folderId** | **character** | The id of the folder you want to create this new data in. Alternatively, the folderPath attribute could be used as well for this. | [optional] 
**folderPath** | **character** | The absolute path of the folder you want to create this new data in which must end with &#39;/&#39;. Alternatively, the folderId attribute could be used as well for this. In case the folder path does not yet exist, it will be automatically created. | [optional] 
**formatCode** | **character** | The code of the format you would like to assign at creation time. This is only allowed for file data. If not specified, auto format assignment will be done. | [optional] 
**dataType** | **character** |  | 


