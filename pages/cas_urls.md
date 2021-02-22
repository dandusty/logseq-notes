---
title: CAS Urls
---

## Old CAS Urls
#+BEGIN_EXAMPLE
CAS login URL – https://login.gatech.edu/cas/login 

CAS validate URL – https://login.gatech.edu/cas/validate 

CAS logout URL – https://login.gatech.edu/cas/logout

#+END_EXAMPLE
## New CAS Urls
#+BEGIN_EXAMPLE
CAS login URL – https://sso.gatech.edu/cas/login 

CAS validate URL – https://sso.gatech.edu/cas/validate 

CAS logout URL – https://sso.gatech.edu/cas/logout
#+END_EXAMPLE
## #sso
## Log out urls
### While joined at the hip
#### sso logout goes to login logout
### When we have cas 3 and cas 6 login systems separated
#### cas 3 logouts forward to cas 6
#### use wording on the logout page to cover any gaps
#### BigIP - we look for cas 3 telling us logout was successful, then we redirect browser over to cas 6 logout
####
### After phased upgrade is finished
#### login logout goes to sso logout
