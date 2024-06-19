---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Ediscovery\CaseSettings;
use Microsoft\Graph\Beta\Generated\Models\Ediscovery\RedundancyDetectionSettings;
use Microsoft\Graph\Beta\Generated\Models\Ediscovery\TopicModelingSettings;
use Microsoft\Graph\Beta\Generated\Models\Ediscovery\OcrSettings;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CaseSettings();
$redundancyDetection = new RedundancyDetectionSettings();
$redundancyDetection->setIsEnabled(false);
$redundancyDetection->setSimilarityThreshold(70);
$redundancyDetection->setMinWords(12);
$redundancyDetection->setMaxWords(400000);
$requestBody->setRedundancyDetection($redundancyDetection);
$topicModeling = new TopicModelingSettings();
$topicModeling->setIsEnabled(false);
$topicModeling->setIgnoreNumbers(false);
$topicModeling->setTopicCount(50);
$topicModeling->setDynamicallyAdjustTopicCount(false);
$requestBody->setTopicModeling($topicModeling);
$ocr = new OcrSettings();
$ocr->setIsEnabled(true);
$ocr->setMaxImageSize(12000);
$requestBody->setOcr($ocr);

$result = $graphServiceClient->compliance()->ediscovery()->cases()->byCaseId('case-id')->settings()->patch($requestBody)->wait();

```