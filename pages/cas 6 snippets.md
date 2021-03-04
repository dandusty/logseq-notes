---
title: CAS 6 Snippets
---

## Adding a hard coded attribute
### "attributeReleasePolicy" : {
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
#+END_EXAMPLE
