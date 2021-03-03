---
title: CAS 6 Troubleshooting
---

## Parsing Logs - Bert's Thoughts
1. Script: Username and/or Application: Show Service tickets issued
2. Script: Trace a service ticket (get all the traceids and search for them in logs)
3. Get the text being sent back to validate a ST
4. Goal: Compare CAS6 response to CAS3
## Viewing attributes in the logs - look for this
#+BEGIN_EXAMPLE
DEBUG [org.apereo.cas.services.AbstractRegisteredServiceAttributeReleasePolicy] -  - <Final collection of attributes allowed are: [{​​accountid=88d419ae-e251-4af3-9dfd-393455a19cdf, Email=[kwhite@example.edu], firstname=[Karl], lastname=[White], mail=[kwhite@example.edu], qualysguard_external_id=[kwhite@example.edu], urn:oasis:names:tc:SAML:2.0:attrname-format:unspecified=[kwhite], urn:oid:0.9.2342.19200300.100.1.1=[kwhite], urn:oid:0.9.2342.19200300.100.1.3=[kwhite@example.edu], urn:oid:1.3.6.1.4.1.5923.1.1.1.1=[student, member], urn:oid:1.3.6.1.4.1.5923.1.1.1.7=[], urn:oid:1.3.6.1.4.1.5923.1.1.1.9=[student@gatech.edu, member@gatech.edu], urn:oid:1.3.6.1.4.1.636.2.12.1.3=kwhite@AD.GATECH.EDU, urn:oid:2.5.4.3=[Karl White], urn:oid:2.5.4.4=[White], urn:oid:2.5.4.42=[Karl], User.Email=[kwhite@example.edu], User.LastName=[White], User.ProfileId=Standard User}
#+END_EXAMPLE
## Checking CAS Status
### Actuator Health - `https://sso.gatech.edu/cas/actuator/health`
### Available endpoints for the actuator - `https://sso.gatech.edu/cas/actuator`
### Custom health
## #sso
