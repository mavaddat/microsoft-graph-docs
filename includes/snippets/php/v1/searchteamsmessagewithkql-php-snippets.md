---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Search\Query\QueryPostRequestBody;
use Microsoft\Graph\Generated\Models\SearchRequest;
use Microsoft\Graph\Generated\Models\EntityType;
use Microsoft\Graph\Generated\Models\SearchQuery;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new QueryPostRequestBody();
$requestsSearchRequest1 = new SearchRequest();
$requestsSearchRequest1->setEntityTypes([new EntityType('chatMessage'),	]);
$requestsSearchRequest1Query = new SearchQuery();
$requestsSearchRequest1Query->setQueryString('contoso from:bob to:alice sent>2022-07-14');
$requestsSearchRequest1->setQuery($requestsSearchRequest1Query);
$requestsSearchRequest1->setFrom(0);
$requestsSearchRequest1->setSize(15);
$requestsSearchRequest1->setEnableTopResults(true);
$requestsArray []= $requestsSearchRequest1;
$requestBody->setRequests($requestsArray);


$result = $graphServiceClient->search()->query()->post($requestBody)->wait();

```