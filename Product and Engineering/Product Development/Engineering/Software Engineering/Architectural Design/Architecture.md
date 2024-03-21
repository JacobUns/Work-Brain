---
tags:
  - Engineering
  - Concept
  - Architecture
aliases:
  - Software Architecture
  - Solutions Architecture
  - Enterprise Architecture
  - Architectural Design
---
# About
As with civil engineering, building [[Software Engineering|software]] that will last for years to come and is easy to maintain and expand requires forethought and planning, and therefore the discipline is a skill in its own right.  
# Forms of Architecture
## Software Architecture
This form of architectural design focuses on a unit of software and how it is going to operate and interact. It could be considered [[Solitary Test|Solitary]] in the same way that Unit Tests can be [[Sociable Test|Sociable]] or [[Solitary Test|Solitary]]. The focus is purely on how does this unit of software need to work and the components it's going to be made from. This is a discipline that becomes more important as there becomes a bigger focus on [[Micro-service Architecture|Micro-service]] architectures as more [[Software Engineering|Software Engineers]] start to pick up responsibilities for architectural design.
## Solutions Architecture
This form of architectural design focuses on the interaction between modules of software and how they need to communicate in a performant manner. In contrast to Software Architecture, this can only be [[Sociable Test|Sociable]] in its approach and could be compared to [[Integration Testing]] as a concept.
## Enterprise Architecture
This form of architectural design focuses on Solutions architecture at scale. It is much less worried about the intricacies of each individual piece of software and instead looks to combine and solutions into an integrated environment without causing friction throughout.
# Data Processing Architectures
When processing data in a solution, there are many options to choose from but the core concepts are those of [[#Queues]] and [[#Stacks]]. Both of these structures come with actions associated to them to add and remove items from the structure.
## Queues
Just like in real life, a queue is a reserved area for something to line up against in order to be processed. It follows a [[Acronyms#^FIFO|FIFO]] approach, where the first item put into the queue will be the first item processed. The concept of a queue is used in many applications of [[Software Engineering]] to process data structures, whether it be in memory with an algorithm or in wider concepts such as [[Event Driven Architecture]]. The FIFO concepts also come from [[Asset Management]] and the physical examples of this can be used analogously to describe the virtual equivalent.

In this example, the Enqueue action will put an item onto the back of the queue and the Dequeue action with take it from the front of the queue. This is important for keeping chronology of the items being processed. Queues 

![[Queue Data Structure.png]]
## Stacks
A stack mimics the action of stacking objects in its concept, where, to be able to do anything with the items at the bottom of the stack, the items at the top must be dealt with first. This is a [[Acronyms#^LIFO|LIFO]] approach, and is regularly seen by [[Software Engineering|Software Engineers]] during debugging of code. 

The actions for a stack are known as Pushing and Popping. Pushing an item onto the stack will place it as the next item for processing. Popping from a stack will retrieve the top-most item each time.

![[Stack Data Structure.png]]
# Types
- [[Domain Driven Design]]
- [[Micro-service Architecture]]
- [[Monoliths]]
- [[Event Driven Architecture]]
- [[Client-Server]]
# UML
Most architecture is done using diagrams that use a common format for communicating concepts between developers to 
- [[C4  Diagram]]
- [[Class Diagram]]
- [[Entity Relationship Diagram (ERD)]]
- [[Process Flow Diagram]]
- [[Sequence Diagram]]