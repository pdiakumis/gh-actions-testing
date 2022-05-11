# icar::CreateCwlAnalysis


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userReference** | **character** | The user-reference of the analysis. This should be something meaningful for the user. | 
**pipelineId** | **character** | The pipeline for which an analysis will be created. | 
**tags** | [**AnalysisTag**](AnalysisTag.md) |  | 
**activationCodeDetailId** | **character** | Indicates under which activation code the pipeline is executed. | 
**analysisStorageId** | **character** | The id of the storage to use for the analysis. | [optional] 
**outputParentFolderId** | **character** | The id of the folder in which the output folder should be created. | [optional] 
**analysisInput** | [**CwlAnalysisInput**](CwlAnalysisInput.md) |  | 


