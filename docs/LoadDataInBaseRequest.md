# icar::LoadDataInBaseRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allowJaggedRows** | **character** | Enable to accept rows that are missing trailing optional columns. Missing values will be treated as nulls. | [optional] [default to FALSE]
**allowQuotedNewlines** | **character** | Enable to include newlines contained in quoted data sections in the cell’s value. When disabled, newlines will signal a new row | [optional] [default to FALSE]
**dataId** | **character** | ID of the data to load into the table | 
**delimiter** | **character** | field delimiter | [optional] [default to &#39;,&#39;]
**encoding** | **character** | Encoding | [optional] [default to &#39;UTF8&#39;]
**forceLoad** | **character** | When false (default): the data will not be loaded if it was already previously loaded to table ; when true, the data will be loaded even if already loaded in the past | [optional] [default to FALSE]
**headerRowsToSkip** | **integer** | number of rows to skip (usually for headers) | [optional] [default to 1]
**ignoreUnknownValues** | **character** | When enabled, rows with extra column values that do not match the schema will be ignored and will not be loaded into the table | [optional] [default to FALSE]
**includeReferences** | **character** | Include references | [optional] [default to TRUE]
**includeDataReference** | **character** | Include Data Reference | [optional] [default to TRUE]
**includeSampleReference** | **character** | Include Sample Reference | [optional] [default to TRUE]
**includePipelineReference** | **character** | Include Pipeline Reference | [optional] [default to TRUE]
**includePipelineExecutionReference** | **character** | Include Pipeline Execution Reference | [optional] [default to TRUE]
**includeTenantReference** | **character** | Include Tenant Reference | [optional] [default to TRUE]
**nullMarker** | **character** | Specifies a string that represents a null value in a CSV/TSV file. | [optional] 
**numberOfErrorsAllowed** | **integer** | The maximum number of bad records that Base can ignore when running the job | [optional] [default to 0]
**quote** | **character** | The value that is used to quote data sections in a CSV/TSV file | [optional] 
**writePreference** | **character** | specifies how to write data in the table. | [optional] [default to &#39;APPENDTOTABLE&#39;]


