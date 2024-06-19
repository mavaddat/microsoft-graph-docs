---
author: sandeo-MSFT
ms.topic: include
---

For delegated scenarios, the calling user must be a user assigned to one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json):

- Cloud Device Administrator
- Helpdesk Administrator
- Intune Service Administrator
- Security Administrator
- Security Reader
- Global Reader

To access the actual passwords on the device by using the `$select=credentials` query parameter, the calling user must be a user assigned to one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json):

- Cloud Device Administrator
- Intune Service Administrator
