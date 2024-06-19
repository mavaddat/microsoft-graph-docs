---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Channel;
use Microsoft\Graph\Beta\Generated\Models\ChannelMembershipType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Channel();
$requestBody->setDisplayName('Architecture Discussion');
$requestBody->setDescription('This channel is where we debate all future architecture plans');
$requestBody->setMembershipType(new ChannelMembershipType('standard'));

$result = $graphServiceClient->teams()->byTeamId('team-id')->channels()->post($requestBody)->wait();

```