---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc device-management virtual-endpoint user-settings patch --cloud-pc-user-setting-id {cloudPcUserSetting-id} --body '{\
  "@odata.type": "#microsoft.graph.cloudPcUserSetting",\
  "displayName": "Example",\
  "restorePointSetting": {\
    "frequencyType": "sixteenHours",\
    "userRestoreEnabled": true\
  },\
  "localAdminEnabled": false,\
  "resetEnabled": true\
}\
'

```