---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\TeamsAppInstallation;
use Microsoft\Graph\Generated\Models\TeamsAppPermissionSet;
use Microsoft\Graph\Generated\Models\TeamsAppResourceSpecificPermission;
use Microsoft\Graph\Generated\Models\TeamsAppResourceSpecificPermissionType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new TeamsAppInstallation();
$consentedPermissionSet = new TeamsAppPermissionSet();
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission1 = new TeamsAppResourceSpecificPermission();
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission1->setPermissionValue('OnlineMeeting.ReadBasic.Chat');
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission1->setPermissionType(new TeamsAppResourceSpecificPermissionType('delegated'));
$resourceSpecificPermissionsArray []= $resourceSpecificPermissionsTeamsAppResourceSpecificPermission1;
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission2 = new TeamsAppResourceSpecificPermission();
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission2->setPermissionValue('OnlineMeetingIncomingAudio.Detect.Chat');
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission2->setPermissionType(new TeamsAppResourceSpecificPermissionType('delegated'));
$resourceSpecificPermissionsArray []= $resourceSpecificPermissionsTeamsAppResourceSpecificPermission2;
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission3 = new TeamsAppResourceSpecificPermission();
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission3->setPermissionValue('ChatMember.Read.Chat');
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission3->setPermissionType(new TeamsAppResourceSpecificPermissionType('application'));
$resourceSpecificPermissionsArray []= $resourceSpecificPermissionsTeamsAppResourceSpecificPermission3;
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission4 = new TeamsAppResourceSpecificPermission();
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission4->setPermissionValue('ChatMessage.Read.Chat');
$resourceSpecificPermissionsTeamsAppResourceSpecificPermission4->setPermissionType(new TeamsAppResourceSpecificPermissionType('application'));
$resourceSpecificPermissionsArray []= $resourceSpecificPermissionsTeamsAppResourceSpecificPermission4;
$consentedPermissionSet->setResourceSpecificPermissions($resourceSpecificPermissionsArray);

$requestBody->setConsentedPermissionSet($consentedPermissionSet);
$additionalData = [
'teamsApp@odata.bind' => 'https://graph.microsoft.com/v1.0/appCatalogs/teamsApps/2b524e28-95ce-4c9b-9773-4a5bd6ec1770',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->chats()->byChatId('chat-id')->installedApps()->post($requestBody)->wait();

```