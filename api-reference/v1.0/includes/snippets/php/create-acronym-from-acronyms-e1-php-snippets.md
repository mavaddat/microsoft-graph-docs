---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Search\Acronym;
use Microsoft\Graph\Generated\Models\Search\AnswerState;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Acronym();
$requestBody->setDisplayName('DNN');
$requestBody->setStandsFor('Deep Neural Network');
$requestBody->setDescription('A deep neural network is a neural network with a certain level of complexity, a neural network with more than two layers.');
$requestBody->setWebUrl('http://microsoft.com/deep-neural-network');
$requestBody->setState(new AnswerState('draft'));

$result = $graphServiceClient->search()->acronyms()->post($requestBody)->wait();

```