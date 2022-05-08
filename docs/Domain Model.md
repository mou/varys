---
title: Domain Model
tags:
  - varys
  - documentation
  - concepts
  - datamodel
---

# Core entities

## Secret

Secret represents all varieties of data, which should not be exposed or be available arbitrary. Ideally secrets values and data only observed during it's creation, handing over and transferring into storage or management system. Because exposing it's value may create a risk or vulnerability to whole system in which it used. Varys does not hold or store secret value, only related metadata.

Besides secret value itself secret has a plenty of metadata associated with it. 

Identity:

* unique identifier inside storage
* storage reference
* title
* human readable description

Temporal:

* when secret was registered
* when secret was updated
* when secret will expire
* when secret became obsolete and marked as non existing

Another important group of properties are various relationship:

* scopes in which this secret is relevant
* persons
  * who responsible to maintain secret and deputies (if secret is provided by third party, this person is typically do all communication with this parties)
  * who is holding secret in possession;
* services
  * providing services
  * consuming services
* other secrets (secrets may be coupled together like pairs username/password or one may be derived from or depend on another, like CA chain)
* references (secrets may be referenced from various sources: documentation pages, issues, configuration files, software source code, etc)
* related documents. Instruction for obtaining, detailed description of how credential used, etc

## Secret Storage

Storage describes external entity which holds the value of secretes. Secret storage doe not imply any requirements or properties to actual entity. It could be anything from safe or bank vault to most complicated HSM solution.

Most of storage properties are optional, because they vary from media to media. The only required are related to storage identity:

* type of storage: paper, safe, security key, hosted hashicorp Vault, cloud Vault-like service, etc
* name used to reference this storage

Important properties:

* persons who can access storage or responsible for it's operations
* Location. It could be URL, another programmatic protocol address, physical position, address, etc
* references to documents describing working with this storage

## Scope

Scope is a virtual entity describing various aspects that could be related to secret. But most importantly limiting area of application of secret and acts as some form of namespace, allowing multiple secrets in different scope partially share identity attributes. For example we can define set of scopes named `Environment` to restrict and differentiate secrets by security sensitivity, and to avoid name collision. Another use case - create scope to separate group of secrets by various attributions: subsidiary inside companies group, product, internal/third-party, maintain chore type (manual/semi-auto/automatic).

Scope attributes mostly used to provide explanation or identify it:

* scope set
* scope name
* description

## Person

Secrets and services has relations to persons, to describe ownership, responsibilities. Person entities can represent both a users of Varys and third party representatives.

In case of corresponding person to a user all the attributes are used from user entity, but for arbitrary external person they may contain:

* name
* sign off (offboard) date (in case person is a user)
* contact email
* contact phone
* position
* notes about person

## Service

Service are the consumers and providers of most secrets. Some services, owned or third party, requires secrets to be accessed, others may require secrets to verify incoming requests, derive short lived secrets or to access another services.

Service attributes:

* name
* address (URL)
* owned or third party
* persons related to service (owners, contacts for third-party services)

## Reference roots

Represents resource which can contain other sub resources references secrets. For example HTTP address of Wiki or other documentation system, source code repository, various definitions and declarations which are not under version control (cloud resources), etc

Properties of reference roots:

* name
* address. In most cases - URL
* description
* icon (helpful for abbreviation)
