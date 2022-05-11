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
*AnalysisStorageApi* | [**GetAnalysisStorageOptions**](docs/AnalysisStorageApi.md#GetAnalysisStorageOptions) | **GET** /api/analysisStorages | Retrieve the list of analysis storage options.
*BundleApi* | [**CreateBundle**](docs/BundleApi.md#CreateBundle) | **POST** /api/bundles | Create a new bundle
*BundleApi* | [**GetBundle**](docs/BundleApi.md#GetBundle) | **GET** /api/bundles/{bundleId} | Retrieve a bundle.
*BundleApi* | [**GetBundles**](docs/BundleApi.md#GetBundles) | **GET** /api/bundles | Retrieve a list of bundles.
*BundleApi* | [**ReleaseBundle**](docs/BundleApi.md#ReleaseBundle) | **POST** /api/bundles/{bundleId}:release | release a bundle
*BundleDataApi* | [**GetBundleData**](docs/BundleDataApi.md#GetBundleData) | **GET** /api/bundles/{bundleId}/data | Retrieve the list of bundle data.
*BundleDataApi* | [**LinkDataToBundle**](docs/BundleDataApi.md#LinkDataToBundle) | **POST** /api/bundles/{bundleId}/data/{dataId} | Link data to this bundle.
*BundleDataApi* | [**UnlinkDataFromBundle**](docs/BundleDataApi.md#UnlinkDataFromBundle) | **DELETE** /api/bundles/{bundleId}/data/{dataId} | Unlink data from this bundle.
*BundlePipelineApi* | [**GetBundlePipelines**](docs/BundlePipelineApi.md#GetBundlePipelines) | **GET** /api/bundles/{bundleId}/pipelines | Retrieve a list of bundle pipelines.
*BundlePipelineApi* | [**LinkPipelineToBundle**](docs/BundlePipelineApi.md#LinkPipelineToBundle) | **POST** /api/bundles/{bundleId}/pipelines/{pipelineId} | Link a pipeline to a bundle.
*BundlePipelineApi* | [**UnlinkPipelineFromBundle**](docs/BundlePipelineApi.md#UnlinkPipelineFromBundle) | **DELETE** /api/bundles/{bundleId}/pipelines/{pipelineId} | Unlink a pipeline from a bundle.
*BundleSampleApi* | [**GetBundleSamples**](docs/BundleSampleApi.md#GetBundleSamples) | **GET** /api/bundles/{bundleId}/samples | Retrieve a list of bundle samples.
*BundleSampleApi* | [**LinkSampleToBundle**](docs/BundleSampleApi.md#LinkSampleToBundle) | **POST** /api/bundles/{bundleId}/samples/{sampleId} | Link a sample to a bundle.
*BundleSampleApi* | [**UnlinkSampleFromBundle**](docs/BundleSampleApi.md#UnlinkSampleFromBundle) | **DELETE** /api/bundles/{bundleId}/samples/{sampleId} | Unlink a sample from a bundle.
*BundleToolApi* | [**GetBundleTools**](docs/BundleToolApi.md#GetBundleTools) | **GET** /api/bundles/{bundleId}/tools | Retrieve a list of bundle tools.
*BundleToolApi* | [**GetToolsEligibleForLinkingToBundle**](docs/BundleToolApi.md#GetToolsEligibleForLinkingToBundle) | **GET** /api/bundles/{bundleId}/tools/eligibleForLinking | Retrieve a list of tools eligible for linking to the bundle.
*BundleToolApi* | [**LinkToolToBundle**](docs/BundleToolApi.md#LinkToolToBundle) | **POST** /api/bundles/{bundleId}/tools/{toolId} | Link a tool to a bundle
*BundleToolApi* | [**UnlinkToolFromBundle**](docs/BundleToolApi.md#UnlinkToolFromBundle) | **DELETE** /api/bundles/{bundleId}/tools/{toolId} | Unlink a tool from this bundle.
*ConnectorApi* | [**CancelConnector**](docs/ConnectorApi.md#CancelConnector) | **POST** /api/connectors/{connectorId}:cancel | Cancel a connector.
*ConnectorApi* | [**CreateConnector**](docs/ConnectorApi.md#CreateConnector) | **POST** /api/connectors | Create a connector.
*ConnectorApi* | [**CreateDownloadRule**](docs/ConnectorApi.md#CreateDownloadRule) | **POST** /api/connectors/{connectorId}/downloadRules | Create a download rule.
*ConnectorApi* | [**CreateUploadRule**](docs/ConnectorApi.md#CreateUploadRule) | **POST** /api/connectors/{connectorId}/uploadRules | Create an upload rule.
*ConnectorApi* | [**DeleteDownloadRule**](docs/ConnectorApi.md#DeleteDownloadRule) | **DELETE** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Delete a download rule.
*ConnectorApi* | [**DeleteUploadRule**](docs/ConnectorApi.md#DeleteUploadRule) | **DELETE** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Delete an upload rule.
*ConnectorApi* | [**DisableConnector**](docs/ConnectorApi.md#DisableConnector) | **POST** /api/connectors/{connectorId}:disable | Disable a connector.
*ConnectorApi* | [**EnableConnector**](docs/ConnectorApi.md#EnableConnector) | **POST** /api/connectors/{connectorId}:enable | Enable a connector.
*ConnectorApi* | [**GetConnector**](docs/ConnectorApi.md#GetConnector) | **GET** /api/connectors/{connectorId} | Retrieve a connector.
*ConnectorApi* | [**GetConnectors**](docs/ConnectorApi.md#GetConnectors) | **GET** /api/connectors | Retrieve a list of connectors.
*ConnectorApi* | [**GetDownloadRule**](docs/ConnectorApi.md#GetDownloadRule) | **GET** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Retrieve a download rule.
*ConnectorApi* | [**GetDownloadRules**](docs/ConnectorApi.md#GetDownloadRules) | **GET** /api/connectors/{connectorId}/downloadRules | Retrieve a list of download rules.
*ConnectorApi* | [**GetUploadRule**](docs/ConnectorApi.md#GetUploadRule) | **GET** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Retrieve an upload rule.
*ConnectorApi* | [**GetUploadRules**](docs/ConnectorApi.md#GetUploadRules) | **GET** /api/connectors/{connectorId}/uploadRules | Retrieve a list of upload rules.
*ConnectorApi* | [**UpdateDownloadRule**](docs/ConnectorApi.md#UpdateDownloadRule) | **PUT** /api/connectors/{connectorId}/downloadRules/{downloadRuleId} | Update a download rule.
*ConnectorApi* | [**UpdateUploadRule**](docs/ConnectorApi.md#UpdateUploadRule) | **PUT** /api/connectors/{connectorId}/uploadRules/{uploadRuleId} | Update an upload rule.
*DataFormatApi* | [**GetDataFormats**](docs/DataFormatApi.md#GetDataFormats) | **GET** /api/dataFormats | Retrieve a list of data formats.
*EntitledBundleApi* | [**GetEntitledBundle**](docs/EntitledBundleApi.md#GetEntitledBundle) | **GET** /api/entitledbundles/{entitledBundleId} | Retrieve an entitled bundle.
*EntitledBundleApi* | [**GetEntitledBundles**](docs/EntitledBundleApi.md#GetEntitledBundles) | **GET** /api/entitledbundles | Retrieve a list of entitled bundles.
*EntitlementDetailApi* | [**FindAllMatchingActivationCodesForCwl**](docs/EntitlementDetailApi.md#FindAllMatchingActivationCodesForCwl) | **POST** /api/activationCodes:findAllMatchingForCwl | Search all matching activation code details for a Cwl pipeline.
*EntitlementDetailApi* | [**FindAllMatchingActivationCodesForNextflow**](docs/EntitlementDetailApi.md#FindAllMatchingActivationCodesForNextflow) | **POST** /api/activationCodes:findAllMatchingForNextflow | Search all matching activation code details for a Nextflow pipeline.
*EntitlementDetailApi* | [**FindBestMatchingActivationCodeForCwl**](docs/EntitlementDetailApi.md#FindBestMatchingActivationCodeForCwl) | **POST** /api/activationCodes:findBestMatchingForCwl | Search the best matching activation code detail for Cwl pipeline.
*EntitlementDetailApi* | [**FindBestMatchingActivationCodesForNextflow**](docs/EntitlementDetailApi.md#FindBestMatchingActivationCodesForNextflow) | **POST** /api/activationCodes:findBestMatchingForNextflow | Search the best matching activation code details for Nextflow pipeline.
*EventCodeApi* | [**GetEventCodes**](docs/EventCodeApi.md#GetEventCodes) | **GET** /api/eventCodes | Retrieve event codes
*EventLogApi* | [**GetEventLogs**](docs/EventLogApi.md#GetEventLogs) | **GET** /api/eventLog | Retrieve a list of event logs.
*MetadataModelApi* | [**GetMetadataModel**](docs/MetadataModelApi.md#GetMetadataModel) | **GET** /api/metadataModels/{metadataModelId} | Retrieve a metadata model. Only metadata models that the user has access to can be retrieved.
*MetadataModelApi* | [**GetMetadataModelFields**](docs/MetadataModelApi.md#GetMetadataModelFields) | **GET** /api/metadataModels/{metadataModelId}/fields | Retrieve the fields of a metadata model. Only metadata models that the user has access to can be retrieved.
*MetadataModelApi* | [**GetMetadataModels**](docs/MetadataModelApi.md#GetMetadataModels) | **GET** /api/metadataModels | Retrieve the metadata models for the tenant associated to the security context.
*MetadataModelApi* | [**GetTenantModel**](docs/MetadataModelApi.md#GetTenantModel) | **GET** /api/metadataModels/tenantModel | Retrieve the tenant model for the tenant associated to the security context.
*NotificationChannelApi* | [**CreateNotificationChannel**](docs/NotificationChannelApi.md#CreateNotificationChannel) | **POST** /api/notificationChannels | Create a notification channel
*NotificationChannelApi* | [**DeleteNotificationChannel**](docs/NotificationChannelApi.md#DeleteNotificationChannel) | **DELETE** /api/notificationChannels/{channelId} | Delete a notification channel
*NotificationChannelApi* | [**GetNotificationChannel**](docs/NotificationChannelApi.md#GetNotificationChannel) | **GET** /api/notificationChannels/{channelId} | Retrieve a notification channel
*NotificationChannelApi* | [**GetNotificationChannels**](docs/NotificationChannelApi.md#GetNotificationChannels) | **GET** /api/notificationChannels | Retrieve notification channels
*NotificationChannelApi* | [**UpdateNotificationChannel**](docs/NotificationChannelApi.md#UpdateNotificationChannel) | **PUT** /api/notificationChannels/{channelId} | Update a notification channel
*PipelineApi* | [**GetPipeline**](docs/PipelineApi.md#GetPipeline) | **GET** /api/pipelines/{pipelineId} | Retrieve a pipeline.
*PipelineApi* | [**GetPipelineInputParameters**](docs/PipelineApi.md#GetPipelineInputParameters) | **GET** /api/pipelines/{pipelineId}/inputParameters | Retrieve input parameters for a pipeline.
*PipelineApi* | [**GetPipelineReferenceSets**](docs/PipelineApi.md#GetPipelineReferenceSets) | **GET** /api/pipelines/{pipelineId}/referenceSets | Retrieve the reference sets of a pipeline.
*PipelineApi* | [**GetPipelines**](docs/PipelineApi.md#GetPipelines) | **GET** /api/pipelines | Retrieve a list of pipelines.
*ProjectApi* | [**CreateProject**](docs/ProjectApi.md#CreateProject) | **POST** /api/projects | Create a new project.
*ProjectApi* | [**GetProject**](docs/ProjectApi.md#GetProject) | **GET** /api/projects/{projectId} | Retrieve a project.
*ProjectApi* | [**GetProjectBundle**](docs/ProjectApi.md#GetProjectBundle) | **GET** /api/projects/{projectId}/bundles/{bundleId} | Retrieve a project bundle.
*ProjectApi* | [**GetProjectBundles**](docs/ProjectApi.md#GetProjectBundles) | **GET** /api/projects/{projectId}/bundles | Retrieve project bundles.
*ProjectApi* | [**GetProjects**](docs/ProjectApi.md#GetProjects) | **GET** /api/projects | Retrieve a list of projects.
*ProjectApi* | [**LinkProjectBundle**](docs/ProjectApi.md#LinkProjectBundle) | **POST** /api/projects/{projectId}/bundles/{bundleId} | Link a bundle to a project.
*ProjectApi* | [**UnlinkProjectBundle**](docs/ProjectApi.md#UnlinkProjectBundle) | **DELETE** /api/projects/{projectId}/bundles/{bundleId} | Unlink a bundle from a project.
*ProjectApi* | [**UpdateProject**](docs/ProjectApi.md#UpdateProject) | **PUT** /api/projects/{projectId} | Update a project.
*ProjectAnalysisApi* | [**AbortAnalysis**](docs/ProjectAnalysisApi.md#AbortAnalysis) | **POST** /api/projects/{projectId}/analyses/{analysisId}:abort | Abort an analysis.
*ProjectAnalysisApi* | [**CreateCwlAnalysis**](docs/ProjectAnalysisApi.md#CreateCwlAnalysis) | **POST** /api/projects/{projectId}/analysis:cwl | Create and start an analysis for a CWL pipeline.
*ProjectAnalysisApi* | [**CreateNextflowAnalysis**](docs/ProjectAnalysisApi.md#CreateNextflowAnalysis) | **POST** /api/projects/{projectId}/analysis:nextflow | Create and start an analysis for a Nextflow pipeline.
*ProjectAnalysisApi* | [**GetAnalyses**](docs/ProjectAnalysisApi.md#GetAnalyses) | **GET** /api/projects/{projectId}/analyses | Retrieve the list of project analyses.
*ProjectAnalysisApi* | [**GetAnalysis**](docs/ProjectAnalysisApi.md#GetAnalysis) | **GET** /api/projects/{projectId}/analyses/{analysisId} | Retrieve an analysis.
*ProjectAnalysisApi* | [**GetAnalysisConfigurations**](docs/ProjectAnalysisApi.md#GetAnalysisConfigurations) | **GET** /api/projects/{projectId}/analyses/{analysisId}/configurations | Retrieve the configurations of an analysis.
*ProjectAnalysisApi* | [**GetAnalysisInputs**](docs/ProjectAnalysisApi.md#GetAnalysisInputs) | **GET** /api/projects/{projectId}/analyses/{analysisId}/inputs | Retrieve the inputs of an analysis.
*ProjectAnalysisApi* | [**GetAnalysisOutputs**](docs/ProjectAnalysisApi.md#GetAnalysisOutputs) | **GET** /api/projects/{projectId}/analyses/{analysisId}/outputs | Retrieve the outputs of an analysis.
*ProjectAnalysisApi* | [**GetAnalysisSteps**](docs/ProjectAnalysisApi.md#GetAnalysisSteps) | **GET** /api/projects/{projectId}/analyses/{analysisId}/steps | Retrieve the individual steps of an analysis.
*ProjectAnalysisApi* | [**HGetExecutionOutputObject**](docs/ProjectAnalysisApi.md#HGetExecutionOutputObject) | **GET** /api/projects/{projectId}/analyses/{analysisId}/rawOutput | Retrieve the raw output of an analysis.
*ProjectAnalysisApi* | [**UpdateAnalysis**](docs/ProjectAnalysisApi.md#UpdateAnalysis) | **PUT** /api/projects/{projectId}/analyses/{analysisId} | Update an analysis.
*ProjectBaseApi* | [**CreateBaseConnectionDetails**](docs/ProjectBaseApi.md#CreateBaseConnectionDetails) | **POST** /api/projects/{projectId}/base:connectionDetails | Creates the connection details to snowflake instance.
*ProjectBaseJobApi* | [**GetBaseJob**](docs/ProjectBaseJobApi.md#GetBaseJob) | **GET** /api/projects/{projectId}/base/jobs/{baseJobId} | Retrieve a base job.
*ProjectBaseJobApi* | [**GetBaseJobs**](docs/ProjectBaseJobApi.md#GetBaseJobs) | **GET** /api/projects/{projectId}/base/jobs | Retrieve a list of base jobs
*ProjectBaseTableApi* | [**GetBaseTables**](docs/ProjectBaseTableApi.md#GetBaseTables) | **GET** /api/projects/{projectId}/base/tables | Retrieve a liste of base tables.
*ProjectBaseTableApi* | [**LoadData**](docs/ProjectBaseTableApi.md#LoadData) | **POST** /api/projects/{projectId}/base/tables/{tableId}:loadData | Load data in a base table.
*ProjectCustomEventsApi* | [**CreateCustomEvent**](docs/ProjectCustomEventsApi.md#CreateCustomEvent) | **POST** /api/projects/{projectId}/customEvents | Create a new custom event.
*ProjectCustomNotificationSubscriptionsApi* | [**CreateNotificationSubscription**](docs/ProjectCustomNotificationSubscriptionsApi.md#CreateNotificationSubscription) | **POST** /api/projects/{projectId}/customNotificationSubscriptions | Create a custom notification subscription
*ProjectCustomNotificationSubscriptionsApi* | [**DeleteNotificationSubscription**](docs/ProjectCustomNotificationSubscriptionsApi.md#DeleteNotificationSubscription) | **DELETE** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Delete a custom notification subscription
*ProjectCustomNotificationSubscriptionsApi* | [**GetNotificationSubscription**](docs/ProjectCustomNotificationSubscriptionsApi.md#GetNotificationSubscription) | **GET** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Retrieve a notification subscription
*ProjectCustomNotificationSubscriptionsApi* | [**GetNotificationSubscriptions**](docs/ProjectCustomNotificationSubscriptionsApi.md#GetNotificationSubscriptions) | **GET** /api/projects/{projectId}/customNotificationSubscriptions | Retrieve notification subscriptions
*ProjectCustomNotificationSubscriptionsApi* | [**UpdateNotificationSubscription**](docs/ProjectCustomNotificationSubscriptionsApi.md#UpdateNotificationSubscription) | **PUT** /api/projects/{projectId}/customNotificationSubscriptions/{subscriptionId} | Update a notification subscription
*ProjectDataApi* | [**AddSecondaryData**](docs/ProjectDataApi.md#AddSecondaryData) | **POST** /api/projects/{projectId}/data/{dataId}/secondaryData/{secondaryDataId} | Add secondary data to data.
*ProjectDataApi* | [**ArchiveData**](docs/ProjectDataApi.md#ArchiveData) | **POST** /api/projects/{projectId}/data/{dataId}:archive | Schedule this data for archival.
*ProjectDataApi* | [**CompleteFolderUploadSession**](docs/ProjectDataApi.md#CompleteFolderUploadSession) | **POST** /api/projects/{projectId}/data/{dataId}/folderUploadSessions/{folderUploadSessionId}:complete | Complete a trackable folder upload session.
*ProjectDataApi* | [**CreateDataInProject**](docs/ProjectDataApi.md#CreateDataInProject) | **POST** /api/projects/{projectId}/data | Create data in this project.
*ProjectDataApi* | [**CreateDownloadUrlForData**](docs/ProjectDataApi.md#CreateDownloadUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createDownloadUrl | Retrieve a download URL for this data.
*ProjectDataApi* | [**CreateFolderUploadSession**](docs/ProjectDataApi.md#CreateFolderUploadSession) | **POST** /api/projects/{projectId}/data/{dataId}/folderUploadSessions | Create a trackable folder upload session.
*ProjectDataApi* | [**CreateInlineViewUrlForData**](docs/ProjectDataApi.md#CreateInlineViewUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createInlineViewUrl | Retrieve an URL for this data to use for inline view in a browser.
*ProjectDataApi* | [**CreateTemporaryCredentialsForData**](docs/ProjectDataApi.md#CreateTemporaryCredentialsForData) | **POST** /api/projects/{projectId}/data/{dataId}:createTemporaryCredentials | Retrieve temporary credentials for this data.
*ProjectDataApi* | [**CreateUploadUrlForData**](docs/ProjectDataApi.md#CreateUploadUrlForData) | **POST** /api/projects/{projectId}/data/{dataId}:createUploadUrl | Retrieve an upload URL for this data.
*ProjectDataApi* | [**DeleteData**](docs/ProjectDataApi.md#DeleteData) | **POST** /api/projects/{projectId}/data/{dataId}:delete | Schedule this data for deletion.
*ProjectDataApi* | [**GetDataEligibleForLinking**](docs/ProjectDataApi.md#GetDataEligibleForLinking) | **GET** /api/projects/{projectId}/data/eligibleForLinking | Retrieve a list of data eligible for linking to the current project.
*ProjectDataApi* | [**GetFolderUploadSession**](docs/ProjectDataApi.md#GetFolderUploadSession) | **GET** /api/projects/{projectId}/data/{dataId}/folderUploadSessions/{folderUploadSessionId} | Retrieve folder upload session details.
*ProjectDataApi* | [**GetNonSampleProjectData**](docs/ProjectDataApi.md#GetNonSampleProjectData) | **GET** /api/projects/{projectId}/data/nonSampleData | Retrieve a list of project data not linked to a sample.
*ProjectDataApi* | [**GetProjectData**](docs/ProjectDataApi.md#GetProjectData) | **GET** /api/projects/{projectId}/data/{dataId} | Retrieve a project data.
*ProjectDataApi* | [**GetProjectDataChildren**](docs/ProjectDataApi.md#GetProjectDataChildren) | **GET** /api/projects/{projectId}/data/{dataId}/children | Retrieve the children of this data.
*ProjectDataApi* | [**GetProjectDataList**](docs/ProjectDataApi.md#GetProjectDataList) | **GET** /api/projects/{projectId}/data | Retrieve the list of project data.
*ProjectDataApi* | [**GetProjectsLinkedToData**](docs/ProjectDataApi.md#GetProjectsLinkedToData) | **GET** /api/projects/{projectId}/data/{dataId}/linkedProjects | Retrieve a list of projects to which this data is linked.
*ProjectDataApi* | [**GetSecondaryData**](docs/ProjectDataApi.md#GetSecondaryData) | **GET** /api/projects/{projectId}/data/{dataId}/secondaryData | Retrieve a list of secondary data for data.
*ProjectDataApi* | [**LinkDataToProject**](docs/ProjectDataApi.md#LinkDataToProject) | **POST** /api/projects/{projectId}/data/{dataId} | Link data to this project.
*ProjectDataApi* | [**RemoveSecondaryData**](docs/ProjectDataApi.md#RemoveSecondaryData) | **DELETE** /api/projects/{projectId}/data/{dataId}/secondaryData/{secondaryDataId} | Remove secondary data from data.
*ProjectDataApi* | [**ScheduleDownloadForData**](docs/ProjectDataApi.md#ScheduleDownloadForData) | **POST** /api/projects/{projectId}/data/{dataId}:scheduleDownload | Schedule a download.
*ProjectDataApi* | [**UnarchiveData**](docs/ProjectDataApi.md#UnarchiveData) | **POST** /api/projects/{projectId}/data/{dataId}:unarchive | Schedule this data for unarchival.
*ProjectDataApi* | [**UnlinkDataFromProject**](docs/ProjectDataApi.md#UnlinkDataFromProject) | **POST** /api/projects/{projectId}/data/{dataId}:unlink | Unlink data from this project.
*ProjectDataApi* | [**UpdateProjectData**](docs/ProjectDataApi.md#UpdateProjectData) | **PUT** /api/projects/{projectId}/data/{dataId} | Update this project data.
*ProjectDataTransferApi* | [**AbortDataTransfer**](docs/ProjectDataTransferApi.md#AbortDataTransfer) | **POST** /api/projects/{projectId}/dataTransfers/{dataTransferId}:abort | Abort a data transfer.
*ProjectDataTransferApi* | [**GetDataTransfer**](docs/ProjectDataTransferApi.md#GetDataTransfer) | **GET** /api/projects/{projectId}/dataTransfers/{dataTransferId} | Retrieve a data transfer.
*ProjectDataTransferApi* | [**GetDataTransfers**](docs/ProjectDataTransferApi.md#GetDataTransfers) | **GET** /api/projects/{projectId}/dataTransfers | Retrieve a list of data transfers.
*ProjectNotificationSubscriptionsApi* | [**CreateNotificationSubscription1**](docs/ProjectNotificationSubscriptionsApi.md#CreateNotificationSubscription1) | **POST** /api/projects/{projectId}/notificationSubscriptions | Create a notification subscription
*ProjectNotificationSubscriptionsApi* | [**DeleteNotificationSubscription1**](docs/ProjectNotificationSubscriptionsApi.md#DeleteNotificationSubscription1) | **DELETE** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Delete a notification subscription
*ProjectNotificationSubscriptionsApi* | [**GetNotificationSubscription1**](docs/ProjectNotificationSubscriptionsApi.md#GetNotificationSubscription1) | **GET** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Retrieve a notification subscription
*ProjectNotificationSubscriptionsApi* | [**GetNotificationSubscriptions1**](docs/ProjectNotificationSubscriptionsApi.md#GetNotificationSubscriptions1) | **GET** /api/projects/{projectId}/notificationSubscriptions | Retrieve notification subscriptions
*ProjectNotificationSubscriptionsApi* | [**UpdateNotificationSubscription1**](docs/ProjectNotificationSubscriptionsApi.md#UpdateNotificationSubscription1) | **PUT** /api/projects/{projectId}/notificationSubscriptions/{subscriptionId} | Update a notification subscription
*ProjectPermissionApi* | [**CreateProjectPermission**](docs/ProjectPermissionApi.md#CreateProjectPermission) | **POST** /api/projects/{projectId}/permissions | Create a project permission.
*ProjectPermissionApi* | [**GetProjectPermission**](docs/ProjectPermissionApi.md#GetProjectPermission) | **GET** /api/projects/{projectId}/permissions/{permissionId} | Retrieve a project permission.
*ProjectPermissionApi* | [**GetProjectPermissions**](docs/ProjectPermissionApi.md#GetProjectPermissions) | **GET** /api/projects/{projectId}/permissions | Retrieve a list of project permissions.
*ProjectPermissionApi* | [**UpdateProjectPermission**](docs/ProjectPermissionApi.md#UpdateProjectPermission) | **PUT** /api/projects/{projectId}/permissions/{permissionId} | Update a project permission.
*ProjectPipelineApi* | [**CreateCwlPipeline**](docs/ProjectPipelineApi.md#CreateCwlPipeline) | **POST** /api/projects/{projectId}/pipelines:createCwlPipeline | Create a CWL pipeline within a project.
*ProjectPipelineApi* | [**CreateNextflowPipeline**](docs/ProjectPipelineApi.md#CreateNextflowPipeline) | **POST** /api/projects/{projectId}/pipelines:createNextflowPipeline | Create a Nextflow pipeline within a project.
*ProjectPipelineApi* | [**GetProjectPipeline**](docs/ProjectPipelineApi.md#GetProjectPipeline) | **GET** /api/projects/{projectId}/pipelines/{pipelineId} | Retrieve a project pipeline.
*ProjectPipelineApi* | [**GetProjectPipelineInputParameters**](docs/ProjectPipelineApi.md#GetProjectPipelineInputParameters) | **GET** /api/projects/{projectId}/pipelines/{pipelineId}/inputParameters | Retrieve input parameters for a project pipeline.
*ProjectPipelineApi* | [**GetProjectPipelineReferenceSets**](docs/ProjectPipelineApi.md#GetProjectPipelineReferenceSets) | **GET** /api/projects/{projectId}/pipelines/{pipelineId}/referenceSets | Retrieve the reference sets of a project pipeline.
*ProjectPipelineApi* | [**GetProjectPipelines**](docs/ProjectPipelineApi.md#GetProjectPipelines) | **GET** /api/projects/{projectId}/pipelines | Retrieve a list of project pipelines.
*ProjectPipelineApi* | [**LinkPipelineToProject**](docs/ProjectPipelineApi.md#LinkPipelineToProject) | **POST** /api/projects/{projectId}/pipelines/{pipelineId} | Link a pipeline to a project.
*ProjectPipelineApi* | [**ReleasePipeline**](docs/ProjectPipelineApi.md#ReleasePipeline) | **POST** /api/projects/{projectId}/pipelines/{pipelineId}:release | Release a pipeline.
*ProjectPipelineApi* | [**UnlinkPipelineFromProject**](docs/ProjectPipelineApi.md#UnlinkPipelineFromProject) | **DELETE** /api/projects/{projectId}/pipelines/{pipelineId} | Unlink a pipeline from a project.
*ProjectSampleApi* | [**AddMetadataModelToSample**](docs/ProjectSampleApi.md#AddMetadataModelToSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/metadata/{metadataModelId} | Add a metadata model to a sample.
*ProjectSampleApi* | [**CompleteProjectSample**](docs/ProjectSampleApi.md#CompleteProjectSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:complete | Completes the sample after data has been linked to it.
*ProjectSampleApi* | [**CreateSampleInProject**](docs/ProjectSampleApi.md#CreateSampleInProject) | **POST** /api/projects/{projectId}/samples | Create a new sample in this project
*ProjectSampleApi* | [**DeepDeleteSample**](docs/ProjectSampleApi.md#DeepDeleteSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteDeep | Delete a sample together with all of its data.
*ProjectSampleApi* | [**DeleteAndUnlinkSample**](docs/ProjectSampleApi.md#DeleteAndUnlinkSample) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteUnlink | Delete a sample and unlink its data.
*ProjectSampleApi* | [**DeleteSampleWithInput**](docs/ProjectSampleApi.md#DeleteSampleWithInput) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteWithInput | Delete a sample as well as its input data.
*ProjectSampleApi* | [**GetProjectSample**](docs/ProjectSampleApi.md#GetProjectSample) | **GET** /api/projects/{projectId}/samples/{sampleId} | Retrieve a project sample.
*ProjectSampleApi* | [**GetProjectSamples**](docs/ProjectSampleApi.md#GetProjectSamples) | **POST** /api/projects/{projectId}/samples:search | Retrieve project samples.
*ProjectSampleApi* | [**GetProjectsForSample**](docs/ProjectSampleApi.md#GetProjectsForSample) | **GET** /api/projects/{projectId}/samples/{sampleId}/projects | Retrieve a list of projects for this sample.
*ProjectSampleApi* | [**GetSampleDataList**](docs/ProjectSampleApi.md#GetSampleDataList) | **GET** /api/projects/{projectId}/samples/{sampleId}/data | Retrieve the list of sample data.
*ProjectSampleApi* | [**GetSampleHistory**](docs/ProjectSampleApi.md#GetSampleHistory) | **GET** /api/projects/{projectId}/samples/{sampleId}/history | Retrieve sample history.
*ProjectSampleApi* | [**GetSampleMetadataField**](docs/ProjectSampleApi.md#GetSampleMetadataField) | **GET** /api/projects/{projectId}/samples/{sampleId}/metadata/field/{fieldId} | Retrieve a metadata field.
*ProjectSampleApi* | [**GetSampleMetadataFieldCount**](docs/ProjectSampleApi.md#GetSampleMetadataFieldCount) | **GET** /api/projects/{projectId}/samples/{sampleId}/metadata/{fieldId}/fieldCount | Retrieves the number of occurrences of a given field.
*ProjectSampleApi* | [**LinkDataToSample**](docs/ProjectSampleApi.md#LinkDataToSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/data/{dataId} | Link data to a sample.
*ProjectSampleApi* | [**LinkSampleToProject**](docs/ProjectSampleApi.md#LinkSampleToProject) | **POST** /api/projects/{projectId}/samples/{sampleId} | Link a sample to a project.
*ProjectSampleApi* | [**MarkSampleDeleted**](docs/ProjectSampleApi.md#MarkSampleDeleted) | **POST** /api/projects/{projectId}/samples/{sampleId}:deleteMark | Mark a sample deleted.
*ProjectSampleApi* | [**UnlinkDataFromSample**](docs/ProjectSampleApi.md#UnlinkDataFromSample) | **POST** /api/projects/{projectId}/samples/{sampleId}/data/{dataId}:unlink | Unlink data from a sample.
*ProjectSampleApi* | [**UnlinkSampleFromProject**](docs/ProjectSampleApi.md#UnlinkSampleFromProject) | **POST** /api/projects/{projectId}/samples/{sampleId}:unlink | Unlink a sample from a project.
*ProjectSampleApi* | [**UpdateProjectSample**](docs/ProjectSampleApi.md#UpdateProjectSample) | **PUT** /api/projects/{projectId}/samples/{sampleId} | Update a project sample.
*ProjectSampleApi* | [**UpdateSampleMetadataFields**](docs/ProjectSampleApi.md#UpdateSampleMetadataFields) | **POST** /api/projects/{projectId}/samples/{sampleId}/metadata:updateFields | Update metadata fields.
*RegionApi* | [**GetRegion**](docs/RegionApi.md#GetRegion) | **GET** /api/regions/{regionId} | Retrieve a region. Only the regions the user has access to through his/her entitlements can be retrieved.
*RegionApi* | [**GetRegions**](docs/RegionApi.md#GetRegions) | **GET** /api/regions | Retrieve a list of regions. Only the regions the user has access to through his/her entitlements are returned.
*SampleApi* | [**GetSamples**](docs/SampleApi.md#GetSamples) | **GET** /api/samples | Retrieve a list of samples.
*StorageBundleApi* | [**GetStorageBundles**](docs/StorageBundleApi.md#GetStorageBundles) | **GET** /api/storageBundles | Retrieve a list of storage bundles.
*StorageConfigurationApi* | [**CreateStorageConfiguration**](docs/StorageConfigurationApi.md#CreateStorageConfiguration) | **POST** /api/storageConfigurations | Create a new storage configuration
*StorageConfigurationApi* | [**GetStorageConfiguration**](docs/StorageConfigurationApi.md#GetStorageConfiguration) | **GET** /api/storageConfigurations/{storageConfigurationId} | Retrieve a storage configuration.
*StorageConfigurationApi* | [**GetStorageConfigurationDetails**](docs/StorageConfigurationApi.md#GetStorageConfigurationDetails) | **GET** /api/storageConfigurations/{storageConfigurationId}/details | Retrieve a storage configuration detail.
*StorageConfigurationApi* | [**GetStorageConfigurations**](docs/StorageConfigurationApi.md#GetStorageConfigurations) | **GET** /api/storageConfigurations | Retrieve a list of storage configurations.
*StorageConfigurationApi* | [**ShareStorageConfiguration**](docs/StorageConfigurationApi.md#ShareStorageConfiguration) | **POST** /api/storageConfigurations/{storageConfigurationId}:share | Share your own storage configuration with tenant.
*StorageCredentialsApi* | [**CreateStorageCredential**](docs/StorageCredentialsApi.md#CreateStorageCredential) | **POST** /api/storageCredentials | Create a new storage credential
*StorageCredentialsApi* | [**GetStorageCredential**](docs/StorageCredentialsApi.md#GetStorageCredential) | **GET** /api/storageCredentials/{storageCredentialId} | Retrieve a storage credential.
*StorageCredentialsApi* | [**GetStorageCredentials**](docs/StorageCredentialsApi.md#GetStorageCredentials) | **GET** /api/storageCredentials | Retrieve a list of storage credentials.
*StorageCredentialsApi* | [**ShareStorageCredential**](docs/StorageCredentialsApi.md#ShareStorageCredential) | **POST** /api/storageCredentials/{storageCredentialId}:share | Share your own storage credentials with tenant.
*StorageCredentialsApi* | [**UpdateStorageCredentialSecrets**](docs/StorageCredentialsApi.md#UpdateStorageCredentialSecrets) | **POST** /api/storageCredentials/{storageCredentialId}:updateSecrets | Update a storage credential's secrets.
*TokenApi* | [**CreateJwtToken**](docs/TokenApi.md#CreateJwtToken) | **POST** /api/tokens | Generate a JWT using an API-key, Basic Authentication or a psToken.
*TokenApi* | [**RefreshJwtToken**](docs/TokenApi.md#RefreshJwtToken) | **POST** /api/tokens:refresh | Refresh a JWT using a not yet expired, still valid JWT.
*UserApi* | [**ApproveUser**](docs/UserApi.md#ApproveUser) | **POST** /api/users/{userId}:approve | Approve a user.
*UserApi* | [**AssignTenantAdminRightsToUser**](docs/UserApi.md#AssignTenantAdminRightsToUser) | **POST** /api/users/{userId}:assignTenantAdministratorRights | Assign tenant administrator rights to a user.
*UserApi* | [**GetUser**](docs/UserApi.md#GetUser) | **GET** /api/users/{userId} | Retrieve a user.
*UserApi* | [**GetUsers**](docs/UserApi.md#GetUsers) | **GET** /api/users | Retrieve a list of users.
*UserApi* | [**RevokeTenantAdminRightsToUser**](docs/UserApi.md#RevokeTenantAdminRightsToUser) | **POST** /api/users/{userId}:revokeTenantAdministratorRights | Revoke tenant administrator rights to a user.
*UserApi* | [**UpdateUser**](docs/UserApi.md#UpdateUser) | **PUT** /api/users/{userId} | Update a user.
*WorkgroupApi* | [**GetWorkgroup**](docs/WorkgroupApi.md#GetWorkgroup) | **GET** /api/workgroups/{workgroupId} | Retrieve a workgroup.
*WorkgroupApi* | [**GetWorkgroups**](docs/WorkgroupApi.md#GetWorkgroups) | **GET** /api/workgroups | Retrieve a list of workgroups.


## Documentation for Models

 - [AWSDetails](docs/AWSDetails.md)
 - [ActivationCodeDetail](docs/ActivationCodeDetail.md)
 - [ActivationCodeDetailList](docs/ActivationCodeDetailList.md)
 - [ActivationCodeDetailUsage](docs/ActivationCodeDetailUsage.md)
 - [Analysis](docs/Analysis.md)
 - [AnalysisData](docs/AnalysisData.md)
 - [AnalysisDataInput](docs/AnalysisDataInput.md)
 - [AnalysisInput](docs/AnalysisInput.md)
 - [AnalysisInputDataMount](docs/AnalysisInputDataMount.md)
 - [AnalysisInputList](docs/AnalysisInputList.md)
 - [AnalysisOutput](docs/AnalysisOutput.md)
 - [AnalysisOutputList](docs/AnalysisOutputList.md)
 - [AnalysisPagedList](docs/AnalysisPagedList.md)
 - [AnalysisParameter](docs/AnalysisParameter.md)
 - [AnalysisRawOutput](docs/AnalysisRawOutput.md)
 - [AnalysisReferenceDataParameter](docs/AnalysisReferenceDataParameter.md)
 - [AnalysisStep](docs/AnalysisStep.md)
 - [AnalysisStepList](docs/AnalysisStepList.md)
 - [AnalysisStorage](docs/AnalysisStorage.md)
 - [AnalysisStorageList](docs/AnalysisStorageList.md)
 - [AnalysisTag](docs/AnalysisTag.md)
 - [Application](docs/Application.md)
 - [AwsCredentials](docs/AwsCredentials.md)
 - [AwsTempCredentials](docs/AwsTempCredentials.md)
 - [BaseConnection](docs/BaseConnection.md)
 - [BaseJob](docs/BaseJob.md)
 - [BaseJobList](docs/BaseJobList.md)
 - [Bundle](docs/Bundle.md)
 - [BundleData](docs/BundleData.md)
 - [BundleDataPagedList](docs/BundleDataPagedList.md)
 - [BundleList](docs/BundleList.md)
 - [BundlePagedList](docs/BundlePagedList.md)
 - [BundlePipeline](docs/BundlePipeline.md)
 - [BundlePipelineList](docs/BundlePipelineList.md)
 - [BundleSample](docs/BundleSample.md)
 - [BundleSamplePagedList](docs/BundleSamplePagedList.md)
 - [BundleTool](docs/BundleTool.md)
 - [BundleToolsList](docs/BundleToolsList.md)
 - [CWLToolDefinition](docs/CWLToolDefinition.md)
 - [CompleteFolderUploadSession](docs/CompleteFolderUploadSession.md)
 - [Connector](docs/Connector.md)
 - [ConnectorList](docs/ConnectorList.md)
 - [Country](docs/Country.md)
 - [CreateBundle](docs/CreateBundle.md)
 - [CreateConnector](docs/CreateConnector.md)
 - [CreateCustomEvent](docs/CreateCustomEvent.md)
 - [CreateCustomNotificationSubscription](docs/CreateCustomNotificationSubscription.md)
 - [CreateCwlAnalysis](docs/CreateCwlAnalysis.md)
 - [CreateData](docs/CreateData.md)
 - [CreateDownloadRule](docs/CreateDownloadRule.md)
 - [CreateNextflowAnalysis](docs/CreateNextflowAnalysis.md)
 - [CreateNotificationChannel](docs/CreateNotificationChannel.md)
 - [CreateNotificationSubscription](docs/CreateNotificationSubscription.md)
 - [CreateProject](docs/CreateProject.md)
 - [CreateProjectPermission](docs/CreateProjectPermission.md)
 - [CreateSample](docs/CreateSample.md)
 - [CreateStorageConfiguration](docs/CreateStorageConfiguration.md)
 - [CreateStorageCredential](docs/CreateStorageCredential.md)
 - [CreateTemporaryCredentials](docs/CreateTemporaryCredentials.md)
 - [CreateUploadRule](docs/CreateUploadRule.md)
 - [CustomNotificationSubscription](docs/CustomNotificationSubscription.md)
 - [CustomNotificationSubscriptionList](docs/CustomNotificationSubscriptionList.md)
 - [CwlAnalysisInput](docs/CwlAnalysisInput.md)
 - [CwlAnalysisJsonInput](docs/CwlAnalysisJsonInput.md)
 - [CwlAnalysisStructuredInput](docs/CwlAnalysisStructuredInput.md)
 - [CwlToolDefinitionList](docs/CwlToolDefinitionList.md)
 - [Data](docs/Data.md)
 - [DataDetails](docs/DataDetails.md)
 - [DataFormat](docs/DataFormat.md)
 - [DataFormatPagedList](docs/DataFormatPagedList.md)
 - [DataList](docs/DataList.md)
 - [DataPagedList](docs/DataPagedList.md)
 - [DataTag](docs/DataTag.md)
 - [DataTransfer](docs/DataTransfer.md)
 - [DataTransfers](docs/DataTransfers.md)
 - [Download](docs/Download.md)
 - [DownloadRule](docs/DownloadRule.md)
 - [DownloadRuleList](docs/DownloadRuleList.md)
 - [EventCode](docs/EventCode.md)
 - [EventCodeList](docs/EventCodeList.md)
 - [EventLog](docs/EventLog.md)
 - [EventLogList](docs/EventLogList.md)
 - [ExecutionConfiguration](docs/ExecutionConfiguration.md)
 - [ExecutionConfigurationList](docs/ExecutionConfigurationList.md)
 - [Field](docs/Field.md)
 - [FieldId](docs/FieldId.md)
 - [FieldList](docs/FieldList.md)
 - [FindProjectSamples](docs/FindProjectSamples.md)
 - [FindSampleBooleanCondition](docs/FindSampleBooleanCondition.md)
 - [FindSampleCondition](docs/FindSampleCondition.md)
 - [FindSampleDateCondition](docs/FindSampleDateCondition.md)
 - [FindSampleNumberCondition](docs/FindSampleNumberCondition.md)
 - [FolderUploadSession](docs/FolderUploadSession.md)
 - [InlineView](docs/InlineView.md)
 - [InputParameter](docs/InputParameter.md)
 - [InputParameterList](docs/InputParameterList.md)
 - [InputPart](docs/InputPart.md)
 - [InputPartMediaType](docs/InputPartMediaType.md)
 - [Link](docs/Link.md)
 - [Links](docs/Links.md)
 - [LoadDataInBaseRequest](docs/LoadDataInBaseRequest.md)
 - [MetadataField](docs/MetadataField.md)
 - [MetadataModel](docs/MetadataModel.md)
 - [MetadataModelList](docs/MetadataModelList.md)
 - [Model](docs/Model.md)
 - [MultipartFormDataInput](docs/MultipartFormDataInput.md)
 - [NextflowAnalysisInput](docs/NextflowAnalysisInput.md)
 - [NotificationChannel](docs/NotificationChannel.md)
 - [NotificationChannelList](docs/NotificationChannelList.md)
 - [NotificationSubscription](docs/NotificationSubscription.md)
 - [NotificationSubscriptionList](docs/NotificationSubscriptionList.md)
 - [Pipeline](docs/Pipeline.md)
 - [PipelineBundle](docs/PipelineBundle.md)
 - [PipelineList](docs/PipelineList.md)
 - [PipelineTag](docs/PipelineTag.md)
 - [Problem](docs/Problem.md)
 - [Project](docs/Project.md)
 - [ProjectBaseTable](docs/ProjectBaseTable.md)
 - [ProjectBaseTableList](docs/ProjectBaseTableList.md)
 - [ProjectBundle](docs/ProjectBundle.md)
 - [ProjectBundleList](docs/ProjectBundleList.md)
 - [ProjectData](docs/ProjectData.md)
 - [ProjectDataPagedList](docs/ProjectDataPagedList.md)
 - [ProjectList](docs/ProjectList.md)
 - [ProjectPagedList](docs/ProjectPagedList.md)
 - [ProjectPermission](docs/ProjectPermission.md)
 - [ProjectPermissionList](docs/ProjectPermissionList.md)
 - [ProjectPipeline](docs/ProjectPipeline.md)
 - [ProjectPipelineList](docs/ProjectPipelineList.md)
 - [ProjectSample](docs/ProjectSample.md)
 - [ProjectSamplePagedList](docs/ProjectSamplePagedList.md)
 - [ProjectTag](docs/ProjectTag.md)
 - [RcloneTempCredentials](docs/RcloneTempCredentials.md)
 - [ReferenceData](docs/ReferenceData.md)
 - [ReferenceDataList](docs/ReferenceDataList.md)
 - [ReferenceSet](docs/ReferenceSet.md)
 - [ReferenceSetList](docs/ReferenceSetList.md)
 - [Region](docs/Region.md)
 - [RegionList](docs/RegionList.md)
 - [Sample](docs/Sample.md)
 - [SampleHistory](docs/SampleHistory.md)
 - [SampleHistoryList](docs/SampleHistoryList.md)
 - [SamplePagedList](docs/SamplePagedList.md)
 - [SampleTag](docs/SampleTag.md)
 - [ScheduleDownload](docs/ScheduleDownload.md)
 - [SearchMatchingActivationCodesForCwlAnalysis](docs/SearchMatchingActivationCodesForCwlAnalysis.md)
 - [SearchMatchingActivationCodesForNextflowAnalysis](docs/SearchMatchingActivationCodesForNextflowAnalysis.md)
 - [Species](docs/Species.md)
 - [StorageBundle](docs/StorageBundle.md)
 - [StorageBundleList](docs/StorageBundleList.md)
 - [StorageConfiguration](docs/StorageConfiguration.md)
 - [StorageConfigurationDetails](docs/StorageConfigurationDetails.md)
 - [StorageConfigurationWithDetails](docs/StorageConfigurationWithDetails.md)
 - [StorageConfigurationWithDetailsList](docs/StorageConfigurationWithDetailsList.md)
 - [StorageCredential](docs/StorageCredential.md)
 - [StorageCredentialList](docs/StorageCredentialList.md)
 - [TempCredentials](docs/TempCredentials.md)
 - [Token](docs/Token.md)
 - [Type](docs/Type.md)
 - [TypeList](docs/TypeList.md)
 - [UpdateMetadata](docs/UpdateMetadata.md)
 - [UpdateMetadataFieldGroup](docs/UpdateMetadataFieldGroup.md)
 - [UpdateSingleMetadataField](docs/UpdateSingleMetadataField.md)
 - [UpdateStorageCredentialSecrets](docs/UpdateStorageCredentialSecrets.md)
 - [Upload](docs/Upload.md)
 - [UploadRule](docs/UploadRule.md)
 - [UploadRuleList](docs/UploadRuleList.md)
 - [User](docs/User.md)
 - [UserList](docs/UserList.md)
 - [Workgroup](docs/Workgroup.md)
 - [WorkgroupList](docs/WorkgroupList.md)


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



