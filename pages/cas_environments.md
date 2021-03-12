---
title: CAS Environments
tags: sso, cas
---

## sso-test.gatech.edu - vip will point to test fargate
## sso-dev.gatech.edu - vip will point to the 205 server
## sso.gatech.edu - vip will point to production fargate
## cas-test.gatech.edu
### Points to the 205 server as of [[Mar 12th, 2021]]
## Set the environment in the docker infrastructure
### On the 205 server, we set RT_ENV in cas-run.sh docker run command
### In Fargate, we do it in the task definition
## Host file changes to point to the 205 server
### 
#+BEGIN_EXAMPLE

#+END_EXAMPLE
# idp-rich (routes to sso-dev March 2021)
130.207.165.156 idp.gatech.edu sso-test.gatech.edu
```
