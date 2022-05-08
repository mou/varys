---
title: "Use cases by role: Security specialists"
tags:
  - varys
  - documentation
  - concepts
---

## Overview

Dashboard for security specialist should emphasize only  very important and critical data, due to broad scope. Main purpose of such dashboard is to identify and mitigate risks:

* link to list of secrets expiring in nearest future
* link to list of secrets ownership on which was not transferred but off-boarding of current owner is imminent
* link to list of secrets referenced by services but without owners for configurable amount of time
* link to list of persons with upcoming or ongoing off-boarding procedures

## Search

For security specialist it's very important to quickly find entity which may not become critical but will in  nearest future:

* all secrets without owners
* all services internal or third-party without owners
* all external persons without contact information
* all secrets for third-party services without attached note how to obtain or prolong them

## Notifications

Notifications for security team from one hand should be exhaustive and from other should not be overwhelming. Most of them should notify user about occurred policy violation or possible risks.

* expired secrets
* orphaned secrets
* new secrets stays without metadata for too long
