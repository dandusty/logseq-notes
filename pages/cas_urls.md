---
title: CAS Urls
---

- Old CAS Urls
  #+BEGIN_EXAMPLE
  CAS login URL – https://login.gatech.edu/cas/login 
  
  CAS validate URL – https://login.gatech.edu/cas/validate 
  
  CAS logout URL – https://login.gatech.edu/cas/logout
  
  #+END_EXAMPLE
- New CAS Urls
  #+BEGIN_EXAMPLE
  CAS login URL – https://sso.gatech.edu/cas/login 
  
  CAS validate URL – https://sso.gatech.edu/cas/validate 
  
  CAS logout URL – https://sso.gatech.edu/cas/logout
  #+END_EXAMPLE
- #sso
- Log out urls
	- While cas 3 and cas 6 are joined at the hip
		- sso logout goes to login logout
	- When we have cas 3 and cas 6 login systems separated
		- use wording on the logout page to cover any gaps
		- BigIP - we look for cas 3 telling us logout was successful, then we redirect browser over to cas 6 logout
		- For sso.gatech logouts, we use wording to tell the user to complete logging out by clicking a button to logout of cas 3
	- After phased upgrade is finished
		- login logout goes to sso logout