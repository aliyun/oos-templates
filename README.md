# [Click here for English Version](#english)

# OOS Templates
本仓库包含了编写 OOS 模板的示例和最佳实践。

## 介绍
阿里云运维编排服务（Operation Orchestration Service，简称OOS）是一个全面的云上自动化运维平台，提供了运维任务的管理和执行。
典型的使用场景包括：事件驱动运维，批量操作运维，定时运维任务，跨地域运维等，OOS特别为一些重要的运维场景提供了审批，通知等功能。
通过使用OOS还可以达到标准化运维任务的目的，从而实践运维即代码（Operations as Code）的先进理念。
OOS支持跨产品使用，您可以使用OOS管理ECS、RDS、SLB、VPC等云产品。

欢迎体验 [OOS控制台](https://home.console.aliyun.com/redirect.htm?productId=ecs&path=automation/region/)，阅读 [OOS帮助文档](https://help.aliyun.com/product/119529.html) 以了解更多细节。

## 公共模板
| 序号   | 名称           | 描述（用途）                     | 链接         |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS-ECS-BulkyDeletePrepaidInstanceByInstanceIds | 批量的根据实例ID的列表释放预付费实例。输入包含-个必选参数：ECS实例ID列表。 | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyDeletePrepaidInstanceByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyDeletePrepaidInstanceByInstanceIds.json) |
| 2 | ACS-ECS-BulkyInstallLogAgentByInstanceIds | 批量的根据实例ID的列表安装日志代理Logtail。输入包含两个必选参数：ECS实例ID列表，Logtail用户定义的ID。 | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyInstallLogAgentByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyInstallLogAgentByInstanceIds.json) |
| 3 | ACS-ECS-BulkyInstallLogAgentByTag | 批量的根据实例标签安装日志代理Logtail。输入包含三个必选参数：ECS实例的标签键和标签值，Logtail用户定义的ID。 | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyInstallLogAgentByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyInstallLogAgentByTag.json) |
| 4 | ACS-ECS-BulkyRunCommandByTag | 批量的根据实例的标签运行云助手命令。输入包含四个必选参数：ECS实例的标签键和标签值，云助手命令，云助手命令类型。 | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyRunCommandByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyRunCommandByTag.json) |
| 5 | ACS-ECS-BulkyTagInstanceByLinuxKernelVersionAndInstanceIds | 批量的根据Linux内核版本为指定的ECS实例创建并绑定标签。输入包含两个必选参数：ECS实例ID列表, 标签键。 | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyTagInstanceByLinuxKernelVersionAndInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyTagInstanceByLinuxKernelVersionAndInstanceIds.json) |
| 6 | ACS-ECS-BulkyTagInstanceByOSTypeAndInstanceIds | 批量的根据操作系统类型为指定的ECS实例创建并绑定标签。输入包含两个必选参数：ECS实例ID列表，标签键。 | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyTagInstanceByOSTypeAndInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyTagInstanceByOSTypeAndInstanceIds.json) |
| 7 | ACS-ECS-BulkyTagInstanceByRunCommandResultAndInstanceIds | 批量的根据执行云助手命令返回的结果为指定的ECS实例创建并绑定标签。输入包含三个必选参数：ECS实例ID列表，标签键，云助手命令。 | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyTagInstanceByRunCommandResultAndInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyTagInstanceByRunCommandResultAndInstanceIds.json) |
| 8 | ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds | 批量升级ECS实例的临时带宽。执行时会对指定的多个实例执行ModifyInstanceNetworkSpec的OpenAPI调用。输入包含五个必选参数：ECS实例ID的列表，公网入带宽最大值，公网出带宽最大值，临时带宽升级开始时间，临时带宽升级结束时间。 | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds.json) |
| 9 | ACS-ECS-BuyCostlyInstancesWithApproval | 带有钉钉审批的ECS实例购买。执行时，会首先向指定的钉钉联系人（群）发送审批通知，审批通过后才会创建ECS。输入包含六个必选参数：钉钉accessToken，ECS镜像ID，实例类型，安全组ID，交换机ID，实例数量 。 | [YAML](PublicTemplates/YAML/ACS-ECS-RunInstancesWithApproval.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BuyCostlyInstancesWithApproval.json) |
| 10 | ACS-ECS-CloneInstancesAcrossAZ | 跨可用区批量复制实例，具体步骤为：获取待复制实例的规格，创建待复制实例的镜像，镜像创建成功后，在目的可用区运行与待复制实例规格相同的实例。输入包含的必选参数：待复制实例ID，模版执行所在的RegionID，目的可用区ID，目的可用区的安全组ID，目的可用区的交换机ID。 | [YAML](PublicTemplates/YAML/ACS-ECS-CloneInstancesAcrossAZ.yml) [JSON](PublicTemplates/JSON/ACS-ECS-CloneInstancesAcrossAZ.json) |
| 11 | ACS-ECS-CloneInstancesAcrossRegion | 跨Region批量复制实例，具体步骤为：创建待复制实例的镜像，镜像创建成功后，将镜像复制到目的Region，镜像复制完成后，在目的Region的目的可用区运行被复制的实例。输入包含的必选参数：待复制实例ID，待复制实例所在的RegionID，目的RegionID,目的Region的目的可用区ID，目的可用区的实例规格，目的可用区的安全组ID，目的可用区的交换机ID。 | [YAML](PublicTemplates/YAML/ACS-ECS-CloneInstancesAcrossRegion.yml) [JSON](PublicTemplates/JSON/ACS-ECS-CloneInstancesAcrossRegion.json) |
| 12 | ACS-ECS-DeleteInstancesWithApprovalByInstanceIds | 带有钉钉审批的ECS实例批量释放。输入包含两个必选参数：ECS实例ID列表，钉钉accessToken。 | [YAML](PublicTemplates/YAML/ACS-ECS-DeleteInstancesWithApprovalByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-DeleteInstancesWithApprovalByInstanceIds.json) |
| 13 | ACS-ECS-RebootInstancesByInstanceIds | 批量的根据实例ID的列表重启ECS实例。执行时会对指定的多个实例执行RebootInstance的OpenAPI调用，只有处于运行中状态的ECS实例才能被成功重启。输入包含一个必选参数：ECS实例ID的列表。 | [YAML](PublicTemplates/YAML/ACS-ECS-RebootInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-RebootInstancesByInstanceIds.json) |
| 14 | ACS-ECS-RebootInstancesByTag | 批量的根据实例的标签重启ECS实例。执行时会对指定标签下的实例执行RebootInstance的OpenAPI调用，只有处于运行中状态的ECS实例才能被成功重启。输入包含两个必选参数：ECS实例的标签键和标签值。 | [YAML](PublicTemplates/YAML/ACS-ECS-RebootInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-RebootInstancesByTag.json) |
| 15 | ACS-ECS-ScheduleToRebootInstancesByTag | 定时重启带有指定标签的ECS实例。在指定的时刻，对指定标签下的实例定时执行RebootInstance的OpenAPI调用，只有处于运行中状态的ECS实例才能被成功重启。输入包含四个必选参数：Cron表达式，定时任务的最后终止时间，ECS实例的标签键和标签值。 | [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToRebootInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToRebootInstancesByTag.json) |
| 16 | ACS-ECS-ScheduleToStartInstancesByTag | 定时启动带有指定标签的ECS实例。在指定的时刻，对指定标签下的实例定时执行StartInstance的OpenAPI调用，只有处于已停止状态的ECS实例才能被成功启动。输入包含四个必选参数：Cron表达式，定时任务的最后终止时间，ECS实例的标签键和标签值。 | [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToStartInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToStartInstancesByTag.json) |
| 17 | ACS-ECS-ScheduleToStopInstancesByTag | 定时停止带有指定标签的ECS实例。在指定的时刻，对指定标签下的实例执行StopInstance的OpenAPI调用，只有处于运行中状态的ECS实例才能被成功停止。输入包含四个必选参数：Cron表达式，定时任务的最后终止时间，ECS实例的标签键和标签值。 | [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToStopInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToStopInstancesByTag.json) |
| 18 | ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds | 定时批量升级ECS实例的临时带宽。在指定的时刻，对指定的多个实例执行ModifyInstanceNetworkSpec的OpenAPI调用。输入包含七个必选参数：Cron表达式，定时任务的最后终止时间，ECS实例ID的列表，公网入带宽最大值，公网出带宽最大值，临时带宽升级开始时间，临时带宽升级结束时间。 | [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds.json) |
| 19 | ACS-ECS-StartInstancesByInstanceIds | 批量的根据实例ID的列表启动ECS实例。执行时会对指定的多个实例执行StartInstance的OpenAPI调用，只有处于已停止状态的ECS实例才能被成功启动。输入包含一个必选参数：ECS实例ID的列表。 | [YAML](PublicTemplates/YAML/ACS-ECS-StartInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StartInstancesByInstanceIds.json) |
| 20 | ACS-ECS-StartInstancesByTag | 批量的根据实例的标签启动ECS实例。执行时会对指定标签下的实例执行StartInstance的OpenAPI调用，只有处于已停止状态的ECS实例才能被成功启动。输入包含两个必选参数：ECS实例的标签键和标签值。 | [YAML](PublicTemplates/YAML/ACS-ECS-StartInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StartInstancesByTag.json) |
| 21 | ACS-ECS-StopInstancesByInstanceIds | 批量的根据实例ID的列表停止ECS实例。执行时会对指定的多个实例执行StopInstance的OpenAPI调用，只有处于运行中状态的ECS实例才能被成功停止。输入包含一个必选参数：ECS实例ID的列表。 | [YAML](PublicTemplates/YAML/ACS-ECS-StopInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StopInstancesByInstanceIds.json) |
| 22 | ACS-ECS-StopInstancesByTag | 批量的根据实例的标签停止ECS实例。执行时会对指定标签下的实例执行StopInstance的OpenAPI调用，只有处于运行中状态的ECS实例才能被成功停止。输入包含两个必选参数：ECS实例的标签键和标签值。 | [YAML](PublicTemplates/YAML/ACS-ECS-StopInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StopInstancesByTag.json) |
| 23 | ACS-ECS-TagInstanceByLinuxKernelVersion | 根据Linux内核版本为指定的ECS实例创建并绑定标签。输入包含两个必选参数：ECS实例ID, 标签键。 | [YAML](PublicTemplates/YAML/ACS-ECS-TagInstanceByLinuxKernelVersion.yml) [JSON](PublicTemplates/JSON/ACS-ECS-TagInstanceByLinuxKernelVersion.json) |
| 24 | ACS-ECS-TagInstanceByOSType | 根据操作系统类型为指定的ECS实例创建并绑定标签。输入包含两个必选参数：ECS实例ID，标签键。 | [YAML](PublicTemplates/YAML/ACS-ECS-TagInstanceByOSType.yml) [JSON](PublicTemplates/JSON/ACS-ECS-TagInstanceByOSType.json) |
| 25 | ACS-ECS-TagInstanceByRunCommandResult | 执行云助手命令，并根据命令返回结果为指定的ECS实例创建并绑定标签。输入包含三个必选参数：ECS实例ID，标签键，云助手命令。 | [YAML](PublicTemplates/YAML/ACS-ECS-TagInstanceByRunCommandResult.yml) [JSON](PublicTemplates/JSON/ACS-ECS-TagInstanceByRunCommandResult.json) |
| 26 | ACS-ECS-UpdateImage | 自动更新镜像，具体逻辑为：从源镜像创建ECS实例，对新生成的实例执行云助手命令，从新实例创建新ECS镜像，最后删除新实例。输入包含七个必选参数：源镜像ID，ECS实例类型，安全组ID，交换机vSwitch ID，云助手命令内容，云助手命令类型，新镜像的名称。 | [YAML](PublicTemplates/YAML/ACS-ECS-UpdateImage.yml) [JSON](PublicTemplates/JSON/ACS-ECS-UpdateImage.json) |

