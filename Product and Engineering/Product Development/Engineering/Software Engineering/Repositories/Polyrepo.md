# Definition
A polyrepo structure is the opposite of a [[Monorepo]] structure. Each team, application or project has its own dedicated repository that encapsulates all code to do with that repository. It is also common for each repository to have it's own build and/or release process.

## Description

![[monorepo-polyrepo.svg]]

![[polyrepo-practice.svg]]

## Advantages
- Allow teams to have full autonomy and ownership of their code
- Full encapsulates and isolates a deployable service creating a truly independently deployable unit

## Disadvantages
- Can cause code duplication between [[repositories]], and removing code duplication requires [[repositories]] and infrastructure setup
- Polyrepo structures can cause inconsistencies in tooling, library usage and quality processes without diligent oversight

## Sources
https://monorepo.tools/#what-is-a-monorepo