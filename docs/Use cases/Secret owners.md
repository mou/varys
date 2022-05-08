---
title: "Use cases by role: Secret owner"
tags:
  - varys
  - documentation
  - concepts
---

## Overview

Opening overview or dashboard page should provide next information relevant for secret owner:

* link to list of secrets marked as deleted since last visit
* link to list of secrets received update not from owner since last visit
* link to list of secrets requiring attention (expiring, ownership transferred from another person to user, requests for role)
* link to list of secrets for which user was assigned as owner

## Search

For secret owner, there should be simple way to quickly query entities with specific properties:

* all owned secrets
* all secrets for which user has a deputy role

## Notifications

For secret owner there should be plenty notifications, due to user responsibility for secret lifecycle and related metadata relevance. Some notification could be aggregated into digest, but some should be emitted at the moment of event.

Critical:

* secret is expire in X
* secret is marked for deletion
* owner of the secret for which user hold deputy role, are marked for signoff/offboard

Non critical:

* new secret requires metadata entry after being created
* secret information was updated
* new references was added or removed to/from secret