## 云产品动作
### DingTalk
| 序号   | 名称           | 描述（用途）                     | 链接         |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS::Approve::DingTalkWebhook | 通过 WebHook 发送通知到钉钉，以进行审批。执行会一直处于暂停状态，待同意或拒绝后，执行会继续或终止。详情请参考 https://open-doc.dingtalk.com/microapp/serverapi2/qf2nxq 。 | [YAML](CloudProductActions/DingTalk/YAML/ACS::Approve::DingTalkWebhook.yml) [JSON](CloudProductActions/DingTalk/JSON/ACS::Approve::DingTalkWebhook.json) |
| 2 | ACS::Notify::DingTalkWebhook | 通过 WebHook 发送通知到钉钉。详情请参考 https://open-doc.dingtalk.com/microapp/serverapi2/qf2nxq 。 | [YAML](CloudProductActions/DingTalk/YAML/ACS::Notify::DingTalkWebhook.yml) [JSON](CloudProductActions/DingTalk/JSON/ACS::Notify::DingTalkWebhook.json) |

### ECS
| 序号   | 名称           | 描述（用途）                     | 链接         |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS::ECS::AllocatePublicIpAddress | 为一台实例分配一个公网IP地址。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::AllocatePublicIpAddress.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::AllocatePublicIpAddress.json) |
| 2 | ACS::ECS::AttachDisk | 安装磁盘。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::AttachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::AttachDisk.json) |
| 3 | ACS::ECS::CreateAndAttachDisk | 创建并且安装磁盘。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateAndAttachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateAndAttachDisk.json) |
| 4 | ACS::ECS::CreateAndAttachNetworkInterface | 创建并安装网卡。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateAndAttachNetworkInterface.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateAndAttachNetworkInterface.json) |
| 5 | ACS::ECS::CreateImage | 创建镜像。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateImage.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateImage.json) |
| 6 | ACS::ECS::CreateSnapshot | 创建快照。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateSnapshot.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateSnapshot.json) |
| 7 | ACS::ECS::DeleteImage | 删除镜像。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DeleteImage.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DeleteImage.json) |
| 8 | ACS::ECS::DeleteInstance | 删除一个ECS实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DeleteInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DeleteInstance.json) |
| 9 | ACS::ECS::DescribeInstancesByName | 根据实例名称查询实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByName.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByName.json) |
| 10 | ACS::ECS::DescribeInstancesByStatus | 根据实例状态查询实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByStatus.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByStatus.json) |
| 11 | ACS::ECS::DescribeInstancesByTag | 根据Tag查询实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByTag.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByTag.json) |
| 12 | ACS::ECS::DetachDisk | 卸载磁盘。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DetachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DetachDisk.json) |
| 13 | ACS::ECS::InstallCloudAssistant | 安装云助手。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::InstallCloudAssistant.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::InstallCloudAssistant.json) |
| 14 | ACS::ECS::InstallLogtail | 安装日志服务。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::InstallLogtail.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::InstallLogtail.json) |
| 15 | ACS::ECS::ModifyInstanceVpcAttribute | 修改一台ECS实例的专有网络 VPC 属性。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyInstanceVpcAttribute.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyInstanceVpcAttribute.json) |
| 16 | ACS::ECS::ModifyPrepaySpec | 升级或者降低预付费实例规格。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyPrepaySpec.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyPrepaySpec.json) |
| 17 | ACS::ECS::ModifyVncPassword | 修改一台 ECS 实例VNC密码。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyVncPassword.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyVncPassword.json) |
| 18 | ACS::ECS::ReInitDisk | 初始化云盘。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ReInitDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ReInitDisk.json) |
| 19 | ACS::ECS::RebootInstance | 重启一个ECS实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RebootInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RebootInstance.json) |
| 20 | ACS::ECS::ReplaceSystemDisk | 更换系统盘。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ReplaceSystemDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ReplaceSystemDisk.json) |
| 21 | ACS::ECS::ResetDisk | 回滚磁盘。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResetDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResetDisk.json) |
| 22 | ACS::ECS::ResetPassword | 修改一台 ECS 实例的密码。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResetPassword.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResetPassword.json) |
| 23 | ACS::ECS::ResizeDisk | 扩容一块数据盘。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResizeDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResizeDisk.json) |
| 24 | ACS::ECS::RunCommand | 执行远程命令。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunCommand.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunCommand.json) |
| 25 | ACS::ECS::RunInstances | 启动一个或多个ECS实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunInstances.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunInstances.json) |
| 26 | ACS::ECS::RunInstancesFromTemplate | 根据启动模板创建ECS实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunInstancesFromTemplate.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunInstancesFromTemplate.json) |
| 27 | ACS::ECS::StartInstance | 启动一个ECS实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::StartInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::StartInstance.json) |
| 28 | ACS::ECS::StopInstance | 停止一个ECS实例。 | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::StopInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::StopInstance.json) |

