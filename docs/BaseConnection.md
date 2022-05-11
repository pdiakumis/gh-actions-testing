# icar::BaseConnection


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authenticator** | **character** | Specifies the supported snowflake authenticator to use. Currently &#39;oauth&#39; only is supported | 
**accessToken** | **character** | Specifies the OAuth token to use for authentication | 
**dnsName** | **character** | snowflake dns name. Usually something like &#39;&lt;&lt;account&gt;&gt;.snowflakecomputing.com&#39; | 
**userPrincipalName** | **character** | Specifies the user principal name. This is required for some snowflake client (snowSQL for instance) | 
**databaseName** | **character** | Specifies the database name bound to the project specified | 
**schemaName** | **character** | Specifies the schema name bound to the project specified | 
**warehouseName** | **character** | Specifies the warehouse name bound to the project specified | 
**roleName** | **character** | Specifies the role name bound to the project specified | 


