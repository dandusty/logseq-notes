---
title: CAS 6 SAML2 Upgrade
---

## Dropbox not working - FIXED
### mail attribute is the actual mail and not eppn
### May be do to Incommon Essential Attribute Bundle
### Fixed by Paul
## Cisco apps not working - some FIXED and some have workarounds
### Cisco call manager may need to be encrypted
### ucucuty01.ucc.gatech.edu is working without encryption
### https://cucmpub01.ucc.gatech.edu:8443/ucmuser may need encryption
### May be related to time skew - http://www.voipinfo.net/docs/cisco/118770-configure-cucm-00.pdf
### Not related to time skew.  It's actually a bug with CAS where it's not using the requested index number for the ACS url.
### We were able to get it working in a temporary state pointing to shib4 using a modified idp metadata file uploaded to Cisco UCM.
### Tested UCM and Jabber and they were working with shib4. Webex Teams and Cisco PCA are working with sso.gatech
## Ehsa not working - FIXED
### https://fm-ehs.ad.gatech.edu/ehsa/
### Attribute release hadn't been set up in CAS 6
### Set up the attribute release in the json and added encryption
##
