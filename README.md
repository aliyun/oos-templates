# OOS Templates
This repository contains examples and best practices for building OOS templates.

## Introduction
The Operation Orchestration Service (OOS) is a powerful automated task management and execution service that helps users perform cloud operations.

The user defines the execution tasks, execution order, execution input and output, etc. through the template, and automates the task by executing the template. The service supports multiple operating modes: automated, semi-automated and interactive to help users complete diverse automation tasks. Common scenarios such as: repeated operation and maintenance tasks, event-driven automation scenarios, special scenarios that require approval, etc. are supported well.

The Operation Orchestration Service (OOS) can also be used as a standardized platform for operation and maintenance tasks, converting operation and maintenance manuals, operation manuals and maintenance manuals into templates, and finally implementing Automation as Code.

OOS sample templates are divided into two parts: public templates and cloud product actions.

## Cloud Product Actions
### ECS
| Name                                     |  Description                             |
| ---------------------------------------- | ---------------------------------------- |
| ACS::ECS::AllocatePublicIpAddress [YAML](CloudProductActions/ECS/YAML/ACS::ECS::AllocatePublicIpAddress.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::AllocatePublicIpAddress.json) | Assigns a public IP address to an instance. |
| ACS::ECS::AttachDisk [YAML](CloudProductActions/ECS/YAML/ACS::ECS::AttachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::AttachDisk.json) | Attaches a data disk to an ECS instance. |
| ACS::ECS::CreateAndAttachDisk [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateAndAttachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateAndAttachDisk.json) | Creates a disk and attaches a data disk to an ECS instance. |
| ACS::ECS::CreateAndAttachNetworkInterface [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateAndAttachNetworkInterface.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateAndAttachNetworkInterface.json) | Creates an elastic network interface (ENI) and attaches to an instance. |
| ACS::ECS::CreateImage [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateImage.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateImage.json) | Creates a custom image. |
| ACS::ECS::CreateSnapshot [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateSnapshot.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateSnapshot.json) | Creates a snapshot for a disk. |
| ACS::ECS::DeleteImage [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DeleteImage.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DeleteImage.json) | Deletes ECS image by specifying imageId. |
| ACS::ECS::DeleteInstance [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DeleteInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DeleteInstance.json) | Deletes ECS instance by specifying instance ID. |
| ACS::ECS::DescribeInstancesByName [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByName.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByName.json) | Views the ECS instances by specifying instance name. |
| ACS::ECS::DescribeInstancesByStatus [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByStatus.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByStatus.json) | Views the ECS instances by specifying instance status. |
| ACS::ECS::DescribeInstancesByTag [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByTag.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByTag.json) | Views the ECS instances by specifying tag. |
| ACS::ECS::DetachDisk [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DetachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DetachDisk.json) | Detaches a disk from an ECS instance. |
| ACS::ECS::InstallCloudAssistant [YAML](CloudProductActions/ECS/YAML/ACS::ECS::InstallCloudAssistant.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::InstallCloudAssistant.json) | Installs cloud assistant on ECS instance by specifying instanceId. |
| ACS::ECS::InstallLogtail [YAML](CloudProductActions/ECS/YAML/ACS::ECS::InstallLogtail.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::InstallLogtail.json) | Installs SLS agent on ECS instance by running a cloud assistant command. |
| ACS::ECS::ModifyInstanceVpcAttribute [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyInstanceVpcAttribute.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyInstanceVpcAttribute.json) | Modifies the VPC attributes of an ECS instance. |
| ACS::ECS::ModifyPrepaySpec [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyPrepaySpec.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyPrepaySpec.json) | Changes the type of your subscription instance. The new instance type will take effect for the entire lifecycle of the instance. |
| ACS::ECS::ModifyVncPassword [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyVncPassword.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyVncPassword.json) | Modifies the Web management terminal password of an ECS instance. |
| ACS::ECS::ReInitDisk [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ReInitDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ReInitDisk.json) | Resets a disk to its initial status. |
| ACS::ECS::RebootInstance [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RebootInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RebootInstance.json) | Restarts the ECS instance by specifying instanceId. |
| ACS::ECS::ReplaceSystemDisk [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ReplaceSystemDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ReplaceSystemDisk.json) | Replaces the system disk of an ECS instance. |
| ACS::ECS::ResetDisk [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResetDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResetDisk.json) | Rolls back a disk to the specific disk status by using one of its snapshots. |
| ACS::ECS::ResetPassword [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResetPassword.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResetPassword.json) | Resets password of an ECS instance. |
| ACS::ECS::ResizeDisk [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResizeDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResizeDisk.json) | Extends the size of a cloud disk. |
| ACS::ECS::RunCommand [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunCommand.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunCommand.json) | Creates a cloud assistant command and triggers it on one ECS instance. |
| ACS::ECS::RunInstances [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunInstances.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunInstances.json) | Creates one or more ECS instances. |
| ACS::ECS::RunInstancesFromTemplate [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunInstancesFromTemplate.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunInstancesFromTemplate.json) | Creates one or more instances by specifying launch template. |
| ACS::ECS::StartInstance [YAML](CloudProductActions/ECS/YAML/ACS::ECS::StartInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::StartInstance.json) | Starts an ECS instance. |
| ACS::ECS::StopInstance [YAML](CloudProductActions/ECS/YAML/ACS::ECS::StopInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::StopInstance.json) | Stops an ECS instance. |
### OOS
| Name                                     |  Description                             |
| ---------------------------------------- | ---------------------------------------- |
| ACS::Approve::DingTalkWebhook [YAML](CloudProductActions/OOS/YAML/ACS::Approve::DingTalkWebhook.yml) [JSON](CloudProductActions/OOS/JSON/ACS::Approve::DingTalkWebhook.json) | Sends notification to DingTalk via webhook for asking approval. The execution remains paused until approved or rejected. Please refer https://open-doc.dingtalk.com/microapp/serverapi2/qf2nxq for details. |
| ACS::Notify::DingTalkWebhook [YAML](CloudProductActions/OOS/YAML/ACS::Notify::DingTalkWebhook.yml) [JSON](CloudProductActions/OOS/JSON/ACS::Notify::DingTalkWebhook.json) | Sends notification to DingTalk via webhook. Please refer https://open-doc.dingtalk.com/microapp/serverapi2/qf2nxq for details. |
### RDS
| Name                                     |  Description                             |
| ---------------------------------------- | ---------------------------------------- |
| ACS::RDS::CreateBackup [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateBackup.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateBackup.json) | Creates backups of a RDS instance. |
| ACS::RDS::CreateDatabase [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateDatabase.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateDatabase.json) | Creates a new database in an instance. |
| ACS::RDS::CreateDbInstance [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateDbInstance.json) | Creates an RDS instance. |
| ACS::RDS::DeleteDbInstance [YAML](CloudProductActions/RDS/YAML/ACS::RDS::DeleteDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::DeleteDbInstance.json) | Deletes DB instance. |
| ACS::RDS::RecoveryDbInstance [YAML](CloudProductActions/RDS/YAML/ACS::RDS::RecoveryDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::RecoveryDbInstance.json) | Recoveries database to an existed or new instance. |
| ACS::RDS::RestartDbInstance [YAML](CloudProductActions/RDS/YAML/ACS::RDS::RestartDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::RestartDbInstance.json) | Restarts an RDS instance. |
| ACS::RDS::UpgradeDbInstanceEngineVersion [YAML](CloudProductActions/RDS/YAML/ACS::RDS::UpgradeDbInstanceEngineVersion.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::UpgradeDbInstanceEngineVersion.json) | Upgrades the database version of an instance. |
## Public Templates
| Name                                     |  Description                             |
| ---------------------------------------- | ---------------------------------------- |
| ACS-ECS-BulkyInstallLogAgentByInstanceIds [YAML](PublicTemplates/YAML/ACS-ECS-BulkyInstallLogAgentByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyInstallLogAgentByInstanceIds.json) | Installs SLS agent on ECS instances by specifying instance IDs. |
| ACS-ECS-BulkyInstallLogAgentByTag [YAML](PublicTemplates/YAML/ACS-ECS-BulkyInstallLogAgentByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyInstallLogAgentByTag.json) | Installs SLS agent on ECS instances by specifying tag. |
| ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds [YAML](PublicTemplates/YAML/ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds.json) | Upgrades internet bandwidth of ECS instances. |
| ACS-ECS-BuyCostlyInstancesWithApproval [YAML](PublicTemplates/YAML/ACS-ECS-BuyCostlyInstancesWithApproval.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BuyCostlyInstancesWithApproval.json) | Creates one or more ECS instances with approval. |
| ACS-ECS-DeleteInstancesWithApprovalByInstanceIds [YAML](PublicTemplates/YAML/ACS-ECS-DeleteInstancesWithApprovalByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-DeleteInstancesWithApprovalByInstanceIds.json) | Deletes the ECS instances with approval. |
| ACS-ECS-RebootInstancesByInstanceIds [YAML](PublicTemplates/YAML/ACS-ECS-RebootInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-RebootInstancesByInstanceIds.json) | Restarts the ECS instances by specifying instance IDs. The specified ECS instances should be in running status. |
| ACS-ECS-RebootInstancesByTag [YAML](PublicTemplates/YAML/ACS-ECS-RebootInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-RebootInstancesByTag.json) | Restarts the ECS instances by specifying tag. The specified ECS instances should be in running status. |
| ACS-ECS-ScheduleToRebootInstancesByTag [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToRebootInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToRebootInstancesByTag.json) | Schedules to reboot the ECS instances by specifying tag. |
| ACS-ECS-ScheduleToStartInstancesByTag [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToStartInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToStartInstancesByTag.json) | Schedules to start the ECS instances by specifying tag. |
| ACS-ECS-ScheduleToStopInstancesByTag [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToStopInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToStopInstancesByTag.json) | Schedules to stop the ECS instances by specifying tag. |
| ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds.json) | Schedules to upgrade internet bandwidth for ECS instances. |
| ACS-ECS-StartInstancesByInstanceIds [YAML](PublicTemplates/YAML/ACS-ECS-StartInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StartInstancesByInstanceIds.json) | Starts the ECS instances by specifying ECS instance IDs. The specified ECS instances should be in stopped status. |
| ACS-ECS-StartInstancesByTag [YAML](PublicTemplates/YAML/ACS-ECS-StartInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StartInstancesByTag.json) | Starts the ECS instances by specifying tag. The specified ECS instances should be in stopped status. |
| ACS-ECS-StopInstancesByInstanceIds [YAML](PublicTemplates/YAML/ACS-ECS-StopInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StopInstancesByInstanceIds.json) | Stops the ECS instances by specifying instance IDs. The specified ECS instances should be in running status. |
| ACS-ECS-StopInstancesByTag [YAML](PublicTemplates/YAML/ACS-ECS-StopInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StopInstancesByTag.json) | Stops the ECS instances by specifying tag. The specified ECS instances should be in running status. |
| ACS-ECS-UpdateImage [YAML](PublicTemplates/YAML/ACS-ECS-UpdateImage.yml) [JSON](PublicTemplates/JSON/ACS-ECS-UpdateImage.json) | Updates an existing ECS image via ECS Cloud Assistant then creates a ECS image. |
