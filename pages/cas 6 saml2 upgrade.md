---
title: CAS 6 SAML2 Upgrade
---

## Dropbox not working - FIXED
:PROPERTIES:
:background_color: #497d46
:END:
### mail attribute is the actual mail and not eppn
### May be do to Incommon Essential Attribute Bundle
### Fixed by Paul
## Cisco apps not working - some FIXED and some have workarounds
:PROPERTIES:
:background_color: #978626
:END:
### Cisco call manager may need to be encrypted
### ucucuty01.ucc.gatech.edu is working without encryption
### https://cucmpub01.ucc.gatech.edu:8443/ucmuser may need encryption
### May be related to time skew - http://www.voipinfo.net/docs/cisco/118770-configure-cucm-00.pdf
### Not related to time skew.  It's actually a bug with CAS where it's not using the requested index number for the ACS url.
### We were able to get it working in a temporary state pointing to shib4 using a modified idp metadata file uploaded to Cisco UCM.
### Tested UCM and Jabber and they were working with shib4. Webex Teams and Cisco PCA are working with sso.gatech
## Ehsa not working - FIXED
:PROPERTIES:
:background_color: #497d46
:END:
### https://fm-ehs.ad.gatech.edu/ehsa/
### Attribute release hadn't been set up in CAS 6
### Set up the attribute release in the json and added encryption
## Infoready not working - FIXED
:PROPERTIES:
:background_color: #497d46
:END:
### https://gatech.infoready4.com/
### Not getting mail or the right eduPersonScopedAffiliation
### Attributes are mapped in json. May need to be moved to groovy to use Paul's eduPersonScopedAffiliation code
### For now, I changed email_primary to mail in the json.  Need to fix email_primary in cas.properties
## GTRC Financials not working - PROD FIXED
:PROPERTIES:
:background_color: #497d46
:END:
### Paul Broe's app
### Prod url - https://financials.gtrc.gatech.edu:5443/cgi-bin/printenv
### Dev url - https://financials-dev.gtrc.gatech.edu:5443/cgi-bin/printenv
### May need different name format - https://apereo.github.io/cas/6.1.x/installation/Configuring-SAML2-Attribute-Release.html#attribute-name-formats
## Expo not working - FIXED
:PROPERTIES:
:background_color: #497d46
:END:
### Url - expo.gatech.edu
### Fixed by using groovy hardcoded attribute values
#### ((60423405-8fd8-40e0-99a0-7388c67dff38))
## OneUSG not working - FIXED
:PROPERTIES:
:background_color: #497d46
:END:
### Testing url - http://idp-demo-prod.bor.usg.edu/
#### Demo has different attributes like Aon Key
### OneUSG Connect - https://oneusgconnect.usg.edu/
### No mail
### gtEmployeeSN does not use the oid value from sn
### employeeNumber does not use the oid value of employeeNumber
### Fixed by moving the attribute release to json
## Onthehub not working - FIXED
:PROPERTIES:
:background_color: #497d46
:END:
### Testing url - https://e5.onthehub.com/WebStore/Welcome.aspx?ws=be68ac5d-eccd-dc11-8873-0030485a6b08&&utm_source=Georgia%20Institute%20of%20Technology
### Had to switch to local metadata which I downloaded from the Incommon Metadata browser site - https://met.refeds.org/met/entity/https%253A%252F%252Fe5.onthehub.com/
### Problem was an invalid signing certificate in the metadata coming from the Incommon aggregate
## Security Scorecard not working - FIXED
:PROPERTIES:
:background_color: #497d46
:END:
### login url - https://platform.securityscorecard.io/
### It was using uid as the nameId in the json, so I switched to eppn since that's what Shib uses.
### I wasn't able to log in to test so I asked Kyle Koza to test.
### He tested and it works
## Adobe Acrobat not working
