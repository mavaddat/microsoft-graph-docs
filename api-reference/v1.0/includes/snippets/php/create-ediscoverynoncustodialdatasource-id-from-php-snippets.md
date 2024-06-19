---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Security\EdiscoveryNoncustodialDataSource;
use Microsoft\Graph\Generated\Models\Security\SiteSource;
use Microsoft\Graph\Generated\Models\Site;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EdiscoveryNoncustodialDataSource();
$dataSource = new SiteSource();
$dataSource->setOdataType('microsoft.graph.security.siteSource');
$dataSourceSite = new Site();
$dataSourceSite->setWebUrl('https://m365x809305.sharepoint.com/sites/Design-topsecret');
$dataSource->setSite($dataSourceSite);
$requestBody->setDataSource($dataSource);

$result = $graphServiceClient->security()->cases()->ediscoveryCases()->byEdiscoveryCaseId('ediscoveryCase-id')->noncustodialDataSources()->post($requestBody)->wait();

```