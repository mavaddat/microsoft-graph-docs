---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc-beta users contacts create --user-id {user-id} --body '{\
  "givenName": "Pavel",\
  "surname": "Bansky",\
  "emailAddresses": [\
    {\
      "address": "pavelb@contoso.com",\
      "name": "Pavel Bansky",\
      "type": "personal"\
    },\
    {\
      "address": "pavelb@contoso.com",\
      "name": "Pavel Bansky",\
      "type": "other",\
      "otherLabel": "Volunteer work"\
    }\
  ],\
  "phones" : [\
    {\
      "number": "+1 732 555 0102",\
      "type": "business"\
    }\
  ]\
}\
'

```