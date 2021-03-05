---
title: CAS 6 Snippets
tags: sso
---

## **Adding a hard coded attribute**
:PROPERTIES:
:id: 60423405-8fd8-40e0-99a0-7388c67dff38
:END:
### 
``` json
"attributeReleasePolicy" : {
    "@class" : "org.apereo.cas.services.ReturnMappedAttributeReleasePolicy",
    "allowedAttributes" : {
          "@class" : "java.util.TreeMap",
          "givenname": "FirstName",
          "sn": "LastName",
          "uid": "uid",
          "mail": "Email",
          "custId": "groovy {return '17462'}",
          "roleId": "groovy {return '413141202'}"
      }
   }
```