---
title: "Use cases by role: General user"
tags:
  - varys
  - documentation
  - concepts
---

## Role description

All authenticated users are belongs to general role. They do not have any special designations or obligations. There are two use cases for this role:

1. search for secrets and related entities (people, services)
1. input new data: secrets,services, reference roots, people

Second scenario instantly grants user other role and extends number of use cases.

## Overview

User which does not belong to any role, has little to none requirements for dashboard. But this is great place to show previously viewed secrets, services, people. Also dashboard can display history of edits of the user.

## Search

General user has no predefined queries and uses just full text search or attribute search using filters.

## Data input

User should be able to create new:

* secret
* reference roots
* service
* people

When users create secret, service or reference root, they automatically became owners of this entities and obtains corresponding roles.
