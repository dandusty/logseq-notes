---
title: CAS 6 Problems
---

## #sso 

## Blackbaud CRM
testing url - 
` https://crm32910s.sky.blackbaud.com/32910s/webui/webshellpage.aspx?databasename=32910s `
- behavior: looping
- solution: moved attribute release to json
## DONE SCHEDULED: <2021-02-15 Mon 08:30> Check Bomgar with CAS
:PROPERTIES:
:todo: 1613427008654
:done: 1613533029388
:END:
## fw.noc
testing url -
https://fw.noc.gatech.edu/simplesaml/module.php/core/authenticate.php?as=default-sp
## Remaining CAS Problems
:PROPERTIES:
:background_color: #978626
:END:
### TurningTechnologies (Incommon Essential Attribute bundle not released)
### Matlab (scoped affiliation)
### github academic and github business (entitlement authorization)
### Ridecell (not able to load )
### With javascript disabled, redirect to Login.gatech doesn't happen (leads to a single factor login opportunity)
  - Can we include something in the flow that warns users that login will not work if javascript isn't enabled? "You need to enable javascript to continue."  This would be on the CAS 6 login page
## Remedy (Alex Agle)
### CAS app that is getting service ticket validated, but can't login successfully
### Can't figure out what's wrong in the logs
