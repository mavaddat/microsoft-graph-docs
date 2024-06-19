---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\EmployeeExperience\Goals\ExportJobs\ExportJobsRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new ExportJobsRequestBuilderGetRequestConfiguration();
$queryParameters = ExportJobsRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = " goalsOrganizationId eq '3d9a8150-90fd-42bd-9777-25ba783d4a05'";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->employeeExperience()->goals()->exportJobs()->get($requestConfiguration)->wait();

```