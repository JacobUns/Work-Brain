## Definition
A monorepo is a single repository containing multiple distinct projects, with well-defined relationships. In contrast, a [[Polyrepo]] achieves the same thing but with complete encapsulation of its code.

## Description
![[monorepo-polyrepo.svg]]
A repository with multiple projects but with no relationship between them would be considered #CodeColocation but not a monorepo. A repository that contains a massive application without division and encapsulation of discrete parts is also not a monorepo.
![[monolith-modular.svg]]
## Advantages
- Reduces the need to publish packages if all consumers are in the same repository
- Reduces potential overhead from infrastructure configuration to deploy and integrate code
- Highlights problems with integrating code immediately and reduces breaking changes
- One place to store all config and testing means reduced cognitive load when setting up a solution and quicker recognition of errors
- Easier dependency management for imported packages
## Disadvantages
- No way to restrict access only to some parts of the solution
- Increases build time as there are more aspects to a solution than with a [[Polyrepo]]

## Sources 
https://monorepo.tools/#what-is-a-monorepo
https://www.toptal.com/front-end/guide-to-monorepos