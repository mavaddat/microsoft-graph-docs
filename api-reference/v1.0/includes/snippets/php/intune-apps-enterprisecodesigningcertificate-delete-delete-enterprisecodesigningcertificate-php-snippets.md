---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);


$graphServiceClient->deviceAppManagement()->enterpriseCodeSigningCertificates()->byEnterpriseCodeSigningCertificateId('enterpriseCodeSigningCertificate-id')->delete()->wait();

```