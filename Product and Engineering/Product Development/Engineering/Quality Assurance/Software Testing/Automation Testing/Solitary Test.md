---
tags:
  - Testing
  - Concept
---
# Definition
A Solitary Test is executed in isolation from anything that may influence its result. In [[Quality Assurance#Software Products|Software Testing]], this is often described as a [[Unit Testing|Unit Test]] but must not communicate with any other unit of the [[product]] to be considered Solitary.

The purpose of Solitary tests is to ensure that the unit behaves exactly as expected given no outside interference. The opposite of this is a [[Sociable Test]], which integrates one unit or  system with another to generate the test result. When another unit starts to communicate with the tested unit it brings with it edge cases that must be considered and will need mitigation. 
# Example

# Source
Found in the #MartinFowler blog about [Testing Shapes](https://martinfowler.com/articles/2021-test-shapes.html), along with [[Sociable Test]] and [[Testing Shapes]] detail.