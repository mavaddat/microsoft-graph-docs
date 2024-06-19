---
title: "cloudPC resource type"
description: "Represents a cloud-managed virtual desktop."
author: "AshleyYangSZ"
ms.localizationpriority: medium
ms.subservice: "cloud-pc"
doc_type: resourcePageType
---

# cloudPC resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a cloud-managed virtual desktop. This Cloud PC is also enrolled in Intune and managed through the Microsoft Endpoint Manager portal, so the Cloud PC also has a corresponding Intune-managed device ID.

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List cloudPCs](../api/virtualendpoint-list-cloudpcs.md)|[cloudPC](../resources/cloudpc.md) collection|List properties and relationships of the Cloud PC objects.|
|[Get cloudPC](../api/cloudpc-get.md)|[cloudPC](../resources/cloudpc.md)|Read the properties and relationships of a Cloud PC object.|
|[Get provisioned Cloud PCs](../api/cloudpc-getprovisionedcloudpcs.md)|[cloudPC](../resources/cloudpc.md) collection|Get all provisioned Cloud PCs of a specific service plan for users under a Microsoft Entra user group.|
|[Change user account type](../api/cloudpc-changeuseraccounttype.md)|None|Change the account type of the user on a specific Cloud PC.|
|[End grace period](../api/cloudpc-endgraceperiod.md)|None|End the grace period for a Cloud PC object.|
|[Get remote action results](../api/manageddevice-getcloudpcremoteactionresults.md)|[cloudPcRemoteActionResult](../resources/cloudpcremoteactionresult.md)|Check the [Cloud PC-specified remote action results](../resources/cloudpcremoteactionresult.md) for a Cloud PC device.|
|[Power on](../api/cloudpc-poweron.md)|None|Power on a specific Windows Frontline Cloud PC object. This action supports MEM admin scenarios.|
|[Power off](../api/cloudpc-poweroff.md)|None|Power off a specific  Windows Frontline Cloud PC object. This action supports MEM admin scenarios.|
|[Reboot](../api/cloudpc-reboot.md)|None|Reboot a specific Cloud PC object.|
|[Rename](../api/cloudpc-rename.md)|None|Rename a specific Cloud PC object. Use this API to update the **displayName** for the Cloud PC entity.|
|[Reprovision](../api/cloudpc-reprovision.md)|None|Reprovision a Cloud PC object.|
|[Resize](../api/cloudpc-resize.md)|None|Upgrade or downgrade an existing Cloud PC to a configuration with a new virtual CPU (vCPU) and storage size.|
|[Start](../api/cloudpc-start.md)|None|Start a specific Cloud PC for a user. Currently, only Windows 365 Frontline Cloud PCs are supported. |
|[Stop](../api/cloudpc-stop.md)|None|Stop a specific Cloud PC for a user. Currently, only Windows 365 Frontline Cloud PCs are supported. |
|[Troubleshoot](../api/cloudpc-troubleshoot.md)|None|Troubleshoot a specific Cloud PC object. Use this API to check the health status of the Cloud PC and the session host.|
|[Restore](../api/cloudpc-restore.md)|None|Restore a Cloud PC object to a previous state from a snapshot.|
|[Set review status](../api/cloudpc-setreviewstatus.md)|None|Set the review status of a specific Cloud PC device using the Cloud PC ID.|
|[Retrieve review status](../api/cloudpc-retrievereviewstatus.md)|[cloudPcReviewStatus](../resources/cloudpcreviewstatus.md)|Get the [review status](..\resources\cloudpcreviewstatus.md) of a Cloud PC.|
|[Bulk set review status](../api/manageddevice-bulksetcloudpcreviewstatus.md)|[cloudPcBulkRemoteActionResult](../resources/cloudpcbulkremoteactionresult.md)|Set the review status of multiple Cloud PC devices with a single request that includes the IDs of Intune managed devices.|
|[List for user](../api/user-list-cloudpcs.md)|[cloudPC](../resources/cloudpc.md) collection|List the Cloud PC devices that are attributed to the signed-in user.|
|[Get launch info for user](../api/cloudpc-getcloudpclaunchinfo.md)|[cloudPcLaunchInfo](../resources/cloudpclaunchinfo.md)|Get the [cloudPcLaunchInfo](../resources/cloudpclaunchinfo.md) for the signed-in user.|
|[Get connectivity history](../api/cloudpc-getcloudpcconnectivityhistory.md)|[cloudPcConnectivityEvent](../resources/cloudpcconnectivityevent.md) collection|Get the Cloud PC connectivity history.|
|[Get supported remote actions](../api/cloudpc-getsupportedcloudpcremoteactions.md)|[cloudPcRemoteActionCapability](../resources/cloudpcremoteactioncapability.md) collection|Get a list of supported Cloud PC remote actions for a specific Cloud PC device, including the action names and capabilities.|
|[Retry partner agent installation](../api/cloudpc-retrypartneragentinstallation.md)|None|Retry installation for the partner agents that failed to install on the Cloud PC.|
|[Validate bulk resize](../api/cloudpc-validatebulkresize.md)|[cloudPcResizeValidateResult](../resources/cloudPcResizeValidationResult.md) collection|Validate that a set of Cloud PC devices meet the requirements to be bulk resized.|
|[Create snapshot](../api/cloudpc-createsnapshot.md)|None|Create a snapshot for a specific Cloud PC device.|
|[Get frontline access state](../api/cloudpc-getfrontlinecloudpcaccessstate.md)|[frontlineCloudPcAccessState](#frontlinecloudpcaccessstate-values)|Get the access state of the frontline Cloud PC. The possible values are: `unassigned`, `noLicensesAvailable`, `activationFailed`, `active`, `activating`, `standbyMode`, `unknownFutureValue`.|
|[Bulk reprovision remote action (deprecated)](../api/manageddevice-bulkreprovisioncloudpc.md) |None|Bulk reprovision a set of Cloud PC devices with Intune managed device IDs. This API is deprecated and stopped returning data on September 24, 2023. Going forward, use the [cloudPcBulkReprovision](../resources/cloudpcbulkreprovision.md) resource. |
|[Bulk resize (deprecated)](../api/cloudpc-bulkresize.md) |[cloudPcRemoteActionResult](../resources//cloudpcremoteactionresult.md) collection|Perform a bulk resize action to resize a group of Cloud PCs that have successfully passed validation (cloudPC: validateBulkResize). If any devices can't be resized, they're labeled as "resize failed", while the remaining devices are `provisioned` for the resize process. This API is deprecated and stopped returning data on September 24, 2023. Going forward, use the [cloudPcBulkResize](../resources/cloudpcbulkresize.md) resource.|
|[Bulk restore remote action (deprecated)](../api/manageddevice-bulkrestorecloudpc.md) |[cloudPcBulkRemoteActionResult](../resources/cloudpcbulkremoteactionresult.md)|Restore multiple Cloud PC devices with a single request that includes the IDs of Intune managed devices and a restore point date and time. This API is deprecated and stopped returning data on September 24, 2023. Going forward, use the [cloudPcBulkRestore](../resources/cloudpcbulkrestore.md) resource.|
|[Get review status (deprecated)](../api/manageddevice-getcloudpcreviewstatus.md) |[cloudPcReviewStatus](../resources/cloudpcreviewstatus.md)|Get the review status of a specific Cloud PC device by managedDeviceId. This API is deprecated and stopped returning data on April 30, 2024. Going forward, use the [cloudPC: retrieveReviewStatus](../api/cloudpc-retrievereviewstatus.md) API.|
|[Get shift work access state (deprecated)](../api/cloudpc-getshiftworkcloudpcaccessstate.md) |[shiftWorkCloudPcAccessState](#shiftworkcloudpcaccessstate-values-deprecated)|Get the access state of the shift work Cloud PC. The possible values are: `unassigned`, `noLicensesAvailable`, `activationFailed`, `active`, `activating`, `waitlisted`, `unknownFutureValue`, `standbyMode`. You must use the `Prefer: include-unknown-enum-members` request header to get the following value in this evolvable enum: `standbyMode`. This API is deprecated and will stop returning data on December 31, 2023. Going forward, use the [getFrontlineCloudPcAccessState](../api/cloudpc-getfrontlinecloudpcaccessstate.md) API.|
|[Reprovision remote action (deprecated)](../api/manageddevice-reprovisioncloudpc.md) |None|Reprovision a Cloud PC with an Intune  [managed device](../resources/cloudpc.md) ID. This API is deprecated and will stop returning data on September 30, 2023. Going forward, use the [reprovision](../api/cloudpc-reprovision.md) API.|
|[Resize remote action (deprecated)](../api/manageddevice-resizecloudpc.md) |None|Upgrade or downgrade an existing Cloud PC to another configuration with a new vCPU and storage size through Intune managed device ID. This API is deprecated and stopped returning data on October 30, 2023. Going forward, use the [cloudPC: resize](../api/cloudpc-resize.md) API.|
|[Restore remote action (deprecated)](../api/manageddevice-restorecloudpc.md) |None|Restore a Cloud PC device to a previous state with an Intune [managed device](../resources/cloudpc.md) ID. This API is deprecated and will stop returning data on September 30, 2023. Going forward, use the [restore](../api/cloudpc-restore.md) API.|
|[Set review status (deprecated)](../api/manageddevice-setcloudpcreviewstatus.md) |None|Set the review status of a specific Cloud PC device using the managed device ID. This API is deprecated and stopped returning data on April 30, 2024. Going forward, use the [cloudPC: setReviewStatus](../api/cloudpc-setreviewstatus.md) API.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|aadDeviceId|String|The Microsoft Entra device ID of the Cloud PC.|
|allotmentDisplayName|String|The allotment name divides tenant licenses into smaller batches or groups that help restrict the number of licenses available for use in a specific assignment. When the **provisioningType** is `dedicated`, the allotment name is `null`. Read-only.|
|connectivityResult|[cloudPcConnectivityResult](../resources/cloudpcconnectivityresult.md)|The connectivity health check result of a Cloud PC, including the updated timestamp and whether the Cloud PC can be connected.|
|deviceRegionName|String|The name of the geographical region where the Cloud PC is currently provisioned. For example, `westus3`, `eastus2`, and `southeastasia`. Read-only.|
|diskEncryptionState|[cloudPcDiskEncryptionState](#cloudpcdiskencryptionstate-values)|The disk encryption applied to the Cloud PC. Possible values: `notAvailable`, `notEncrypted`, `encryptedUsingPlatformManagedKey`, `encryptedUsingCustomerManagedKey`, and `unknownFutureValue`.|
|displayName|String|The display name of the Cloud PC.|
|gracePeriodEndDateTime|DateTimeOffset|The date and time when the grace period ends and reprovisioning or deprovisioning happens. Required only if the status is `inGracePeriod`. The timestamp is shown in ISO 8601 format and Coordinated Universal Time (UTC). For example, midnight UTC on Jan 1, 2014 is `2014-01-01T00:00:00Z`.|
|id|String|The unique identifier for the Cloud PC. Read-only.|
|imageDisplayName|String|Name of the OS image that's on the Cloud PC.|
|lastLoginResult|[cloudPcLoginResult](../resources/cloudpcloginresult.md)|The last login result of the Cloud PC. For example, `{ "time": "2014-01-01T00:00:00Z"}`.|
|lastModifiedDateTime|DateTimeOffset|The last modified date and time of the Cloud PC. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014, is `2014-01-01T00:00:00Z`.|
|lastRemoteActionResult|[cloudPcRemoteActionResult](../resources/cloudpcremoteactionresult.md)|The last remote action result of the enterprise Cloud PCs. The supported remote actions are: `Reboot`, `Rename`, `Reprovision`, `Restore`, `Troubleshoot`.|
|managedDeviceId|String|The Intune device ID of the Cloud PC.|
|managedDeviceName|String|The Intune device name of the Cloud PC.|
|onPremisesConnectionName|String|The Azure network connection that is applied during the provisioning of Cloud PCs.|
|osVersion|[cloudPcOperatingSystem](../resources/cloudpcorganizationsettings.md#cloudpcoperatingsystem-values)|The version of the operating system (OS) to provision on Cloud PCs. Possible values are: `windows10`, `windows11`, `unknownFutureValue`.|
|partnerAgentInstallResults|[cloudPcPartnerAgentInstallResult](../resources/cloudpcpartneragentinstallresult.md) collection|The results of every partner agent's installation status on Cloud PC.|
|powerState|[cloudPcPowerState](#cloudpcpowerstate-values)|The power state of a Cloud PC. The possible values are: `running`, `poweredOff`, `unknown`. This property only supports shift work Cloud PCs.|
|provisioningPolicyId|String|The provisioning policy ID of the Cloud PC.|
|provisioningPolicyName|String|The provisioning policy that is applied during the provisioning of Cloud PCs.|
|provisioningType|[cloudPcProvisioningType](../resources/cloudpcprovisioningpolicy.md#cloudpcprovisioningtype-values)|The type of licenses to be used when provisioning Cloud PCs using this policy. Possible values are: `dedicated`, `shared`, `unknownFutureValue`,`sharedByUser`, `sharedByUser`. You must use the `Prefer: include-unknown-enum-members` request header to get the following values from this [evolvable enum](/graph/best-practices-concept#handling-future-members-in-evolvable-enumerations): `sharedByUser`, `sharedByEntraGroup`. The default value is `dedicated`. CAUTION: The `shared` member is deprecated and will stop returning on April 30, 2027； in the future, use the `sharedByUser` member. |
|servicePlanId|String|The service plan ID of the Cloud PC.|
|servicePlanName|String|The service plan name of the Cloud PC.|
|servicePlanType|[cloudPcServicePlanType](../resources/cloudpcserviceplan.md#cloudpcserviceplantype-values)|The service plan type of the Cloud PC.|
|status|[microsoft.graph.cloudPcStatus](#cloudpcstatus-values)|The status of the Cloud PC. Possible values are: `notProvisioned`, `provisioning`, `provisioned`, `inGracePeriod`, `deprovisioning`, `failed`, `provisionedWithWarnings`, `resizing`, `restoring`, `pendingProvision`, `unknownFutureValue`, `movingRegion`, `resizePendingLicense`. You must use the `Prefer: include-unknown-enum-members` request header to get the following values from this [evolvable enum](/graph/best-practices-concept#handling-future-members-in-evolvable-enumerations): `movingRegion`, `resizePendingLicense`.|
|statusDetails|[cloudPcStatusDetails](../resources/cloudpcstatusdetails.md)|The details of the Cloud PC status.|
|userAccountType|[cloudPcUserAccountType](../resources/cloudpcorganizationsettings.md#cloudpcuseraccounttype-values)|The account type of the user on provisioned Cloud PCs. Possible values are: `standardUser`, `administrator`, `unknownFutureValue`.|
|userPrincipalName|String|The user principal name (UPN) of the user assigned to the Cloud PC.|

### cloudPcDiskEncryptionState values

|Member|Description|
|:---|:---|
|notAvailable|The Cloud PC isn't provisioned or is in a state where encryption isn't available.|
|notEncrypted|The Cloud PC should be encrypted, but the encryption isn't done so yet (reserved, shouldn't happen).|
|encryptedUsingPlatformManagedKey|The Cloud PC is encrypted using a platform-managed key. This member is the default value if the customer-managed key isn't enabled.|
|encryptedUsingCustomerManagedKey|The Cloud PC is encrypted using the customer-managed key.|
|unknownFutureValue|Evolvable enumeration sentinel value. Don't use.|

### cloudPcPowerState values

|Member|Description|
|:---|:---|
|running|The Cloud PC status is running.|
|poweredOff|The Cloud PC status is powered off.|
|unknown|The Cloud PC status is unknown.|

### cloudPcStatus values
The following table lists the members of an [evolvable enumeration](/graph/best-practices-concept#handling-future-members-in-evolvable-enumerations). You must use the `Prefer: include-unknown-enum-members` request header to get the following values in this evolvable enum: `movingRegion`, `resizePendingLicense`.

|Member|Description|
|:---|:---|
|notProvisioned|The Cloud PC hasn't been provisioned yet.|
|provisioning|Cloud PC provisioning is in progress.|
|provisioned|The Cloud PC is provisioned and users can access it.|
|inGracePeriod|The Cloud PC is in the one-week grace period before deprovision.|
|deprovisioning|The Cloud PC is deprovisioning.|
|failed|The operation on Cloud PC failed.|
|provisionedWithWarnings|The Cloud PC is provisioned and end users can access it with some warnings. The user can continue to use this Cloud PC.|
|resizing|The Cloud PC is resizing.|
|pendingProvision|The provisioning is pending on the Cloud PC. In this case, the number of Cloud PCs in the grace period is more than the number of total available licenses. |
|restoring|The Cloud PC is restoring.|
|unknownFutureValue|Evolvable enumeration sentinel value. Don't use.|
|movingRegion|Indicates that the Cloud PC is being moved from one region to another.|
|resizePendingLicense|Indicates that the Cloud PC resize process was initiated but can't be completed because the target license hasn't been identified. It's currently awaiting customer action to resolve the licensing issue.|

### frontlineCloudPcAccessState values

|Member|Description|
|:---|:---|
|unassigned|Set to unassigned if the Cloud PC doesn't consume any shared-use licenses. The default value is `unassigned`.|
|noLicensesAvailable|Indicates that all shared-use licenses are in use.|
|activationFailed|Indicates that the frontline Cloud PC activation failed after the user requested a frontline Cloud PC.|
|active|Indicates that the frontline Cloud PC is in an active state with a shared-use license assigned, and the user can connect to the Cloud PC.|
|activating|Indicates that a user requested to connect the Cloud PC and the service is starting.|
|standbyMode|Indicates that the frontline Cloud PC is in a standby state before it's shut down and deallocated. A frontline Cloud PC in a standby state is still accessible by the user.|
|unknownFutureValue|Evolvable enumeration sentinel value. Don't use.|

### shiftWorkCloudPcAccessState values (deprecated)
The following table lists the members of an [evolvable enumeration](#shiftworkcloudpcaccessstate-values-deprecated). You must use the `Prefer: include-unknown-enum-members` request header to get the following values in this evolvable enum: `standbyMode`.

|Member|Description|
|:---|:---|
|unassigned|Set to unassigned if the Cloud PC isn't consuming any shared-use licenses. The default value is `unassigned`.|
|noLicensesAvailable|Indicates that all shared-use licenses are in use.|
|activationFailed|Indicates that the shift work Cloud PC activation failed after the user requested a shift work Cloud PC.|
|active|Indicates that the shift work Cloud PC is in an active state with a shared-use license assigned, and the user can connect to the Cloud PC.|
|activating|Indicates that a user requested to connect the Cloud PC and the service is starting.|
|waitlisted (deprecated)|Indicates that the shift work Cloud PC is in a waitlisted state after the user requests to connect this Cloud PC and all shared use licenses are being actively used. This value is deprecated and will stop returning on May 17, 2023. |
|unknownFutureValue|Evolvable enumeration sentinel value. Don't use.|
|standbyMode|Indicates that the shift work Cloud PC is in a standby state before it's shut down and deallocated. A shift work Cloud PC in standby state is still accessible by the user.|

## Relationships

None.

## JSON representation

The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.cloudPC",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->

``` json
{
  "@odata.type": "#microsoft.graph.cloudPC",
  "aadDeviceId": "String",
  "allotmentDisplayName": "String",
  "connectivityResult": "String",
  "deviceRegionName": "String",
  "diskEncryptionState": "String",
  "displayName": "String",
  "gracePeriodEndDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "imageDisplayName": "String",
  "lastLoginResult": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "lastRemoteActionResult": "String",
  "managedDeviceId": "String",
  "managedDeviceName": "String",
  "onPremisesConnectionName": "String",
  "powerState": "String",
  "osVersion": "String",
  "partnerAgentInstallResults": "String",
  "provisioningPolicyId": "String",
  "provisioningPolicyName": "String",
  "provisioningType": "String",
  "servicePlanId": "String",
  "servicePlanName": "String",
  "servicePlanType": "String",
  "status": "String",
  "userAccountType": "String",
  "userPrincipalName": "String"
}
```