### FC
| 序号   | 名称           | 描述（用途）                     | 链接         |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS::FC::InvokeFunction | 调用function。 | [YAML](CloudProductActions/FC/YAML/ACS::FC::InvokeFunction.yml) [JSON](CloudProductActions/FC/JSON/ACS::FC::InvokeFunction.json) |

### RDS
| 序号   | 名称           | 描述（用途）                     | 链接         |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS::RDS::CreateBackup | 为数据库实例创建一个备份集。 | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateBackup.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateBackup.json) |
| 2 | ACS::RDS::CreateDatabase | 创建关系型数据库。 | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateDatabase.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateDatabase.json) |
| 3 | ACS::RDS::CreateDbInstance | 创建数据库实例。 | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateDbInstance.json) |
| 4 | ACS::RDS::DeleteDbInstance | 删除数据库实例。 | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::DeleteDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::DeleteDbInstance.json) |
| 5 | ACS::RDS::RecoveryDbInstance | 将数据库恢复到一个已存在或新的数据库实例上。 | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::RecoveryDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::RecoveryDbInstance.json) |
| 6 | ACS::RDS::RestartDbInstance | 重启数据库实例。 | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::RestartDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::RestartDbInstance.json) |
| 7 | ACS::RDS::UpgradeDbInstanceEngineVersion | 升级数据库版本。 | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::UpgradeDbInstanceEngineVersion.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::UpgradeDbInstanceEngineVersion.json) |


