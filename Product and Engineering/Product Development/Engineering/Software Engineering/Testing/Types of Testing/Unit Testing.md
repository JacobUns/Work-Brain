---
tags:
  - Practice
  - Software
  - Testing
aliases:
  - Unit Test
---
# About
Unit Tests are intended to test an individual unit of code. It's a highly prevalent method of testing with Engineers, and often comes coupled with the [[Test Driven Development]] methodology.

Should frequently use [[Mocking]] or [[Stubbing]] to simulate the responses from other units of code that would interact with the tested unit. Not using [[Mocking|Mocks]] or [[Stubbing|Stubs]] results in highly [[Sociable Test|Sociable Tests]] which can cause difficulty or dependency between units when refactoring code as many tests may require modification as a result.