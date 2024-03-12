---
tags:
  - Diagram
  - Model
  - Engineering
---

# Description
A sequence diagram shows the process interactions arranged in time order from UML. Used to document a requirements for a new system or document an existing one.

They're sometimes known as Event Diagrams or Event Scenarios.
# Symbols
## Activation box
Represents the time needed for an object to complete a task. The longer the task, the longer the activation box.
## Actor
External entities that interact with a system
## Filled Arrow
Synchronous Message
## Hollow Arrow
Asynchronous Message
## Example
```plantuml
actor User order 10
participant MainPostgresDB order 20
participant RedisCache order 30
participant AuthMemCache order 40
participant InsendiAuth order 50
participant BackendService order 60
participant FeatureFlagAPI order 70
participant FeatureFlagCache order 80
participant LaunchDarklyAdapter order 90
participant LaunchDarkly order 100
participant DataDog order 110

== Server Initialisation ==

FeatureFlagAPI -> DataDog: Server Started Event Sent
FeatureFlagAPI -> LaunchDarklyAdapter : Get All Flags
LaunchDarklyAdapter -> LaunchDarkly : Get All Flags
LaunchDarklyAdapter <-- LaunchDarkly: List of Flags
FeatureFlagAPI <-- LaunchDarklyAdapter : List of Flags
FeatureFlagAPI -> FeatureFlagCache : Store Flags
FeatureFlagAPI -> DataDog : FF Cache Created Event Sent

== User Request ==

User -> BackendService : Request Data w/ Token
activate BackendService

BackendService -> InsendiAuth : Token Authentication Request
activate InsendiAuth

InsendiAuth -> AuthMemCache : Check Cache
InsendiAuth <-- AuthMemCache : No data returned
InsendiAuth -> RedisCache : Check Cache
InsendiAuth <-- RedisCache : No data returned
InsendiAuth -> MainPostgresDB : Query Identity
InsendiAuth <-- MainPostgresDB : Identity Data
InsendiAuth -> AuthMemCache : Create Cache
InsendiAuth -> RedisCache : Create Cache

BackendService <-- InsendiAuth : Validated Identity
deactivate InsendiAuth

BackendService -> FeatureFlagAPI : Check Flag with Identity
activate FeatureFlagAPI

FeatureFlagAPI -> FeatureFlagCache : Retrieve Flag
FeatureFlagAPI <-- FeatureFlagCache : Flag Returned
FeatureFlagAPI -> LaunchDarkly : Send Analytics
FeatureFlagAPI -> DataDog : Send Analytics

BackendService <-- FeatureFlagAPI : Valid Response
deactivate FeatureFlagAPI

User <-- BackendService : Data Requested
deactivate BackendService
```
