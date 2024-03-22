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

# Test Structure
To enhance the maintainability of our code and ensure that we follow [[Clean Code]] standards, we look for methods to structure tests to make them more readable and modifiable. 
## 3As
The Three A's stand of **Arrange**, **Act**, **Assert**. These detail how the test should be structured to provide clear understanding of what occurs in each section.
### Arrange
The Arrange section provides context for all the inputs and requirements for the test to be executed. It should include all of the mocking, preparation, and variable initialisation that is required by any function that is being tested as part of the unit test. 
```C#
[TestClass]
public class ExampleTestCases {
	[TestMethod]
	public void SadPathTestCase(){
		// Arrange
		var listInput = new List<string>();
		var mockClass = new Mock<RequiredClassForTesting>(listInput);
		var classToBeTested = new ClassToBeTested(mockClass);
	}
} 
```
### Act
The Act section of the test illustrates the specific piece of functionality that is being tested within this test method. It should be clearly distinguishable from all other parts of the code in a similar fashion to Arrange.

```C#
[TestClass]
public class ExampleTestCases {
	[TestMethod]
	public void SadPathTestCase(){
		// Arrange
		var listInput = new List<string>();
		var mockClass = new Mock<RequiredClassForTesting>(listInput);
		var classToBeTested = new ClassToBeTested(mockClass);

		mockClass.Setup(x => x.GenerateSentence(It.IsAny<List<string>()>))
			.Returns(null)
		
		// Act
		var testMethodOutput = classToBeTested.DoSomething(new DataObject
		{
			data1 = "The quick brown fox jumped over ",
			data2 = 5
			data3 = " lazy dogs."
		});
	}
} 
```
### Assert
The Assert section clearly identify what the unit test is checking for within this test method. Depending on the unit testing framework being used the language may be different than a developer should be expecting but this shouldn't matter to someone trying to maintain the code in the future.
``` C#
[TestClass]
public class ExampleTestCases {
	[TestMethod]
	public void SadPathTestCase(){
		// Arrange
		var listInput = new List<string>();
		var mockClass = new Mock<RequiredClassForTesting>(listInput);
		var classToBeTested = new ClassToBeTested(mockClass);

		mockClass.Setup(x => x.GenerateSentence(It.IsAny<List<string>()>))
			.Returns(null)
		
		// Act
		var testMethodOutput = classToBeTested.DoSomething(new DataObject
		{
			data1 = "The quick brown fox jumped over ",
			data2 = 5
			data3 = " lazy dogs."
		});

		// Assert
		Assert.IsTrue(testMethodOutput.ProcessedSuccessfully);
		Assert.IsTrue(It.IsNotNull(testMethodOutput.ProcessingResult));
	}
} 
```