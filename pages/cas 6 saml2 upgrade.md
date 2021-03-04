---
title: CAS 6 SAML2 Upgrade
---

## Dropbox not working

### mail attribute is the actual mail and not eppn
### May be do to Incommon Essential Attribute Bundle
## Cisco apps not working
### Cisco call manager may need to be encrypted
### ucucuty01.ucc.gatech.edu is working without encryption
### https://cucmpub01.ucc.gatech.edu:8443/ucmuser may need encryption
### May be related to time skew - http://www.voipinfo.net/docs/cisco/118770-configure-cucm-00.pdf
### Not related to time skew.  It's actually a bug with CAS where it's not using the requested index number for the ACS url.
