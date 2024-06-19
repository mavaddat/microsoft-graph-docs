---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Search\Query\QueryPostRequestBody;
use Microsoft\Graph\Beta\Generated\Models\SearchRequest;
use Microsoft\Graph\Beta\Generated\Models\EntityType;
use Microsoft\Graph\Beta\Generated\Models\SearchQuery;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new QueryPostRequestBody();
$requestsSearchRequest1 = new SearchRequest();
$requestsSearchRequest1->setEntityTypes([new EntityType('chatMessage'),	]);
$requestsSearchRequest1Query = new SearchQuery();
$requestsSearchRequest1Query->setQueryString('test');
$requestsSearchRequest1->setQuery($requestsSearchRequest1Query);
$requestsSearchRequest1->setFrom(0);
$requestsSearchRequest1->setSize(25);
$requestsArray []= $requestsSearchRequest1;
$requestBody->setRequests($requestsArray);


$result = $graphServiceClient->search()->query()->post($requestBody)->wait();

```