# English
This repository contains examples and best practices for building OOS templates.

## Introduction
The Operation Orchestration Service (OOS) is a comprehensive cloud-based automated O&M platform that provides management and execution of O&M tasks.
Typical usage scenarios include event-driven O&M, batch O&M, scheduled O&M tasks, and cross-regional O&M. 
OOS provides approval, notification, and other functions for some important O&M scenarios.
By using OOS, you can also achieve the goal of standardized O&M tasks, thus practicing the advanced concept of Operations as Code.
OOS supports cross-product use, you can use OOS to manage cloud products such as ECS, RDS, SLB, VPC and so on.

## Public Templates
| No.   | Name           | Description                     | Links        |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS-ECS-BulkyDeletePrepaidInstanceByInstanceIds | Bukly delete prepaid instances by instance IDs.The specified ECS instances must be in stopped status. | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyDeletePrepaidInstanceByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyDeletePrepaidInstanceByInstanceIds.json) |
| 2 | ACS-ECS-BulkyInstallLogAgentByInstanceIds | Installs SLS agent on ECS instances by specifying instance IDs. | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyInstallLogAgentByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyInstallLogAgentByInstanceIds.json) |
| 3 | ACS-ECS-BulkyInstallLogAgentByTag | Installs SLS agent on ECS instances by specifying tag. | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyInstallLogAgentByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyInstallLogAgentByTag.json) |
| 4 | ACS-ECS-BulkyRunCommandByTag | Run command on ECS instances by specifying tag. | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyRunCommandByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyRunCommandByTag.json) |
| 5 | ACS-ECS-BulkyTagInstanceByLinuxKernelVersionAndInstanceIds | Bulky tag ECS instances using Linux kernel version as tag value by specifying instance IDs. | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyTagInstanceByLinuxKernelVersionAndInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyTagInstanceByLinuxKernelVersionAndInstanceIds.json) |
| 6 | ACS-ECS-BulkyTagInstanceByOSTypeAndInstanceIds | Bulky tag ECS instances using OS type as tag value by specifying instance IDs. | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyTagInstanceByOSTypeAndInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyTagInstanceByOSTypeAndInstanceIds.json) |
| 7 | ACS-ECS-BulkyTagInstanceByRunCommandResultAndInstanceIds | Bulky tag ECS instances using RunCommand invocation result as tag value. | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyTagInstanceByRunCommandResultAndInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyTagInstanceByRunCommandResultAndInstanceIds.json) |
| 8 | ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds | Upgrades internet bandwidth of ECS instances. | [YAML](PublicTemplates/YAML/ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BulkyUpgradeInternetBandwidthByInstanceIds.json) |
| 9 | ACS-ECS-BuyCostlyInstancesWithApproval | Creates one or more ECS instances with approval. | [YAML](PublicTemplates/YAML/ACS-ECS-RunInstancesWithApproval.yml) [JSON](PublicTemplates/JSON/ACS-ECS-BuyCostlyInstancesWithApproval.json) |
| 10 | ACS-ECS-CloneInstancesAcrossAZ | Cross available zone copy and run ECS instance of same InstanceType by InstanceIds. | [YAML](PublicTemplates/YAML/ACS-ECS-CloneInstancesAcrossAZ.yml) [JSON](PublicTemplates/JSON/ACS-ECS-CloneInstancesAcrossAZ.json) |
| 11 | ACS-ECS-CloneInstancesAcrossRegion | Cross Region copy and run ECS instance by InstanceIds. | [YAML](PublicTemplates/YAML/ACS-ECS-CloneInstancesAcrossRegion.yml) [JSON](PublicTemplates/JSON/ACS-ECS-CloneInstancesAcrossRegion.json) |
| 12 | ACS-ECS-DeleteInstancesWithApprovalByInstanceIds | Deletes the ECS instances with approval. | [YAML](PublicTemplates/YAML/ACS-ECS-DeleteInstancesWithApprovalByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-DeleteInstancesWithApprovalByInstanceIds.json) |
| 13 | ACS-ECS-RebootInstancesByInstanceIds | Restarts the ECS instances by specifying instance IDs. The specified ECS instances should be in running status. | [YAML](PublicTemplates/YAML/ACS-ECS-RebootInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-RebootInstancesByInstanceIds.json) |
| 14 | ACS-ECS-RebootInstancesByTag | Restarts the ECS instances by specifying tag. The specified ECS instances should be in running status. | [YAML](PublicTemplates/YAML/ACS-ECS-RebootInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-RebootInstancesByTag.json) |
| 15 | ACS-ECS-ScheduleToRebootInstancesByTag | Schedules to reboot the ECS instances by specifying tag. | [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToRebootInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToRebootInstancesByTag.json) |
| 16 | ACS-ECS-ScheduleToStartInstancesByTag | Schedules to start the ECS instances by specifying tag. | [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToStartInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToStartInstancesByTag.json) |
| 17 | ACS-ECS-ScheduleToStopInstancesByTag | Schedules to stop the ECS instances by specifying tag. | [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToStopInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToStopInstancesByTag.json) |
| 18 | ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds | Schedules to upgrade internet bandwidth for ECS instances. | [YAML](PublicTemplates/YAML/ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-ScheduleToUpgradeInternetBandwidthByInstanceIds.json) |
| 19 | ACS-ECS-StartInstancesByInstanceIds | Starts the ECS instances by specifying ECS instance IDs. The specified ECS instances should be in stopped status. | [YAML](PublicTemplates/YAML/ACS-ECS-StartInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StartInstancesByInstanceIds.json) |
| 20 | ACS-ECS-StartInstancesByTag | Starts the ECS instances by specifying tag. The specified ECS instances should be in stopped status. | [YAML](PublicTemplates/YAML/ACS-ECS-StartInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StartInstancesByTag.json) |
| 21 | ACS-ECS-StopInstancesByInstanceIds | Stops the ECS instances by specifying instance IDs. The specified ECS instances should be in running status. | [YAML](PublicTemplates/YAML/ACS-ECS-StopInstancesByInstanceIds.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StopInstancesByInstanceIds.json) |
| 22 | ACS-ECS-StopInstancesByTag | Stops the ECS instances by specifying tag. The specified ECS instances should be in running status. | [YAML](PublicTemplates/YAML/ACS-ECS-StopInstancesByTag.yml) [JSON](PublicTemplates/JSON/ACS-ECS-StopInstancesByTag.json) |
| 23 | ACS-ECS-TagInstanceByLinuxKernelVersion | Tag an ECS instance using Linux kernel version as tag value. | [YAML](PublicTemplates/YAML/ACS-ECS-TagInstanceByLinuxKernelVersion.yml) [JSON](PublicTemplates/JSON/ACS-ECS-TagInstanceByLinuxKernelVersion.json) |
| 24 | ACS-ECS-TagInstanceByOSType | Tag an ECS instance using OS type as tag value. | [YAML](PublicTemplates/YAML/ACS-ECS-TagInstanceByOSType.yml) [JSON](PublicTemplates/JSON/ACS-ECS-TagInstanceByOSType.json) |
| 25 | ACS-ECS-TagInstanceByRunCommandResult | Tag a Linux ECS using RunCommand invocation result as tag value. | [YAML](PublicTemplates/YAML/ACS-ECS-TagInstanceByRunCommandResult.yml) [JSON](PublicTemplates/JSON/ACS-ECS-TagInstanceByRunCommandResult.json) |
| 26 | ACS-ECS-UpdateImage | Updates an existing ECS image via ECS Cloud Assistant then creates a ECS image. | [YAML](PublicTemplates/YAML/ACS-ECS-UpdateImage.yml) [JSON](PublicTemplates/JSON/ACS-ECS-UpdateImage.json) |

