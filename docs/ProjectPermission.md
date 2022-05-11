# icar::ProjectPermission


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **character** |  | 
**timeCreated** | **character** |  | 
**timeModified** | **character** |  | 
**ownerId** | **character** |  | 
**tenantId** | **character** |  | 
**tenantName** | **character** |  | [optional] 
**roleProject** | **character** |  | 
**roleFlow** | **character** |  | 
**roleBase** | **character** |  | 
**roleBench** | **character** |  | 
**membershipType** | **character** |  | 
**user** | [**User**](User.md) |  | [optional] 
**emailAddress** | **character** | Only present when membershipType is EMAIL | [optional] 
**workgroup** | [**Workgroup**](Workgroup.md) |  | [optional] 
**invitationAccepted** | **character** | Only present when membershipType is EMAIL | [optional] 
**invitationRejected** | **character** | Only present when user is invited by EMAIL | [optional] 
**uploadAllowed** | **character** |  | 
**downloadAllowed** | **character** |  | 


