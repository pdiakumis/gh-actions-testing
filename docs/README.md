# R API client for ICA

R API client to interact with Illumina Connected Analytics v2.

## Installation

```R
install.packages("remotes")
remotes::install_github("umccr-illumina/icar")
library(icar)
```

- For local development:

```sh
git clone https://github.com/umccr-illumina/icar
cd icar
R CMD build .
R CMD check icar_0.0.1.tar.gz --no-manual
R CMD INSTALL icar_0.0.1.tar.gz
```

## Documentation for API Endpoints

All URIs are relative to */ica/rest*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AnalysisStorageApi* | [**GetAnalysisStorageOptions**](AnalysisStorageApi.md#GetAnalysisStorageOptions) | **GET** /api/analysisStorages | Retrieve the list of analysis storage options.
*BundleApi* | [**CreateBundle**](BundleApi.md#CreateBundle) | **POST** /api/bundles | Create a new bundle
*BundleApi* | [**GetBundle**](BundleApi.md#GetBundle) | **GET** /api/bundles/{bundleId} | Retrieve a bundle.
*BundleApi* | [**GetBundles**](BundleApi.md#GetBundles) | **GET** /api/bundles | Retrieve a list of bundles.
*BundleApi* | [**ReleaseBundle**](BundleApi.md#ReleaseBundle) | **POST** /api/bundles/{bundleId}:release | release a bundle
*BundleDataApi* | [**GetBundleData**](BundleDataApi.md#GetBundleData) | **GET** /api/bundles/{bundleId}/data | Retrieve the list of bundle data.
*BundleDataApi* | [**LinkDataToBundle**](BundleDataApi.md#LinkDataToBundle) | **POST** /api/bundles/{bundleId}/data/{dataId} | Link data to this bundle.
*BundleDataApi* | [**UnlinkDataFromBundle**](BundleDataApi.md#UnlinkDataFromBundle) | **DELETE** /api/bundles/{bundleId}/data/{dataId} | Unlink data from this bundle.
*BundlePipelineApi* | [**GetBundlePipelines**](BundlePipelineApi.md#GetBundlePipelines) | **GET** /api/bundles/{bundleId}/pipelines | Retrieve a list of bundle pipelines.
*BundlePipelineApi* | [**LinkPipelineToBundle**](BundlePipelineApi.md#LinkPipelineToBundle) | **POST** /api/bundles/{bundleId}/pipelines/{pipelineId} | Link a pipeline to a bundle.
*BundlePipelineApi* | [**UnlinkPipelineFromBundle**](BundlePipelineApi.md#UnlinkPipelineFromBundle) | **DELETE** /api/bundles/{bundleId}/pipelines/{pipelineId} | Unlink a pipeline from a bundle.
*BundleSampleApi* | [**GetBundleSamples**](BundleSampleApi.md#GetBundleSamples) | **GET** /api/bundles/{bundleId}/samples | Retrieve a list of bundle samples.
*BundleSampleApi* | [**LinkSampleToBundle**](BundleSampleApi.md#LinkSampleToBundle) | **POST** /api/bundles/{bundleId}/samples/{sampleId} | Link a sample to a bundle.
*BundleSampleApi* | [**UnlinkSampleFromBundle**](BundleSampleApi.md#UnlinkSampleFromBundle) | **DELETE** /api/bundles/{bundleId}/samples/{sampleId} | Unlink a sample from a bundle.
*BundleToolApi* | [**GetBundleTools**](BundleToolApi.md#GetBundleTools) | **GET** /api/bundles/{bundleId}/tools | Retrieve a list of bundle tools.
*BundleToolApi* | [**GetToolsEligibleForLinkingToBundle**](BundleToolApi.md#GetToolsEligibleForLinkingToBundle) | **GET** /api/bundles/{bundleId}/tools/eligibleForLinking | Retrieve a list of tools eligible for linking to the bundle.
*BundleToolApi* | [**LinkToolToBundle**](BundleToolApi.md#LinkToolToBundle) | **POST** /api/bundles/{bundleId}/tools/{toolId} | Link a tool to a bundle
*BundleToolApi* | [**UnlinkToolFromBundle**](BundleToolApi.md#UnlinkToolFromBundle) | **DELETE** /api/bundles/{bundleId}/tools/{toolId} | Unlink a tool from this bundle.
*ConnectorApi* | [**CancelConnector**](ConnectorApi.md#CancelConnector) | **POST** /api/connectors/{connectorId}:cancel | Cancel a connector.
*ConnectorApi* | [**CreateConnector**](ConnectorApi.md#CreateConnector) | **POST** /api/connectors | Create a connector.
*ConnectorApi* | [**CreateDownloadRule**](ConnectorApi.md#CreateDownloadRule) | **POST** /api/connectors/{connectorId}/downloadRules | Create a download rule.
*ConnectorApi* | [**CreateUploadRule**](ConnectorApi.md#CreateUploadRule) | **POST** /api/connectors/{connectorId}/uploadRules | Create an upload rule.
*ConnectorApi* | [**DeleteDownloadRule**](ConnectorApi.md#DeleteDownloadRule) | **DELETE** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Delete a download rule.
*ConnectorApi* | [**DeleteUploadRule**](ConnectorApi.md#DeleteUploadRule) | **DELETE** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Delete an upload rule.
*ConnectorApi* | [**DisableConnector**](ConnectorApi.md#DisableConnector) | **POST** /api/connectors/{connectorId}:disable | Disable a connector.
*ConnectorApi* | [**EnableConnector**](ConnectorApi.md#EnableConnector) | **POST** /api/connectors/{connectorId}:enable | Enable a connector.
*ConnectorApi* | [**GetConnector**](ConnectorApi.md#GetConnector) | **GET** /api/connectors/{connectorId} | Retrieve a connector.
*ConnectorApi* | [**GetConnectors**](ConnectorApi.md#GetConnectors) | **GET** /api/connectors | Retrieve a list of connectors.
*ConnectorApi* | [**GetDownloadRule**](ConnectorApi.md#GetDownloadRule) | **GET** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Retrieve a download rule.
*ConnectorApi* | [**GetDownloadRules**](ConnectorApi.md#GetDownloadRules) | **GET** /api/connectors/{connectorId}/downloadRules | Retrieve a list of download rules.
*ConnectorApi* | [**GetUploadRule**](ConnectorApi.md#GetUploadRule) | **GET** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Retrieve an upload rule.
*ConnectorApi* | [**GetUploadRules**](ConnectorApi.md#GetUploadRules) | **GET** /api/connectors/{connectorId}/uploadRules | Retrieve a list of upload rules.
*ConnectorApi* | [**UpdateDownloadRule**](ConnectorApi.md#UpdateDownloadRule) | **PUT** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Update a download rule.
*ConnectorApi* | [**UpdateUploadRule**](ConnectorApi.md#UpdateUploadRule) | **PUT** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Update an upload rule.
*DataFormatApi* | [**GetDataFormats**](DataFormatApi.md#GetDataFormats) | **GET** /api/dataFormats | Retrieve a list of data formats.
*EntitledBundleApi* | [**GetEntitledBundle**](EntitledBundleApi.md#GetEntitledBundle) | **GET** /api/entitledbundles/{entitledBundleId} | Retrieve an entitled bundle.
*EntitledBundleApi* | [**GetEntitledBundles**](EntitledBundleApi.md#GetEntitledBundles) | **GET** /api/entitledbundles | Retrieve a list of entitled bundles.
*EntitlementDetailApi* | [**FindAllMatchingActivationCodesForCwl**](EntitlementDetailApi.md#FindAllMatchingActivationCodesForCwl) | **POST** /api/activationCodes:findAllMatchingForCwl | Search all matching activation code details for a Cwl pipeline.
*EntitlementDetailApi* | [**FindAllMatchingActivationCodesForNextflow**](EntitlementDetailApi.md#FindAllMatchingActivationCodesForNextflow) | **POST** /api/activationCodes:findAllMatchingForNextflow | Search all matching activation code details for a Nextflow pipeline.
*EntitlementDetailApi* | [**FindBestMatchingActivationCodeForCwl**](EntitlementDetailApi.md#FindBestMatchingActivationCodeForCwl) | **POST** /api/activationCodes:findBestMatchingForCwl | Search the best matching activation code detail for Cwl pipeline.
*EntitlementDetailApi* | [**FindBestMatchingActivationCodesForNextflow**](EntitlementDetailApi.md#FindBestMatchingActivationCodesForNextflow) | **POST** /api/activationCodes:findBestMatchingForNextflow | Search the best matching activation code details for Nextflow pipeline.
*EventCodeApi* | [**GetEventCodes**](EventCodeApi.md#GetEventCodes) | **GET** /api/eventCodes | Retrieve event codes
*EventLogApi* | [**GetEventLogs**](EventLogApi.md#GetEventLogs) | **GET** /api/eventLog | Retrieve a list of event logs.
*MetadataModelApi* | [**GetMetadataModel**](MetadataModelApi.md#GetMetadataModel) | **GET** /api/metadataModels/{metadataModelId} | Retrieve a metadata model. Only metadata models that the user has access to can be retrieved.
*MetadataModelApi* | [**GetMetadataModelFields**](MetadataModelApi.md#GetMetadataModelFields) | **GET** /api/metadataModels/{metadataModelId}/fields | Retrieve the fields of a metadata model. Only metadata models that the user has access to can be retrieved.
*MetadataModelApi* | [**GetMetadataModels**](MetadataModelApi.md#GetMetadataModels) | **GET** /api/metadataModels | Retrieve the metadata models for the tenant associated to the security context.
*MetadataModelApi* | [**GetTenantModel**](MetadataModelApi.md#GetTenantModel) | **GET** /api/metadataModels/tenantModel | Retrieve the tenant model for the tenant associated to the security context.
*NotificationChannelApi* | [**CreateNotificationChannel**](NotificationChannelApi.md#CreateNotificationChannel) | **POST** /api/notificationChannels | Create a notification channel
*NotificationChannelApi* | [**DeleteNotificationChannel**](NotificationChannelApi.md#DeleteNotificationChannel) | **DELETE** /api/notificationChannels/{channelId} | Delete a notification channel
*NotificationChannelApi* | [**GetNotificationChannel**](NotificationChannelApi.md#GetNotificationChannel) | **GET** /api/notificationChannels/{channelId} | Retrieve a notification channel
*NotificationChannelApi* | [**GetNotificationChannels**](NotificationChannelApi.md#GetNotificationChannels) | **GET** /api/notificationChannels | Retrieve notification channels
*NotificationChannelApi* | [**UpdateNotificationChannel**](NotificationChannelApi.md#UpdateNotificationChannel) | **PUT** /api/notificationChannels/{channelId} | Update a notification channel
*PipelineApi* | [**GetPipeline**](PipelineApi.md#GetPipeline) | **GET** /api/pipelines/{pipelineId} | Retrieve a pipeline.
*PipelineApi* | [**GetPipelineInputParameters**](PipelineApi.md#GetPipelineInputParameters) | **GET** /api/pipelines/{pipelineId}/inputParameters | Retrieve input parameters for a pipeline.
*PipelineApi* | [**GetPipelineReferenceSets**](PipelineApi.md#GetPipelineReferenceSets) | **GET** /api/pipelines/{pipelineId}/referenceSets | Retrieve the reference sets of a pipeline.
*PipelineApi* | [**GetPipelines**](PipelineApi.md#GetPipelines) | **GET** /api/pipelines | Retrieve a list of pipelines.
*ProjectApi* | [**CreateProject**](ProjectApi.md#CreateProject) | **POST** /api/projects | Create a new project.
*ProjectApi* | [**GetProject**](ProjectApi.md#GetProject) | **GET** /api/projects/{projectId} | Retrieve a project.
*ProjectApi* | [**GetProjectBundle**](ProjectApi.md#GetProjectBundle) | **GET** /api/projects/{projectId}/bundles/{bundleId} | Retrieve a project bundle.
*ProjectApi* | [**GetProjectBundles**](ProjectApi.md#GetProjectBundles) | **GET** /api/projects/{projectId}/bundles | Retrieve project bundles.
*ProjectApi* | [**GetProjects**](ProjectApi.md#GetProjects) | **GET** /api/projects | Retrieve a list of projects.
*ProjectApi* | [**LinkProjectBundle**](ProjectApi.md#LinkProjectBundle) | **POST** /api/projects/{projectId}/bundles/{bundleId} | Link a bundle to a project.
*ProjectApi* | [**UnlinkProjectBundle**](ProjectApi.md#UnlinkProjectBundle) | **DELETE** /api/projects/{projectId}/bundles/{bundleId} | Unlink a bundle from a project.
*ProjectApi* | [**UpdateProject**](ProjectApi.md#UpdateProject) | **PUT** /api/projects/{projectId} | Update a project.
*ProjectAnalysisApi* | [**AbortAnalysis**](ProjectAnalysisApi.md#AbortAnalysis) | **POST** /api/projects/{projectId}/analyses/{analysisId}:abort | Abort an analysis.
*ProjectAnalysisApi* | [**CreateCwlAnalysis**](ProjectAnalysisApi.md#CreateCwlAnalysis) | **POST** /api/projects/{projectId}/analysis:cwl | Create and start an analysis for a CWL pipeline.
*ProjectAnalysisApi* | [**CreateNextflowAnalysis**](ProjectAnalysisApi.md#CreateNextflowAnalysis) | **POST** /api/projects/{projectId}/analysis:nextflow | Create and start an analysis for a Nextflow pipeline.
*ProjectAnalysisApi* | [**GetAnalyses**](ProjectAnalysisApi.md#GetAnalyses) | **GET** /api/projects/{projectId}/analyses | Retrieve the list of project analyses.
*ProjectAnalysisApi* | [**GetAnalysis**](ProjectAnalysisApi.md#GetAnalysis) | **GET** /api/projects/{projectId}/analyses/{analysisId} | Retrieve an analysis.
*ProjectAnalysisApi* | [**GetAnalysisConfigurations**](ProjectAnalysisApi.md#GetAnalysisConfigurations) | **GET** /api/projects/{projectId}/analyses/{analysisId}/configurations | Retrieve the configurations of an analysis.
*ProjectAnalysisApi* | [**GetAnalysisInputs**](ProjectAnalysisApi.md#GetAnalysisInputs) | **GET** /api/projects/{projectId}/analyses/{analysisId}/inputs | Retrieve the inputs of an analysis.
*ProjectAnalysisApi* | [**GetAnalysisOutputs**](ProjectAnalysisApi.md#GetAnalysisOutputs) | **GET** /api/projects/{projectId}/analyses/{analysisId}/outputs | Retrieve the outputs of an analysis.
*ProjectAnalysisApi* | [**GetAnalysisSteps**](ProjectAnalysisApi.md#GetAnalysisSteps) | **GET** /api/projects/{projectId}/analyses/{analysisId}/steps | Retrieve the individual steps of an analysis.
*ProjectAnalysisApi* | [**HGetExecutionOutputObject**](ProjectAnalysisApi.md#HGetExecutionOutputObject) | **GET** /api/projects/{projectId}/analyses/{analysisId}/rawOutput | Retrieve the raw output of an analysis.
*ProjectAnalysisApi* | [**UpdateAnalysis**](ProjectAnalysisApi.md#UpdateAnalysis) | **PUT** /api/projects/{projectId}/analyses/{analysisId} | Update an analysis.
*ProjectBaseApi* | [**CreateBaseConnectionDetails**](ProjectBaseApi.md#CreateBaseConnectionDetails) | **POST** /api/projects/{projectId}/base:connectionDetails | Creates the connection details to snowflake instance.
*ProjectBaseJobApi* | [**GetBaseJob**](ProjectBaseJobApi.md#GetBaseJob) | **GET** /api/projects/{projectId}/base/jobs/{baseJobId} | Retrieve a base job.
*ProjectBaseJobApi* | [**GetBaseJobs**](ProjectBaseJobApi.md#GetBaseJobs) | **GET** /api/projects/{projectId}/base/jobs | Retrieve a list of base jobs
*ProjectBaseTableApi* | [**GetBaseTables**](ProjectBaseTableApi.md#GetBaseTables) | **GET** /api/projects/{projectId}/base/tables | Retrieve a liste of base tables.
*ProjectBaseTableApi* | [**LoadData**](ProjectBaseTableApi.md#LoadData) | **POST** /api/projects/{projectId}/base/tables/{tableId}:loadData | Load data in a base table.
*ProjectCustomEventsApi* | [**CreateCustomEvent**](ProjectCustomEventsApi.md#CreateCustomEvent) | **POST** /api/projects/{projectId}/customEvents | Create a new custom event.
*ProjectCustomNotificationSubscriptionsApi* | [**CreateNotificationSubscription**](ProjectCustomNotificationSubscriptionsApi.md#CreateNotificationSubscription) | **POST** /api/projects/{projectId}/customNotificationSubscriptions | Create a custom notification subscription
*ProjectCustomNotificationSubscriptionsApi* | [**DeleteNotificationSubscription**](ProjectCustomNotificationSubscriptionsApi.md#DeleteNotificationSubscription) | **DELETE** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Delete a custom notification subscription
*ProjectCustomNotificationSubscriptionsApi* | [**GetNotificationSubscription**](ProjectCustomNotificationSubscriptionsApi.md#GetNotificationSubscription) | **GET** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Retrieve a notification subscription
*ProjectCustomNotificationSubscriptionsApi* | [**GetNotificationSubscriptions**](ProjectCustomNotificationSubscriptionsApi.md#GetNotificationSubscriptions) | **GET** /api/projects/{projectId}/customNotificationSubscriptions | Retrieve notification subscriptions
*ProjectCustomNotificationSubscriptionsApi* | [**UpdateNotificationSubscription**](ProjectCustomNotificationSubscriptionsApi.md#UpdateNotificationSubscription) | **PUT** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Update a notification subscription
*ProjectDataApi* | [**AddSecondaryData**](ProjectDataApi.md#AddSecondaryData) | **POST** /api/projects/{projectId}/data/{dataId}/secondaryData/{secondaryDataId} | Add secondary data to data.
*ProjectDataApi* | [**ArchiveData**](ProjectDataApi.md#ArchiveData) | **POST** /api/projects/{projectId}/data/{dataId}:archive | Schedule this data for archival.
*ProjectDataApi* | [**CompleteFolderUploadSession**](ProjectDataApi.md#CompleteFolderUploadSession) | **POST** /api/projects/{projectId}/data/{dataId}/folderUploadSessions/{folderUploadSessionId}:complete | Complete a trackable folder upload session.
*ProjectDataApi* | [**CreateDataInProject**](ProjectDataApi.md#CreateDataInProject) | **POST** /api/projects/{projectId}/data | Create data in this project.
*ProjectDataApi* | [**CreateDownloadUrlForData**](ProjectDataApi.md#CreateDownloadUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createDownloadUrl | Retrieve a download URL for this data.
*ProjectDataApi* | [**CreateFolderUploadSession**](ProjectDataApi.md#CreateFolderUploadSession) | **POST** /api/projects/{projectId}/data/{dataId}/folderUploadSessions | Create a trackable folder upload session.
*ProjectDataApi* | [**CreateInlineViewUrlForData**](ProjectDataApi.md#CreateInlineViewUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createInlineViewUrl | Retrieve an URL for this data to use for inline view in a browser.
*ProjectDataApi* | [**CreateTemporaryCredentialsForData**](ProjectDataApi.md#CreateTemporaryCredentialsForData) | **POST** /api/projects/{projectId}/data/{dataId}:createTemporaryCredentials | Retrieve temporary credentials for this data.
*ProjectDataApi* | [**CreateUploadUrlForData**](ProjectDataApi.md#CreateUploadUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createUploadUrl | Retrieve an upload URL for this data.
*ProjectDataApi* | [**DeleteData**](ProjectDataApi.md#DeleteData) | **POST** /api/projects/{projectId}/data/{dataId}:delete | Schedule this data for deletion.
*ProjectDataApi* | [**GetDataEligibleForLinking**](ProjectDataApi.md#GetDataEligibleForLinking) | **GET** /api/projects/{projectId}/data/eligibleForLinking | Retrieve a list of data eligible for linking to the current project.
*ProjectDataApi* | [**GetFolderUploadSession**](ProjectDataApi.md#GetFolderUploadSession) | **GET** /api/projects/{projectId}/data/{dataId}/folderUploadSessions/{folderUploadSessionId} | Retrieve folder upload session details.
*ProjectDataApi* | [**GetNonSampleProjectData**](ProjectDataApi.md#GetNonSampleProjectData) | **GET** /api/projects/{projectId}/data/nonSampleData | Retrieve a list of project data not linked to a sample.
*ProjectDataApi* | [**GetProjectData**](ProjectDataApi.md#GetProjectData) | **GET** /api/projects/{projectId}/data/{dataId} | Retrieve a project data.
*ProjectDataApi* | [**GetProjectDataChildren**](ProjectDataApi.md#GetProjectDataChildren) | **GET** /api/projects/{projectId}/data/{dataId}/children | Retrieve the children of this data.
*ProjectDataApi* | [**GetProjectDataList**](ProjectDataApi.md#GetProjectDataList) | **GET** /api/projects/{projectId}/data | Retrieve the list of project data.
*ProjectDataApi* | [**GetProjectsLinkedToData**](ProjectDataApi.md#GetProjectsLinkedToData) | **GET** /api/projects/{projectId}/data/{dataId}/linkedProjects | Retrieve a list of projects to which this data is linked.
*ProjectDataApi* | [**GetSecondaryData**](ProjectDataApi.md#GetSecondaryData) | **GET** /api/projects/{projectId}/data/{dataId}/secondaryData | Retrieve a list of secondary data for data.
*ProjectDataApi* | [**LinkDataToProject**](ProjectDataApi.md#LinkDataToProject) | **POST** /api/projects/{projectId}/data/{dataId} | Link data to this project.
*ProjectDataApi* | [**RemoveSecondaryData**](ProjectDataApi.md#RemoveSecondaryData) | **DELETE** /api/projects/{projectId}/data/{dataId}/secondaryData/{secondaryDataId} | Remove secondary data from data.
*ProjectDataApi* | [**ScheduleDownloadForData**](ProjectDataApi.md#ScheduleDownloadForData) | **POST** /api/projects/{projectId}/data/{dataId}:scheduleDownload | Schedule a download.
*ProjectDataApi* | [**UnarchiveData**](ProjectDataApi.md#UnarchiveData) | **POST** /api/projects/{projectId}/data/{dataId}:unarchive | Schedule this data for unarchival.
*ProjectDataApi* | [**UnlinkDataFromProject**](ProjectDataApi.md#UnlinkDataFromProject) | **POST** /api/projects/{projectId}/data/{dataId}:unlink | Unlink data from this project.
*ProjectDataApi* | [**UpdateProjectData**](ProjectDataApi.md#UpdateProjectData) | **PUT** /api/projects/{projectId}/data/{dataId} | Update this project data.
*ProjectDataTransferApi* | [**AbortDataTransfer**](ProjectDataTransferApi.md#AbortDataTransfer) | **POST** /api/projects/{projectId}/dataTransfers/{dataTransferId}:abort | Abort a data transfer.
*ProjectDataTransferApi* | [**GetDataTransfer**](ProjectDataTransferApi.md#GetDataTransfer) | **GET** /api/projects/{projectId}/dataTransfers/{dataTransferId} | Retrieve a data transfer.
*ProjectDataTransferApi* | [**GetDataTransfers**](ProjectDataTransferApi.md#GetDataTransfers) | **GET** /api/projects/{projectId}/dataTransfers | Retrieve a list of data transfers.
*ProjectNotificationSubscriptionsApi* | [**CreateNotificationSubscription1**](ProjectNotificationSubscriptionsApi.md#CreateNotificationSubscription1) | **POST** /api/projects/{projectId}/notificationSubscriptions | Create a notification subscription
*ProjectNotificationSubscriptionsApi* | [**DeleteNotificationSubscription1**](ProjectNotificationSubscriptionsApi.md#DeleteNotificationSubscription1) | **DELETE** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Delete a notification subscription
*ProjectNotificationSubscriptionsApi* | [**GetNotificationSubscription1**](ProjectNotificationSubscriptionsApi.md#GetNotificationSubscription1) | **GET** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Retrieve a notification subscription
*ProjectNotificationSubscriptionsApi* | [**GetNotificationSubscriptions1**](ProjectNotificationSubscriptionsApi.md#GetNotificationSubscriptions1) | **GET** /api/projects/{projectId}/notificationSubscriptions | Retrieve notification subscriptions
*ProjectNotificationSubscriptionsApi* | [**UpdateNotificationSubscription1**](ProjectNotificationSubscriptionsApi.md#UpdateNotificationSubscription1) | **PUT** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Update a notification subscription
*ProjectPermissionApi* | [**CreateProjectPermission**](ProjectPermissionApi.md#CreateProjectPermission) | **POST** /api/projects/{projectId}/permissions | Create a project permission.
*ProjectPermissionApi* | [**GetProjectPermission**](ProjectPermissionApi.md#GetProjectPermission) | **GET** /api/projects/{projectId}/permissions/{permissionId} | Retrieve a project permission.
*ProjectPermissionApi* | [**GetProjectPermissions**](ProjectPermissionApi.md#GetProjectPermissions) | **GET** /api/projects/{projectId}/permissions | Retrieve a list of project permissions.
*ProjectPermissionApi* | [**UpdateProjectPermission**](ProjectPermissionApi.md#UpdateProjectPermission) | **PUT** /api/projects/{projectId}/permissions/{permissionId} | Update a project permission.
*ProjectPipelineApi* | [**CreateCwlPipeline**](ProjectPipelineApi.md#CreateCwlPipeline) | **POST** /api/projects/{projectId}/pipelines:createCwlPipeline | Create a CWL pipeline within a project.
*ProjectPipelineApi* | [**CreateNextflowPipeline**](ProjectPipelineApi.md#CreateNextflowPipeline) | **POST** /api/projects/{projectId}/pipelines:createNextflowPipeline | Create a Nextflow pipeline within a project.
*ProjectPipelineApi* | [**GetProjectPipeline**](ProjectPipelineApi.md#GetProjectPipeline) | **GET** /api/projects/{projectId}/pipelines/{pipelineId} | Retrieve a project pipeline.
*ProjectPipelineApi* | [**GetProjectPipelineInputParameters**](ProjectPipelineApi.md#GetProjectPipelineInputParameters) | **GET** /api/projects/{projectId}/pipelines/{pipelineId}/inputParameters | Retrieve input parameters for a project pipeline.
*ProjectPipelineApi* | [**GetProjectPipelineReferenceSets**](ProjectPipelineApi.md#GetProjectPipelineReferenceSets) | **GET** /api/projects/{projectId}/pipelines/{pipelineId}/referenceSets | Retrieve the reference sets of a project pipeline.
*ProjectPipelineApi* | [**GetProjectPipelines**](ProjectPipelineApi.md#GetProjectPipelines) | **GET** /api/projects/{projectId}/pipelines | Retrieve a list of project pipelines.
*ProjectPipelineApi* | [**LinkPipelineToProject**](ProjectPipelineApi.md#LinkPipelineToProject) | **POST** /api/projects/{projectId}/pipelines/{pipelineId} | Link a pipeline to a project.
*ProjectPipelineApi* | [**ReleasePipeline**](ProjectPipelineApi.md#ReleasePipeline) | **POST** /api/projects/{projectId}/pipelines/{pipelineId}:release | Release a pipeline.
*ProjectPipelineApi* | [**UnlinkPipelineFromProject**](ProjectPipelineApi.md#UnlinkPipelineFromProject) | **DELETE** /api/projects/{projectId}/pipelines/{pipelineId} | Unlink a pipeline from a project.
*ProjectSampleApi* | [**AddMetadataModelToSample**](ProjectSampleApi.md#AddMetadataModelToSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/metadata/{metadataModelId} | Add a metadata model to a sample.
*ProjectSampleApi* | [**CompleteProjectSample**](ProjectSampleApi.md#CompleteProjectSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:complete | Completes the sample after data has been linked to it.
*ProjectSampleApi* | [**CreateSampleInProject**](ProjectSampleApi.md#CreateSampleInProject) | **POST** /api/projects/{projectId}/samples | Create a new sample in this project
*ProjectSampleApi* | [**DeepDeleteSample**](ProjectSampleApi.md#DeepDeleteSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteDeep | Delete a sample together with all of its data.
*ProjectSampleApi* | [**DeleteAndUnlinkSample**](ProjectSampleApi.md#DeleteAndUnlinkSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteUnlink | Delete a sample and unlink its data.
*ProjectSampleApi* | [**DeleteSampleWithInput**](ProjectSampleApi.md#DeleteSampleWithInput) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteWithInput | Delete a sample as well as its input data.
*ProjectSampleApi* | [**GetProjectSample**](ProjectSampleApi.md#GetProjectSample) | **GET** /api/projects/{projectId}/samples/{sampleId} | Retrieve a project sample.
*ProjectSampleApi* | [**GetProjectSamples**](ProjectSampleApi.md#GetProjectSamples) | **POST** /api/projects/{projectId}/samples:search | Retrieve project samples.
*ProjectSampleApi* | [**GetProjectsForSample**](ProjectSampleApi.md#GetProjectsForSample) | **GET** /api/projects/{projectId}/samples/{sampleId}/projects | Retrieve a list of projects for this sample.
*ProjectSampleApi* | [**GetSampleDataList**](ProjectSampleApi.md#GetSampleDataList) | **GET** /api/projects/{projectId}/samples/{sampleId}/data | Retrieve the list of sample data.
*ProjectSampleApi* | [**GetSampleHistory**](ProjectSampleApi.md#GetSampleHistory) | **GET** /api/projects/{projectId}/samples/{sampleId}/history | Retrieve sample history.
*ProjectSampleApi* | [**GetSampleMetadataField**](ProjectSampleApi.md#GetSampleMetadataField) | **GET** /api/projects/{projectId}/samples/{sampleId}/metadata/field/{fieldId} | Retrieve a metadata field.
*ProjectSampleApi* | [**GetSampleMetadataFieldCount**](ProjectSampleApi.md#GetSampleMetadataFieldCount) | **GET** /api/projects/{projectId}/samples/{sampleId}/metadata/{fieldId}/fieldCount | Retrieves the number of occurrences of a given field.
*ProjectSampleApi* | [**LinkDataToSample**](ProjectSampleApi.md#LinkDataToSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/data/{dataId} | Link data to a sample.
*ProjectSampleApi* | [**LinkSampleToProject**](ProjectSampleApi.md#LinkSampleToProject) | **POST** /api/projects/{projectId}/samples/{sampleId} | Link a sample to a project.
*ProjectSampleApi* | [**MarkSampleDeleted**](ProjectSampleApi.md#MarkSampleDeleted) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteMark | Mark a sample deleted.
*ProjectSampleApi* | [**UnlinkDataFromSample**](ProjectSampleApi.md#UnlinkDataFromSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/data/{dataId}:unlink | Unlink data from a sample.
*ProjectSampleApi* | [**UnlinkSampleFromProject**](ProjectSampleApi.md#UnlinkSampleFromProject) | **POST** /api/projects/{projectId}/samples/{sampleId}:unlink | Unlink a sample from a project.
*ProjectSampleApi* | [**UpdateProjectSample**](ProjectSampleApi.md#UpdateProjectSample) | **PUT** /api/projects/{projectId}/samples/{sampleId} | Update a project sample.
*ProjectSampleApi* | [**UpdateSampleMetadataFields**](ProjectSampleApi.md#UpdateSampleMetadataFields) | **POST** /api/projects/{projectId}/samples/{sampleId}/metadata:updateFields | Update metadata fields.
*RegionApi* | [**GetRegion**](RegionApi.md#GetRegion) | **GET** /api/regions/{regionId} | Retrieve a region. Only the regions the user has access to through his/her entitlements can be retrieved.
*RegionApi* | [**GetRegions**](RegionApi.md#GetRegions) | **GET** /api/regions | Retrieve a list of regions. Only the regions the user has access to through his/her entitlements are returned.
*SampleApi* | [**GetSamples**](SampleApi.md#GetSamples) | **GET** /api/samples | Retrieve a list of samples.
*StorageBundleApi* | [**GetStorageBundles**](StorageBundleApi.md#GetStorageBundles) | **GET** /api/storageBundles | Retrieve a list of storage bundles.
*StorageConfigurationApi* | [**CreateStorageConfiguration**](StorageConfigurationApi.md#CreateStorageConfiguration) | **POST** /api/storageConfigurations | Create a new storage configuration
*StorageConfigurationApi* | [**GetStorageConfiguration**](StorageConfigurationApi.md#GetStorageConfiguration) | **GET** /api/storageConfigurations/{storageConfigurationId} | Retrieve a storage configuration.
*StorageConfigurationApi* | [**GetStorageConfigurationDetails**](StorageConfigurationApi.md#GetStorageConfigurationDetails) | **GET** /api/storageConfigurations/{storageConfigurationId}/details | Retrieve a storage configuration detail.
*StorageConfigurationApi* | [**GetStorageConfigurations**](StorageConfigurationApi.md#GetStorageConfigurations) | **GET** /api/storageConfigurations | Retrieve a list of storage configurations.
*StorageConfigurationApi* | [**ShareStorageConfiguration**](StorageConfigurationApi.md#ShareStorageConfiguration) | **POST** /api/storageConfigurations/{storageConfigurationId}:share | Share your own storage configuration with tenant.
*StorageCredentialsApi* | [**CreateStorageCredential**](StorageCredentialsApi.md#CreateStorageCredential) | **POST** /api/storageCredentials | Create a new storage credential
*StorageCredentialsApi* | [**GetStorageCredential**](StorageCredentialsApi.md#GetStorageCredential) | **GET** /api/storageCredentials/{storageCredentialId} | Retrieve a storage credential.
*StorageCredentialsApi* | [**GetStorageCredentials**](StorageCredentialsApi.md#GetStorageCredentials) | **GET** /api/storageCredentials | Retrieve a list of storage credentials.
*StorageCredentialsApi* | [**ShareStorageCredential**](StorageCredentialsApi.md#ShareStorageCredential) | **POST** /api/storageCredentials/{storageCredentialId}:share | Share your own storage credentials with tenant.
*StorageCredentialsApi* | [**UpdateStorageCredentialSecrets**](StorageCredentialsApi.md#UpdateStorageCredentialSecrets) | **POST** /api/storageCredentials/{storageCredentialId}:updateSecrets | Update a storage credential's secrets.
*TokenApi* | [**CreateJwtToken**](TokenApi.md#CreateJwtToken) | **POST** /api/tokens | Generate a JWT using an API-key, Basic Authentication or a psToken.
*TokenApi* | [**RefreshJwtToken**](TokenApi.md#RefreshJwtToken) | **POST** /api/tokens:refresh | Refresh a JWT using a not yet expired, still valid JWT.
*UserApi* | [**ApproveUser**](UserApi.md#ApproveUser) | **POST** /api/users/{userId}:approve | Approve a user.
*UserApi* | [**AssignTenantAdminRightsToUser**](UserApi.md#AssignTenantAdminRightsToUser) | **POST** /api/users/{userId}:assignTenantAdministratorRights | Assign tenant administrator rights to a user.
*UserApi* | [**GetUser**](UserApi.md#GetUser) | **GET** /api/users/{userId} | Retrieve a user.
*UserApi* | [**GetUsers**](UserApi.md#GetUsers) | **GET** /api/users | Retrieve a list of users.
*UserApi* | [**RevokeTenantAdminRightsToUser**](UserApi.md#RevokeTenantAdminRightsToUser) | **POST** /api/users/{userId}:revokeTenantAdministratorRights | Revoke tenant administrator rights to a user.
*UserApi* | [**UpdateUser**](UserApi.md#UpdateUser) | **PUT** /api/users/{userId} | Update a user.
*WorkgroupApi* | [**GetWorkgroup**](WorkgroupApi.md#GetWorkgroup) | **GET** /api/workgroups/{workgroupId} | Retrieve a workgroup.
*WorkgroupApi* | [**GetWorkgroups**](WorkgroupApi.md#GetWorkgroups) | **GET** /api/workgroups | Retrieve a list of workgroups.


## Documentation for Models

 - [AWSDetails](AWSDetails.md)
 - [ActivationCodeDetail](ActivationCodeDetail.md)
 - [ActivationCodeDetailList](ActivationCodeDetailList.md)
 - [ActivationCodeDetailUsage](ActivationCodeDetailUsage.md)
 - [Analysis](Analysis.md)
 - [AnalysisData](AnalysisData.md)
 - [AnalysisDataInput](AnalysisDataInput.md)
 - [AnalysisInput](AnalysisInput.md)
 - [AnalysisInputDataMount](AnalysisInputDataMount.md)
 - [AnalysisInputList](AnalysisInputList.md)
 - [AnalysisOutput](AnalysisOutput.md)
 - [AnalysisOutputList](AnalysisOutputList.md)
 - [AnalysisPagedList](AnalysisPagedList.md)
 - [AnalysisParameter](AnalysisParameter.md)
 - [AnalysisRawOutput](AnalysisRawOutput.md)
 - [AnalysisReferenceDataParameter](AnalysisReferenceDataParameter.md)
 - [AnalysisStep](AnalysisStep.md)
 - [AnalysisStepList](AnalysisStepList.md)
 - [AnalysisStorage](AnalysisStorage.md)
 - [AnalysisStorageList](AnalysisStorageList.md)
 - [AnalysisTag](AnalysisTag.md)
 - [Application](Application.md)
 - [AwsCredentials](AwsCredentials.md)
 - [AwsTempCredentials](AwsTempCredentials.md)
 - [BaseConnection](BaseConnection.md)
 - [BaseJob](BaseJob.md)
 - [BaseJobList](BaseJobList.md)
 - [Bundle](Bundle.md)
 - [BundleData](BundleData.md)
 - [BundleDataPagedList](BundleDataPagedList.md)
 - [BundleList](BundleList.md)
 - [BundlePagedList](BundlePagedList.md)
 - [BundlePipeline](BundlePipeline.md)
 - [BundlePipelineList](BundlePipelineList.md)
 - [BundleSample](BundleSample.md)
 - [BundleSamplePagedList](BundleSamplePagedList.md)
 - [BundleTool](BundleTool.md)
 - [BundleToolsList](BundleToolsList.md)
 - [CWLToolDefinition](CWLToolDefinition.md)
 - [CompleteFolderUploadSession](CompleteFolderUploadSession.md)
 - [Connector](Connector.md)
 - [ConnectorList](ConnectorList.md)
 - [Country](Country.md)
 - [CreateBundle](CreateBundle.md)
 - [CreateConnector](CreateConnector.md)
 - [CreateCustomEvent](CreateCustomEvent.md)
 - [CreateCustomNotificationSubscription](CreateCustomNotificationSubscription.md)
 - [CreateCwlAnalysis](CreateCwlAnalysis.md)
 - [CreateData](CreateData.md)
 - [CreateDownloadRule](CreateDownloadRule.md)
 - [CreateNextflowAnalysis](CreateNextflowAnalysis.md)
 - [CreateNotificationChannel](CreateNotificationChannel.md)
 - [CreateNotificationSubscription](CreateNotificationSubscription.md)
 - [CreateProject](CreateProject.md)
 - [CreateProjectPermission](CreateProjectPermission.md)
 - [CreateSample](CreateSample.md)
 - [CreateStorageConfiguration](CreateStorageConfiguration.md)
 - [CreateStorageCredential](CreateStorageCredential.md)
 - [CreateTemporaryCredentials](CreateTemporaryCredentials.md)
 - [CreateUploadRule](CreateUploadRule.md)
 - [CustomNotificationSubscription](CustomNotificationSubscription.md)
 - [CustomNotificationSubscriptionList](CustomNotificationSubscriptionList.md)
 - [CwlAnalysisInput](CwlAnalysisInput.md)
 - [CwlAnalysisJsonInput](CwlAnalysisJsonInput.md)
 - [CwlAnalysisStructuredInput](CwlAnalysisStructuredInput.md)
 - [CwlToolDefinitionList](CwlToolDefinitionList.md)
 - [Data](Data.md)
 - [DataDetails](DataDetails.md)
 - [DataFormat](DataFormat.md)
 - [DataFormatPagedList](DataFormatPagedList.md)
 - [DataList](DataList.md)
 - [DataPagedList](DataPagedList.md)
 - [DataTag](DataTag.md)
 - [DataTransfer](DataTransfer.md)
 - [DataTransfers](DataTransfers.md)
 - [Download](Download.md)
 - [DownloadRule](DownloadRule.md)
 - [DownloadRuleList](DownloadRuleList.md)
 - [EventCode](EventCode.md)
 - [EventCodeList](EventCodeList.md)
 - [EventLog](EventLog.md)
 - [EventLogList](EventLogList.md)
 - [ExecutionConfiguration](ExecutionConfiguration.md)
 - [ExecutionConfigurationList](ExecutionConfigurationList.md)
 - [Field](Field.md)
 - [FieldId](FieldId.md)
 - [FieldList](FieldList.md)
 - [FindProjectSamples](FindProjectSamples.md)
 - [FindSampleBooleanCondition](FindSampleBooleanCondition.md)
 - [FindSampleCondition](FindSampleCondition.md)
 - [FindSampleDateCondition](FindSampleDateCondition.md)
 - [FindSampleNumberCondition](FindSampleNumberCondition.md)
 - [FolderUploadSession](FolderUploadSession.md)
 - [InlineView](InlineView.md)
 - [InputParameter](InputParameter.md)
 - [InputParameterList](InputParameterList.md)
 - [InputPart](InputPart.md)
 - [InputPartMediaType](InputPartMediaType.md)
 - [Link](Link.md)
 - [Links](Links.md)
 - [LoadDataInBaseRequest](LoadDataInBaseRequest.md)
 - [MetadataField](MetadataField.md)
 - [MetadataModel](MetadataModel.md)
 - [MetadataModelList](MetadataModelList.md)
 - [Model](Model.md)
 - [MultipartFormDataInput](MultipartFormDataInput.md)
 - [NextflowAnalysisInput](NextflowAnalysisInput.md)
 - [NotificationChannel](NotificationChannel.md)
 - [NotificationChannelList](NotificationChannelList.md)
 - [NotificationSubscription](NotificationSubscription.md)
 - [NotificationSubscriptionList](NotificationSubscriptionList.md)
 - [Pipeline](Pipeline.md)
 - [PipelineBundle](PipelineBundle.md)
 - [PipelineList](PipelineList.md)
 - [PipelineTag](PipelineTag.md)
 - [Problem](Problem.md)
 - [Project](Project.md)
 - [ProjectBaseTable](ProjectBaseTable.md)
 - [ProjectBaseTableList](ProjectBaseTableList.md)
 - [ProjectBundle](ProjectBundle.md)
 - [ProjectBundleList](ProjectBundleList.md)
 - [ProjectData](ProjectData.md)
 - [ProjectDataPagedList](ProjectDataPagedList.md)
 - [ProjectList](ProjectList.md)
 - [ProjectPagedList](ProjectPagedList.md)
 - [ProjectPermission](ProjectPermission.md)
 - [ProjectPermissionList](ProjectPermissionList.md)
 - [ProjectPipeline](ProjectPipeline.md)
 - [ProjectPipelineList](ProjectPipelineList.md)
 - [ProjectSample](ProjectSample.md)
 - [ProjectSamplePagedList](ProjectSamplePagedList.md)
 - [ProjectTag](ProjectTag.md)
 - [RcloneTempCredentials](RcloneTempCredentials.md)
 - [ReferenceData](ReferenceData.md)
 - [ReferenceDataList](ReferenceDataList.md)
 - [ReferenceSet](ReferenceSet.md)
 - [ReferenceSetList](ReferenceSetList.md)
 - [Region](Region.md)
 - [RegionList](RegionList.md)
 - [Sample](Sample.md)
 - [SampleHistory](SampleHistory.md)
 - [SampleHistoryList](SampleHistoryList.md)
 - [SamplePagedList](SamplePagedList.md)
 - [SampleTag](SampleTag.md)
 - [ScheduleDownload](ScheduleDownload.md)
 - [SearchMatchingActivationCodesForCwlAnalysis](SearchMatchingActivationCodesForCwlAnalysis.md)
 - [SearchMatchingActivationCodesForNextflowAnalysis](SearchMatchingActivationCodesForNextflowAnalysis.md)
 - [Species](Species.md)
 - [StorageBundle](StorageBundle.md)
 - [StorageBundleList](StorageBundleList.md)
 - [StorageConfiguration](StorageConfiguration.md)
 - [StorageConfigurationDetails](StorageConfigurationDetails.md)
 - [StorageConfigurationWithDetails](StorageConfigurationWithDetails.md)
 - [StorageConfigurationWithDetailsList](StorageConfigurationWithDetailsList.md)
 - [StorageCredential](StorageCredential.md)
 - [StorageCredentialList](StorageCredentialList.md)
 - [TempCredentials](TempCredentials.md)
 - [Token](Token.md)
 - [Type](Type.md)
 - [TypeList](TypeList.md)
 - [UpdateMetadata](UpdateMetadata.md)
 - [UpdateMetadataFieldGroup](UpdateMetadataFieldGroup.md)
 - [UpdateSingleMetadataField](UpdateSingleMetadataField.md)
 - [UpdateStorageCredentialSecrets](UpdateStorageCredentialSecrets.md)
 - [Upload](Upload.md)
 - [UploadRule](UploadRule.md)
 - [UploadRuleList](UploadRuleList.md)
 - [User](User.md)
 - [UserList](UserList.md)
 - [Workgroup](Workgroup.md)
 - [WorkgroupList](WorkgroupList.md)


## Documentation for Authorization


### ApiKeyAuth

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header

### BasicAuth

- **Type**: HTTP basic authentication

### JwtAuth

- **Type**: HTTP basic authentication

### PsTokenAuth

- **Type**: HTTP basic authentication



## Author



