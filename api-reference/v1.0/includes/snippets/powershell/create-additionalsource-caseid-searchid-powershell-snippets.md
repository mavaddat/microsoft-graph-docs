---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Security

$params = @{
	"@odata.type" = "microsoft.graph.security.siteSource"
	site = @{
		webUrl = "https://contoso.sharepoint.com/sites/SecretSite"
	}
}

New-MgSecurityCaseEdiscoveryCaseSearchAdditionalSource -EdiscoveryCaseId $ediscoveryCaseId -EdiscoverySearchId $ediscoverySearchId -BodyParameter $params

```