## Cloud Product Actions
### DingTalk
| No.   | Name           | Description                     | Links        |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS::Approve::DingTalkWebhook | Sends notification to DingTalk via webhook for asking approval. The execution remains paused until approved or rejected. Please refer https://open-doc.dingtalk.com/microapp/serverapi2/qf2nxq for details. | [YAML](CloudProductActions/DingTalk/YAML/ACS::Approve::DingTalkWebhook.yml) [JSON](CloudProductActions/DingTalk/JSON/ACS::Approve::DingTalkWebhook.json) |
| 2 | ACS::Notify::DingTalkWebhook | Sends notification to DingTalk via webhook. Please refer https://open-doc.dingtalk.com/microapp/serverapi2/qf2nxq for details. | [YAML](CloudProductActions/DingTalk/YAML/ACS::Notify::DingTalkWebhook.yml) [JSON](CloudProductActions/DingTalk/JSON/ACS::Notify::DingTalkWebhook.json) |

### ECS
| No.   | Name           | Description                     | Links        |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS::ECS::AllocatePublicIpAddress | Assigns a public IP address to an instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::AllocatePublicIpAddress.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::AllocatePublicIpAddress.json) |
| 2 | ACS::ECS::AttachDisk | Attaches a data disk to an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::AttachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::AttachDisk.json) |
| 3 | ACS::ECS::CreateAndAttachDisk | Creates a disk and attaches a data disk to an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateAndAttachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateAndAttachDisk.json) |
| 4 | ACS::ECS::CreateAndAttachNetworkInterface | Creates an elastic network interface (ENI) and attaches to an instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateAndAttachNetworkInterface.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateAndAttachNetworkInterface.json) |
| 5 | ACS::ECS::CreateImage | Creates a custom image. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateImage.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateImage.json) |
| 6 | ACS::ECS::CreateSnapshot | Creates a snapshot for a disk. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::CreateSnapshot.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::CreateSnapshot.json) |
| 7 | ACS::ECS::DeleteImage | Deletes ECS image by specifying imageId. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DeleteImage.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DeleteImage.json) |
| 8 | ACS::ECS::DeleteInstance | Deletes ECS instance by specifying instance ID. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DeleteInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DeleteInstance.json) |
| 9 | ACS::ECS::DescribeInstancesByName | Views the ECS instances by specifying instance name. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByName.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByName.json) |
| 10 | ACS::ECS::DescribeInstancesByStatus | Views the ECS instances by specifying instance status. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByStatus.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByStatus.json) |
| 11 | ACS::ECS::DescribeInstancesByTag | Views the ECS instances by specifying tag. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DescribeInstancesByTag.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DescribeInstancesByTag.json) |
| 12 | ACS::ECS::DetachDisk | Detaches a disk from an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::DetachDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::DetachDisk.json) |
| 13 | ACS::ECS::InstallCloudAssistant | Installs cloud assistant on ECS instance by specifying instanceId. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::InstallCloudAssistant.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::InstallCloudAssistant.json) |
| 14 | ACS::ECS::InstallLogtail | Installs SLS agent on ECS instance by running a cloud assistant command. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::InstallLogtail.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::InstallLogtail.json) |
| 15 | ACS::ECS::ModifyInstanceVpcAttribute | Modifies the VPC attributes of an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyInstanceVpcAttribute.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyInstanceVpcAttribute.json) |
| 16 | ACS::ECS::ModifyPrepaySpec | Changes the type of your subscription instance. The new instance type will take effect for the entire lifecycle of the instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyPrepaySpec.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyPrepaySpec.json) |
| 17 | ACS::ECS::ModifyVncPassword | Modifies the Web management terminal password of an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ModifyVncPassword.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ModifyVncPassword.json) |
| 18 | ACS::ECS::ReInitDisk | Resets a disk to its initial status.The specified ECS instances should be in stopped status. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ReInitDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ReInitDisk.json) |
| 19 | ACS::ECS::RebootInstance | Restarts the ECS instance by specifying instanceId. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RebootInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RebootInstance.json) |
| 20 | ACS::ECS::ReplaceSystemDisk | Replaces the system disk of an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ReplaceSystemDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ReplaceSystemDisk.json) |
| 21 | ACS::ECS::ResetDisk | Rolls back a disk to the specific disk status by using one of its snapshots. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResetDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResetDisk.json) |
| 22 | ACS::ECS::ResetPassword | Resets password of an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResetPassword.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResetPassword.json) |
| 23 | ACS::ECS::ResizeDisk | Extends the size of a cloud disk. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::ResizeDisk.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::ResizeDisk.json) |
| 24 | ACS::ECS::RunCommand | Creates a cloud assistant command and triggers it on one ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunCommand.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunCommand.json) |
| 25 | ACS::ECS::RunInstances | Creates one or more ECS instances. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunInstances.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunInstances.json) |
| 26 | ACS::ECS::RunInstancesFromTemplate | Creates one or more instances by specifying launch template. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::RunInstancesFromTemplate.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::RunInstancesFromTemplate.json) |
| 27 | ACS::ECS::StartInstance | Starts an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::StartInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::StartInstance.json) |
| 28 | ACS::ECS::StopInstance | Stops an ECS instance. | [YAML](CloudProductActions/ECS/YAML/ACS::ECS::StopInstance.yml) [JSON](CloudProductActions/ECS/JSON/ACS::ECS::StopInstance.json) |

