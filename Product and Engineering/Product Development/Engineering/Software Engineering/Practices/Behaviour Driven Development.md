---
tags:
  - Engineering
  - Practice
aliases:
  - BDD
---
# About
Also known as BDD, this is a practice that encourages collaboration between [[Software Engineering|Software Engineers]], [[Quality Assurance|QAs]] and customer representation, whether this is a [[Product Management]] or an actual customer. It focuses on conversation and concrete examples to create shared understanding of the behaviour a system should exhibit.
# Practices
## Gherkin
This is a language commonly associated with BDD. It uses terms and structure to clearly describe the behaviours of a system, and focuses on readability for users. It is also used to describe [[Quality Assurance#Test Cases|Test Cases]] or [[User Stories#Acceptance Criteria|Acceptance Criteria]] for complex topics that require simplification for non-technical stakeholders that may inspect or be shown these artefacts by the development team.
### Keywords
Somewhat similar to the [[Unit Testing#3As|3As of Unit Testing]], Gherkin looks to arrange the context of the language into some distinct sections to make clear what is required, what is being tested, and what the output should be for each test.
#### Given
Similar to the [[Unit Testing#Arrange|Arrange]] step of the [[Unit Testing#3As|3As]], the Given keyword in Gherkin illustrates to the reader the [[Learning Test Cycles#Assumptions|Assumption]] that are being made by the test. For a [[Quality Assurance|QA]], this gives them some prerequisites that must be completed by using the system. For a user, this helps frame the steps that have already been taken

```Gherkin
Given a customer with an account has logged into the web store
```

In the above example, there are some [[Learning Test Cycles#Assumptions|Assumptions]] that have been made as well as the identification of a [[Personas|Persona]] that is being applied to the problem. This example assumes that the user is a customer [[Personas|Persona]], that they know their username and password, that they have entered the information correctly, and then they have clicked login. All of this is summerised in a single statement.
#### When
Similar to the [[Unit Testing#Act|Act]] step of the [[Unit Testing#3As|3As]], the When keyword indicates to the reader the action that is being performed and tested. It clearly identifies the actions that need to be taken by the user to create the desired outcome.

```Gherkin
Given a customer with an account has logged into the web store
When the user adds an item they wish to buy to their basket
```

Again, there are some [[Learning Test Cycles#Assumptions|Assumptions]] we can make about the steps in the When. To find the the item that the user wishes to buy, they must have either searched for a [[product]] or accessed a saved item.
#### Then
Finally, similarly to the [[Unit Testing#Assert|Assert]] step of the [[Unit Testing#3As|3As]], comes the validation of the output. This step clearly details any specifics that need to be validated based on the flow.

```Gherkin
Given a customer with an account has logged into the web store
When the user adds an item they wish to buy to their basket
Then the web store should pop up a sidebar on the right of the window with the basket
```

In the above example, information about the specific and expected operation the web store should performed are outlined. If, for instance, the side bar opened but contained no items this would clearly identify a failure in the function.

With the whole statement completed, the reader also now has a clear understanding of the actions that must be taken to see the result of the expressed behavior. It is not a set of instructions or reproduction steps, but an expression of the cause and effect that a system should exhibit.
### Operators
At times, there are multiple strings to a process that need to be joined together. While not a recognised keywords, the use of the operators **And**, **Or** and **Not** helps to indicate to a user that multiple steps or outcomes exist that must be completed or tested to achieve the desired outcome.

```Gherkin
Given a customer with an account has logged into the web store
When the user adds an item they wish to buy to their basket from the suggested items on the homepage
Then the web store should pop up a sidebar on the right of the window with the basket containing any items that have been added but not purchased and should ask the user if they want to Buy Now
```
# Tools
## Cucumber
Cucumber is a [[Quality Assurance|testing]] tool to represent Gherkin in [[Automation Testing]]. There are two versions, one which is Open Source and contributed to by a community, and Pro version which offers integration with Jira as well as a suite of tools for using its interpretation for the language. Due to its open source nature, the community have also made it possible to integrate Cucumber natively into some [[Quality Assurance|testing]] frameworks such as [[Automation Testing#Playwright|Playwright]]. 
## Specflow
Similarly to Cucumber, Specflow is a tool for converting Gherkin language into executable tests for the purpose of [[Automation Testing]]. Specflow was created for the purpose of integration with [[Automation Testing#Selenium|Selenium]] and .NET languages.
# References
[Specflow - Gherkin](https://specflow.org/learn/gherkin/)
# Sources
[Specflow](https://specflow.org/)
[Cucumber](https://cucumber.io/)