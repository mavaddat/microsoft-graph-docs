---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Search\Bookmark;
use Microsoft\Graph\Generated\Models\Search\AnswerKeyword;
use Microsoft\Graph\Generated\Models\Search\AnswerState;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Bookmark();
$requestBody->setDisplayName('Contoso Install Site');
$requestBody->setWebUrl('http://www.contoso.com/');
$requestBody->setDescription('Try or buy Contoso for Home or Business and view product information');
$keywords = new AnswerKeyword();
$keywords->setKeywords(['Contoso', 'install', 	]);
$keywords->setReservedKeywords(['Contoso', 	]);
$keywords->setMatchSimilarKeywords(true);
$requestBody->setKeywords($keywords);
$requestBody->setState(new AnswerState('published'));

$result = $graphServiceClient->search()->bookmarks()->post($requestBody)->wait();

```