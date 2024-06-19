---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\M365AppsInstallationOptions;
use Microsoft\Graph\Beta\Generated\Models\AppsUpdateChannelType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new M365AppsInstallationOptions();
$requestBody->setUpdateChannel(new AppsUpdateChannelType('current'));

$result = $graphServiceClient->admin()->microsoft365Apps()->installationOptions()->patch($requestBody)->wait();

```