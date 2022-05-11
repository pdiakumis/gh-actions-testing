# icar::CreateProjectPermission


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**roleProject** | **character** |  | 
**roleFlow** | **character** |  | 
**roleBase** | **character** |  | 
**roleBench** | **character** |  | 
**membershipType** | **character** | How users are invited to the project | 
**userId** | **character** | the id of the user that should be given access, required when membershipType is USER | [optional] 
**emailAddress** | **character** | The email to invite a user on, required when membershipType is EMAIL | [optional] 
**workgroupId** | **character** | the id of the workgroup to give access, required when membershipType is WORKGROUP | [optional] 
**uploadAllowed** | **character** | Indicates if uploading data is allowed or not. | 
**downloadAllowed** | **character** | Indicates if downloading data is allowed or not. | 


