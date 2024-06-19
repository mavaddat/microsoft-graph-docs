---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\WorkbookChartGridlines;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new WorkbookChartGridlines();
$requestBody->setVisible(true);

$result = $graphServiceClient->drives()->byDriveId('drive-id')->items()->byDriveItemId('driveItem-id')->workbook()->worksheets()->byWorkbookWorksheetId('workbookWorksheet-id')->charts()->byWorkbookChartId('workbookChart-id')->axes()->valueAxis()->minorGridlines()->patch($requestBody)->wait();

```