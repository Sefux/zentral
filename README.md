# Welcome to Zentral

[![Tests](https://github.com/zentralopensource/zentral/actions/workflows/tests.yml/badge.svg)](https://github.com/zentralopensource/zentral/actions/workflows/tests.yml)
[![Coverage Status](https://coveralls.io/repos/github/zentralopensource/zentral/badge.svg?branch=main)](https://coveralls.io/github/zentralopensource/zentral?branch=main)
[![Documentation Status](https://readthedocs.org/projects/zentral/badge/?version=latest)](https://docs.zentral.io)

[Zentral](https://zentral.com) is a system to manage Apple devices under high security considerations. Zentral integrates deeply with enterprise architecture, such as IdPs, SIEMs and an entity’s PKI to implement robust security measures and best practices. Zentral fully supports config-as-code and its APIs can be managed with the [Zentral Official Terraform Provider](https://registry.terraform.io/providers/zentralopensource/zentral/latest/docs).

## Key concepts

### Open source agents
Zentral is built on and orchestrates popular open source agents:
[Munki](https://github.com/munki/munki) to manage software distribution and patching
[Osquery](https://github.com/osquery/osquery) to get data from devices
[Santa](https://github.com/northpolesec/santa) for binary authorization and data collection

### Event-driven architecture
- Everything in Zentral is an event
- Events are presented in a unified, machine readable format
- Events can be filtered and shipped to different stores

### Tagging & sharding
Tags can be used to scope configuration to devices across all modules in Zentral. You can tag devices based on set conditions and attributes, you can use SCIM to create tags based on IdP group membership and you can also build mass tagging automations.
You can use sharding to roll out configuration only to smaller subsets of machines. For example, you could use 20% shard on the tag `canary` to test a new version of a software on only a sample of devices, before releasing it to the whole canary group. 

### Software governance & compliance engine
Zentral offers Application Allowlisting with a user portal to handle authorization requests, based on user voting or admin approvals. Decisions are persistent because of stable identifiers and Zentral presents a full audit trail for permissions. Aggregates of Santa events expose shadow IT and guide building the Allowlist. Zentral's Munki integration gives you control and reporting over distribution & patching of software on the fleet. 
Zentral can run compliance checks against custom benchmarks. Compliance checks can be based on inventory data, scripts and queries. You can send compliance change events to other systems for conditional access via the Shared Signals Framework.

### GitOps & config as code with Terraform
Almost every configuration item in Zentral can be managed as a [Terraform Resource](https://registry.terraform.io/providers/zentralopensource/zentral/latest/docs). You can keep a whole macOS client configured from a [repository](https://github.com/zentralopensource/zentral-cloud-tf-starter-kit), with CI/CD and peer review and you can always return to a previous "known good configuration". 

## Key components

### Unified Inventory
Zentral's core capability is normalising data gathered from different [inventory sources](https://docs.zentral.io/en/latest/apps/inventory/) into a unified data schema. You can search for devices based all kinds of data that Zentral collects and you can view deeply into a devices health, events attached to it and its MDM command history for troubleshooting.

### Apple MDM
Zentral 

### Munki module

### Osquery module 

### Santa module

### User portal

## How to learn Zentral
The Zentral docs are in the [docs](https://github.com/zentralopensource/zentral/blob/main/docs) directory. They are published at [https://docs.zentral.io](https://docs.zentral.io).

## Releases
You will find the latest release information [on GitHub](https://github.com/zentralopensource/zentral/releases).
