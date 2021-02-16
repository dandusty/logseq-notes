---
title: CAS 6 Runbook
---

## http://iamweb1.iam.gatech.edu/docs/internal/runbooks/cas6

## CAS6 Restarts

Production: There are three ways to restart CAS6

1. Wait after config changes. The refresh process should restart the containers
1. Use the cas-ecs-service commandline on the config refresher #+BEGIN_EXAMPLE
. /srv/setenv
cas-ecs-service -- update-service --force-new-deployment
or
cas-ecs-service --service cas-management -- update-service --force-new-deployment
#+END_EXAMPLE
 3. Use the AWS Web Console. Update the Service, either changing something or clicking "Force new deployment" on the first page.
