---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Chats\Item\Messages\MessagesRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new MessagesRequestBuilderGetRequestConfiguration();
$queryParameters = MessagesRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->top = 2;
$queryParameters->orderby = ["lastModifiedDateTime desc"];
$queryParameters->filter = "lastModifiedDateTime gt 2022-09-22T00:00:00.000Z and lastModifiedDateTime lt 2022-09-24T00:00:00.000Z";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->chats()->byChatId('chat-id')->messages()->get($requestConfiguration)->wait();

```