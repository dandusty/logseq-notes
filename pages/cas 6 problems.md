---
title: CAS 6 Problems
---

- DONE SCHEDULED: <2021-02-15 Mon 08:30> Check Bomgar with CAS
  todo:: 1613427008654
  done:: 1613533029388
- #sso
- Remaining CAS Problems
  background-color:: #793e3e
	- Ridecell (not able to load metadata)
		- Login url - https://gt-new.ridecell.com/request
		- May need to use local metadata as a workaround
	- Mytest
		- Authentication Interrupt not working as needed
	- With javascript disabled, redirect to Login.gatech doesn't happen (leads to a single factor login opportunity)
		- Can we include something in the flow that warns users that login will not work if javascript isn't enabled? "You need to enable javascript to continue."  This would be on the CAS 6 login page
	- Remedy (Alex Agle)
		- CAS app that is getting service ticket validated, but can't login successfully
		- Can't figure out what's wrong in the logs
	- Eli Patterson's time out issue
		- He waited a long time on the CAS login page and then tried to login and he got the Application Not Authorized to Use CAS message
		- He then opened another tab and got a Login Successful pag
		- Bert suggested modifying the error message to say "Application Not Found or Not Authorized to Use CAS" and mention in the sub text that the user can retry and it may work
	- Workday not working with IE 11 or Edge
		- Production Workday url - https://wd5.myworkday.com/gatech/d/home.htmld
	- Mist - new app not working with CAS
	- Incommon - mdq not working
	- Banner - CAS protocol not working
		- May switch to SAML2
	- Malicious users can bypass Duo by authenticating with sso.gatech and ignoring the javascript warning if they have disabled javascript.  They can ignore the warning and go to the app without using duo and
- Resolved CAS Problems
  background-color:: #497d46
	- Matlab (scoped affiliation) - Mathworks
	- github academic and github business (entitlement authorization)
		- solved with inline groovy
		- gtAccountEntitlement had to be included in the attribute map
	- [[fw.noc SSO]]
	- TurningTechnologies (Incommon Essential Attribute bundle not released)
		- Paul has pushed a fix for this (Works)
	- Blackbaud CRM
	  testing url - 
	  https://crm32910s.sky.blackbaud.com/32910s/webui/webshellpage.aspx?databasename=32910s
- behavior: looping
- solution: moved attribute release to json