### FC
| No.   | Name           | Description                     | Links        |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS::FC::InvokeFunction | Invoke Created Function. | [YAML](CloudProductActions/FC/YAML/ACS::FC::InvokeFunction.yml) [JSON](CloudProductActions/FC/JSON/ACS::FC::InvokeFunction.json) |

### RDS
| No.   | Name           | Description                     | Links        |
| ----- | -------------- | ------------------------------- | ------------ |
| 1 | ACS::RDS::CreateBackup | Creates backups of a RDS instance. | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateBackup.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateBackup.json) |
| 2 | ACS::RDS::CreateDatabase | Creates a new database in an instance. | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateDatabase.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateDatabase.json) |
| 3 | ACS::RDS::CreateDbInstance | Creates an RDS instance. | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::CreateDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::CreateDbInstance.json) |
| 4 | ACS::RDS::DeleteDbInstance | Deletes DB instance. | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::DeleteDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::DeleteDbInstance.json) |
| 5 | ACS::RDS::RecoveryDbInstance | Recoveries database to an existed or new instance. | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::RecoveryDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::RecoveryDbInstance.json) |
| 6 | ACS::RDS::RestartDbInstance | Restarts an RDS instance. | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::RestartDbInstance.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::RestartDbInstance.json) |
| 7 | ACS::RDS::UpgradeDbInstanceEngineVersion | Upgrades the database version of an instance. | [YAML](CloudProductActions/RDS/YAML/ACS::RDS::UpgradeDbInstanceEngineVersion.yml) [JSON](CloudProductActions/RDS/JSON/ACS::RDS::UpgradeDbInstanceEngineVersion.json) |
