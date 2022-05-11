# icar::FindProjectSamples


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conditions** | [**array[FindSampleCondition]**](FindSampleCondition.md) | Adds a condition on a string field. | 
**dateConditions** | [**array[FindSampleDateCondition]**](FindSampleDateCondition.md) | Adds a condition on a date metadate field. If both the dateBefore and dateAfter parameter are null it will return any sample that has no value for the date field. | 
**numberConditions** | [**array[FindSampleNumberCondition]**](FindSampleNumberCondition.md) | Adds a condition on a number metadata field. If both the lowerBoundary and upperBoundary parameter are null it will return any sample that has no value for the number field. | 
**booleanConditions** | [**array[FindSampleBooleanCondition]**](FindSampleBooleanCondition.md) | Adds a condition on a boolean field. | 
**fullTextSearchString** | **character** | Adds a fuzzy matching condition for the text on all string fields of the sample i.e. on both the fixed fields (name, description) as any metadata text field. | [optional] 
**includeDeleted** | **character** | Indicates whether deleted samples should be included. | [optional] [default to FALSE]
**userTags** | **array[character]** | The usertags to filter on. The userTagMatchMode-parameter determines how the filtering is done. | [optional] 
**userTagMatchMode** | **character** | How the usertags are filtered. | [optional] 
**runInputTags** | **array[character]** | The runInputTags to filter on. The runInputTagMatchMode-parameter determines how the filtering is done. | [optional] 
**runInputTagMatchMode** | **character** | How the runInputTags are filtered. | [optional] 
**connectorTags** | **array[character]** | The connectorTags to filter on. The connectorTagMatchMode-parameter determines how the filtering is done. | [optional] 
**connectorTagMatchMode** | **character** | How the connectorTags are filtered. | [optional] 
**techTags** | **array[character]** | The technicalTags to filter on. The techTagMatchMode-parameter determines how the filtering is done. | [optional] 
**techTagMatchMode** | **character** | How the technicalTags are filtered. | [optional] 


