# icar::CwlAnalysisInput

This object contains a \"oneOf\" construct. With the \"objectType\" attribute you can specify which object type you want to provide. Use \"STRUCTURED\" for type \"CreateAnalysisStructuredInput\" or use \"JSON\" for type \"CreateAnalysisJsonInput\".

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**objectType** | **character** |  | 
**inputs** | [**array[AnalysisDataInput]**](AnalysisDataInput.md) |  | 
**parameters** | [**array[AnalysisParameter]**](AnalysisParameter.md) |  | [optional] 
**referenceDataParameters** | [**array[AnalysisReferenceDataParameter]**](AnalysisReferenceDataParameter.md) |  | [optional] 
**inputJson** | **character** | Contains the input JSON, as an escaped JSON String. | 
**dataIds** | **array[character]** |  | [optional] 
**mounts** | [**array[AnalysisInputDataMount]**](AnalysisInputDataMount.md) |  | [optional] 


