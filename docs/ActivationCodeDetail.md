# icar::ActivationCodeDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **character** |  | 
**allowedSlots** | **integer** | The allowed slot within this code, empty means unlimited | [optional] 
**usedSlots** | **integer** | Indicates how many slots can are used. | [optional] 
**movedSlots** | **integer** | The slots that where moved to another activation code | [optional] 
**originalSlots** | **integer** | The assigned allowed slot within this code, empty means unlimited | [optional] 
**pipelineBundle** | [**PipelineBundle**](PipelineBundle.md) |  | 
**usages** | [**array[ActivationCodeDetailUsage]**](ActivationCodeDetailUsage.md) |  | 


