---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphdevicemanagement "github.com/microsoftgraph/msgraph-sdk-go/devicemanagement"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

requestBody := graphdevicemanagement.NewImportPostRequestBody()


importedWindowsAutopilotDeviceIdentity := graphmodels.NewImportedWindowsAutopilotDeviceIdentity()
id := "985b4f49-4f49-985b-494f-5b98494f5b98"
importedWindowsAutopilotDeviceIdentity.SetId(&id) 
groupTag := "Group Tag value"
importedWindowsAutopilotDeviceIdentity.SetGroupTag(&groupTag) 
serialNumber := "Serial Number value"
importedWindowsAutopilotDeviceIdentity.SetSerialNumber(&serialNumber) 
productKey := "Product Key value"
importedWindowsAutopilotDeviceIdentity.SetProductKey(&productKey) 
importId := "Import Id value"
importedWindowsAutopilotDeviceIdentity.SetImportId(&importId) 
hardwareIdentifier := []byte("aGFyZHdhcmVJZGVudGlmaWVy")
importedWindowsAutopilotDeviceIdentity.SetHardwareIdentifier(&hardwareIdentifier) 
state := graphmodels.NewImportedWindowsAutopilotDeviceIdentityState()
deviceImportStatus := graphmodels.PENDING_IMPORTEDWINDOWSAUTOPILOTDEVICEIDENTITYIMPORTSTATUS 
state.SetDeviceImportStatus(&deviceImportStatus) 
deviceRegistrationId := "Device Registration Id value"
state.SetDeviceRegistrationId(&deviceRegistrationId) 
deviceErrorCode := int32(15)
state.SetDeviceErrorCode(&deviceErrorCode) 
deviceErrorName := "Device Error Name value"
state.SetDeviceErrorName(&deviceErrorName) 
importedWindowsAutopilotDeviceIdentity.SetState(state)
assignedUserPrincipalName := "Assigned User Principal Name value"
importedWindowsAutopilotDeviceIdentity.SetAssignedUserPrincipalName(&assignedUserPrincipalName) 

importedWindowsAutopilotDeviceIdentities := []graphmodels.ImportedWindowsAutopilotDeviceIdentityable {
	importedWindowsAutopilotDeviceIdentity,
}
requestBody.SetImportedWindowsAutopilotDeviceIdentities(importedWindowsAutopilotDeviceIdentities)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
import, err := graphClient.DeviceManagement().ImportedWindowsAutopilotDeviceIdentities().Import().PostAsImportPostResponse(context.Background(), requestBody, nil)


```