---
aliases:
  - TDD
tags:
  - Testing
---

# Summary
## Definition
Test Driven Development (TDD) is a method of writing code where the focus is on the behaviour that is going to be exhibited by someone using that code. Ideally, TDD should be used along-side the [[Object Orientated Programming]] paradigm to keep code implementation separated from the tests themselves.

The method requires writing the tests associated to code before writing the code itself to prove that the code behaves as expected. Each change should be small, and you should remain in control of your test the entire time. If you are not able to predict preciously what change is going to happen, this indicates you are making too large a change. The key to successful TDD is small increments and fast feedback.

You should not be writing all test first, and then trying to make them all pass. The point of TDD is to take small steps, create a test for a [[Learning Test Cycles#Hypotheses|Hypotheses]], then write just enough code to prove that [[Learning Test Cycles#Hypotheses|Hypothesis]]. Finally, it's just as much about creating documentation for how your system should work as it is about [[Quality Assurance|testing]] your code works as expected. Your tests will show someone new to the code how it should work, and provide them the confidence they need to make changes to that code.

## Framework for TDD
![[TDD TRbGbR Framework.png]]
### Framework Summary
The aim of the framework is to stay in control of your code at all times. It should never pass unexpectedly or fail unexpectedly. This can be done by making many small changes. If you lose control, take smaller steps. Finally, start from the inside with your core interface and work outwards building on complexity slowly.

#### Framework:
- [[Test Driven Development#Step 1 - Think|Step 1 - Think]]
	- Identify a small test for specific behaviour
- [[Test Driven Development#Step 2 - Red Bar|Step 2 - Red Bar]]
	- Write just enough test code that the test would cover behaviour identified in Step 1
	- Test against a public interface, following [[Encapsulation]].
	- Run the test - it should fail
- [[Test Driven Development#Step 3 - Green Bar|Step 3 - Green Bar]]
	- Write just enough code to make the test pass
	- Run the test - it should pass in an expected manner
- [[Test Driven Development#Step 4 - Refactor |Step 4 - Refactor]]
	- Aggressively refactor to find improvements
- [[#Step 5 - Repeat|Step 5 - Repeat]]

#### Benefits
- Little time should be spent debugging as all changes should be known and planned.
- Mistakes should be identified in a matter of minutes and fixed easily.
- Should be able to refactor at every opportunity with confidence that the tests will catch any mistakes

# Process
### Step 1 - Think
- Imagine behaviour you want your code to have
	- Think of the very first piece to be implemented
		- Should be very small
		- Preferably less than five lines of code
- Think of a test that will fail under specific behaviour
	- Should also be very few lines of code
	- Test should test behaviour, not implementation
	- Ideally test against an interface
		- If the interface doesn't change, the test should continue to pass

This step is the hardest part of TDD as it requires thinking ahead. What do you want to do? And what test is required to prove it first?

Pairing and Mobbing can help. The driver works on making the current test pass, while a navigator thinks ahead figuring out which increment and test should come next.

If thinking ahead is too difficult, spike the approach, the come back to this step.

### Step 2 - Red Bar
Next step is to write the test. The goal of this step is to remain in control of your code, and to always know what the code is doing and why, not just to have a passing test.

- The test should only test current increment of behaviour identified in Step 1
	- Ideally less than five lines of code
- Write the test based on a public interface
	- Respect [[Encapsulation]]
	- The test should use names that don't exist yet to intentionally force designing from the perspective of someone consuming the interface
- Write the assertions on the test by predicting how the test will fail, not just that it does fail
	- This represents the [[Learning Test Cycles#Hypotheses|Hypothesis]] being tested
- Run the test
	- You should always be able to predict what's going to happen
		- If the test doesn't fail, or fails in a different way you are no longer in control
		- Troubleshoot any problems. Maybe it failed in a different place, or in a different manner than expected
	- Unexpected Successes are just as problematic as Unexpected Failures

### Step 3 - Green Bar
- Write just enough production code to make the test pass
	- Usually less than five lines of code
	- Design purity or conceptual elegance don't matter at this point. It will be modified in the next step
- Run the test
- The test should pass, resulting in a green outcome if you're still in control
	- If the test fails, get back to known-good as quickly as possible
		- Should be easy if you've written the right amount of code
		- Mistakes usually obvious with the right amount of code written
			- If not obvious, consider undoing your change and start again
			- May also require you to comment out or delete the test and try a smaller increment
- The key is to remain in control the entire time

If problems are encountered that result in beating your head against a wall, it's almost always better to try again with a smaller increment that to try and push through, though this may be tempting. If you feel like the answer is just around the corner, set a timer for 5-10mins, and if you haven't resolved the problem within that time then unwind the change and start again with a smaller increment.

### Step 4 - Refactor
When your tests are passing, refactor without worrying about breaking anything.
- Review the code so far and look for improvements
- If pairing, ask the navigator for any suggestions for improvement
- Keep refactors small
- Run your tests after each refactor
- If a test fails, revert to known-good code
- Any refactors made should not change or add behaviour, as new behaviour requires a new failing test

### Step 5 - Repeat
When ready to add a new behaviour, start from the beginning of the cycle.

It's likely you'll run through several cycles very quickly, then spend more time thinking and refactoring for a few cycles, then speed up again.

## Eat the Onion from the Inside Out
Sometimes taking small steps can be challenging. When approaching a new piece of code, start with the core problem and behaviour and work outwards. An example strategy for this starts with the interface.
### Core Interfaces
- Define the interface you want to call
- Keep it simple
- See whether calling the interface makes sense in context
- Hardcode the expected response at this time.
### Calculations and Branches
Hardcoded responses aren't good enough for production code
- What calculations are needed to change from a hardcoded response to a dynamic response? Add each one branch or one calculation at a time
- Focus on happy path tests, how will the code be used everyday?
### Loops and Generalization
Code often involves loops and alternative ways of being used.
- Once the core business logic is done, add one alternative at a time.
- Refactor as you go and keep the code clean. This might require using generic forms to keep code clean.
### Special cases and error handling
After happy-path cases, write a test for each potential edge case that may come from your code.
- Imagine everything that can go wrong
- Does your code call any code that may throw an exception?
- Do you make any [[Learning Test Cycles#Assumptions|Assumptions]] that need validating?
### Runtime assertions
You might identify situations that come from programming errors, such as array index out of bounds, or variables that should never be null. Add assertions for these so they fail fast.

## ZOMBIES
A mnemonic from #JamesGrenning that can help:
- Test **Z**ero
- Test **O**ne
- Test **M**any
While you test pay attention to:
- **B**oundaries
- **I**nterfaces
- **E**xceptions
While keeping your code **S**imple

## Sources
The details of this are taken from articles and content written by #JamesShore. Further reading around his topics can be done [here](http://www.jamesshore.com/v2/books/aoad2/test-driven_development). There is a simple summary explaining where the concept comes from written by #MartinFowler [here](https://martinfowler.com/bliki/TestDrivenDevelopment.html) .