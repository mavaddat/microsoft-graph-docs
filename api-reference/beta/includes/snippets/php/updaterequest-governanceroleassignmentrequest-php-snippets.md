---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$result = $graphServiceClient->privilegedAccess()->byPrivilegedAccessId('privilegedAccess-id')->roleAssignmentRequests()->byGovernanceRoleAssignmentRequestId('governanceRoleAssignmentRequest-id')->updateRequest()->post()->wait();

```