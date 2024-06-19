---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\ServicePrincipals\Item\Synchronization\Jobs\Item\ProvisionOnDemand\ProvisionOnDemandPostRequestBody;
use Microsoft\Graph\Generated\Models\SynchronizationJobApplicationParameters;
use Microsoft\Graph\Generated\Models\SynchronizationJobSubject;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ProvisionOnDemandPostRequestBody();
$parametersSynchronizationJobApplicationParameters1 = new SynchronizationJobApplicationParameters();
$parametersSynchronizationJobApplicationParameters1->setRuleId('6c409270-f78a-4bc6-af23-7cf3ab6482fe');
$subjectsSynchronizationJobSubject1 = new SynchronizationJobSubject();
$subjectsSynchronizationJobSubject1->setObjectId('CN=AdeleV,CN=Users,DC=corp,DC=chicago,DC=com');
$subjectsSynchronizationJobSubject1->setObjectTypeName('user');
$subjectsArray []= $subjectsSynchronizationJobSubject1;
$parametersSynchronizationJobApplicationParameters1->setSubjects($subjectsArray);

$parametersArray []= $parametersSynchronizationJobApplicationParameters1;
$requestBody->setParameters($parametersArray);


$result = $graphServiceClient->servicePrincipals()->byServicePrincipalId('servicePrincipal-id')->synchronization()->jobs()->bySynchronizationJobId('synchronizationJob-id')->provisionOnDemand()->post($requestBody)->wait();

```