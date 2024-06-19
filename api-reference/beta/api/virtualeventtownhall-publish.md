---
title: "virtualEventTownhall: publish"
description: "Publish a virtual event town hall to make it visible to its audience."
author: "frankpeng7"
ms.localizationpriority: medium
ms.subservice: "cloud-communications"
doc_type: apiPageType
---

# virtualEventTownhall: publish
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Publish a [virtualEventTownhall](../resources/virtualeventtownhall.md) to make it visible to its audience.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "virtualevent-publish-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/virtualevent-publish-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /solutions/virtualEvents/townhalls/{id}/publish
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request

The following example shows a request.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "virtualeventtownhall.publish",
  "sampleKeys": ["bce9a3ca-a310-48fa-baf3-1cedcd04bb3f@4aa05bcc-1cac-4a83-a9ae-0db84b88f4ba"]
}
-->
``` http
POST https://graph.microsoft.com/beta/solutions/virtualEvents/townhalls/bce9a3ca-a310-48fa-baf3-1cedcd04bb3f@4aa05bcc-1cac-4a83-a9ae-0db84b88f4ba/publish
```

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/virtualeventtownhallpublish-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

The following example shows the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```
