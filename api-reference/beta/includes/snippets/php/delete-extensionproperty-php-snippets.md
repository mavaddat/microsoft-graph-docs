---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$graphServiceClient->applications()->byApplicationId('application-id')->extensionProperties()->byExtensionPropertyId('extensionProperty-id')->delete()->wait();

```