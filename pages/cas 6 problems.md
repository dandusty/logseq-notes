---
title: CAS 6 Problems
---

## DONE SCHEDULED: <2021-02-15 Mon 08:30> Check Bomgar with CAS
:PROPERTIES:
:todo: 1613427008654
:done: 1613533029388
:END:
## #sso
## Remaining CAS Problems
:PROPERTIES:
:background_color: #793e3e
:END:
### Matlab (scoped affiliation) - Mathworks
#### Only releasing eduPersonTargetedId
#### Needs
### github academic and github business (entitlement authorization)
### Ridecell (not able to load metadata)
### With javascript disabled, redirect to Login.gatech doesn't happen (leads to a single factor login opportunity)
#### Can we include something in the flow that warns users that login will not work if javascript isn't enabled? "You need to enable javascript to continue."  This would be on the CAS 6 login page
### Remedy (Alex Agle)
#### CAS app that is getting service ticket validated, but can't login successfully
#### Can't figure out what's wrong in the logs
### Eli Patterson's time out issue
#### He waited a long time on the CAS login page and then tried to login and he got the Application Not Authorized to Use CAS message
#### He then opened another tab and got a Login Successful pag
#### Bert suggested modifying the error message to say "Application Not Found or Not Authorized to Use CAS" and mention in the sub text that the user can retry and it may work
### Workday not working with IE 11 or Edge
#### Production Workday url - `https://wd5.myworkday.com/gatech/d/home.htmld`
## Resolved CAS Problems
:PROPERTIES:
:background_color: #497d46
:END:
### [[fw.noc SSO]]
### TurningTechnologies (Incommon Essential Attribute bundle not released)
#### Paul has pushed a fix for this (Works)
### Blackbaud CRM
testing url - 
` https://crm32910s.sky.blackbaud.com/32910s/webui/webshellpage.aspx?databasename=32910s `
- behavior: looping
- solution: moved attribute release to json

k