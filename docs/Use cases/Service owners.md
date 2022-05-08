---
title: "Use cases by role: Service owner"
tags:
  - varys
  - documentation
  - concepts
---

## Overview

Dashboard of service owner contain next statistics and links to detailed lists of items:

* link to list of added secrets, which represents credentials to owned services
* link to list of secrets related to owned services, which requires attention (expiring, with requested roles)
* link to list of services introduced usage of owned service secrets
* link to list of secrets which owners are planed sign off or off-boarding and somehow related to owned services

## Search

For service owner there should be shortcuts or simple way to query next searches:

* All owned services
* All secrets used by owned services
* All secrets owned services provides as credentials

## Notifications

Similar to other user roles, service owner can receive notifications aggregated into digest, and immediate critical ones.

Critical:

* owned service was marked as deleted
* secrets related to owned service was marked as deleted

Non critical:

* new secret was added to relation with owned service
* service metadata was updated
