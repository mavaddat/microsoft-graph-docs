---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$graphServiceClient->networkAccess()->filteringProfiles()->byFilteringProfileId('filteringProfile-id')->policies()->byPolicyLinkId('policyLink-id')->delete()->wait();

```