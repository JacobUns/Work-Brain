---
tags:
  - Testing
  - AutomationTesting
  - Discipline
aliases:
  - QA
  - QAs
  - Testing
---
# About
The discipline of Quality Assurance is that of testing what has been produced within a [[Product Team]]. It is the first line of defense against degradation of service and deterioration of customer confidence and engagement due to reduction in quality. The practice focuses on determining whether what has been produced is of the right level of quality, but not necessarily whether it achieves as much value as expected. This may be done through [[Release on Demand]] strategies, such as [[AB Testing]] or [[Usability Testing]].
# Practices
## Test Cases
Test Cases define the execution of steps to create behaviour in a system and should be outlined with the expected behaviour. This then forms the basis of defining and documenting the system interactions during development and enables [[Regression Testing]] for any deviation.

The test case may either identify what is typically referred to as the Happy or Sad path during the test, but should keep to the bounds of one flow rather than crossing context. This is to ensure clarity in purpose and execution outcome, as executing multiple flows in one test can make it difficult to understand each test's purpose. Doing so also makes it more difficult to parallelize work between either automation or individuals, depending on the type of testing being executed.
### Happy Path
Happy path testing should detail the expected steps required to produce the positive result for the system. It often assumes that users will input all the correct information and required parameters for the test to pass. As a result, it's typically the first type of testing that is executed by developers and testers alike.
### Sad Path
Of the two types of testing, Sad Path is often the most difficult and generally most neglected form of testing for which to create a high level of coverage. Sad path requires the engineer or tester to validate that the system behaves as expected when things go wrong, either by way of a user providing the wrong type of information, or from 
## Test Suites

# Types
Testing can be broken into two categories, [[Manual Testing|manual]] and [[Automation Testing|automated]]. They both achieve the same thing; [[Automation Testing]] achieves it slower in the shorter term, but faster and with less waste in the long-term. The downside with [[Automation Testing]] is that the tests must be maintained once they are created, and their creation can be expensive both in execution cost and effort to development.

[[Manual Testing]] creates significantly more waste due to the requirement to execute
## Physical Products
The types of test executed will depend on the product being tested. If the tests are running on physical products such as circuit boards or machines, it is possible to set up something akin to a [[Integration Testing|Integration Test]] by building a board which has swappable components. It will also be possible to [[End-to-End Testing|End-to-End]], [[Regression Testing|Regression]] and [[Performance Testing|Performance]] test what has been built, but the methods and effort required will vastly differ from Software. 

At De Beers, the development of the Autoflow machines required specific parcels of stones to be used due to the sort distribution and like-for-like comparisons. They would need to be run through multiple times with different procedures, and the light levels and outputs measured using spreadsheet tooling. With the AMS Micro, pick-and-place performance, run-rate and other such metrics were captured to understand how the machine was behaving before the [[Go-to-Market|Go-to-Market Strategy]] was executed.

Due to the nature of physical products, testing these through [[Automation Testing|Automation]] is much more difficult and so more often organisations prefer to manually test their creations instead.
## Software Products
Software products will have a very similar set of tests to Physical in terms of concepts, but the benefit of software testing is that, should a business decide to invest in their infrastructure, that it can all be done virtually and in minutes and seconds rather than days. We can also go down to smaller granularity in much faster loops than physical products, but the concepts remain the same. For instance, one of the modern standards for [[Software Engineering|Software Development]] is the creation of [[Unit Testing|Unit Tests]]. Physical products can theoretically also be [[Unit Testing|Unit Tested]], but it has a much longer lead time and execution time. 

# Example Test Structure
![[Software Testing Structure.png]]