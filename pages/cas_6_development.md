---
title: CAS 6 Development
---

- Where should we be making changes?
  1. Which branch should we all use?
  2. How do we reconcile changes between master and test for the groovy script?
  3. What is the best practice for doing separate work in git going forward? Separate feature branches?
- Making changes - 03-02-2021
  1. Make a change to the test branch first
  2. Go to master branch
  3. Compare & pull request
  4. Should see base: master <- compare: test
  5. Commit merge
- Bert is adding an Incommon warmup process to the CAS 6 startup
	- Each container runs this every few seconds
	- It's used as one of the two healthchecks for the CAS containers
		- If the script doesn't work for 3 minutes, then it will restart the container