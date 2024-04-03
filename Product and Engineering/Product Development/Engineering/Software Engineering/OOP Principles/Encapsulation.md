---
tags:
  - Software
  - Engineering
  - Concept
  - oop
---
# Definition
The act of bundling data and methods required to operate an object within a unit of code. In [[Object Orientated Programming]] languages such as .NET and Java, this is common practice and often not thought about by developers as it is the act of creating classes with getter and setter attributes and defined methods for interacting with its attributes.

Encapsulation helps set what can affect data and use methods of an object. Without Encapsulation, code may be misused or important attributes may be changed in unexpected ways which can cause unwanted paths in workflow of code. This is controlled using access modifiers against objects, methods and attributes.

# Access Modifiers
Used to define visibility of classes, methods and attributes. The Access Modifier specifies the level of accessibility for the class, method or attribute, and you should generally use the most restrictive modifier that still allows you to implement your business logic.
## Private
- Most Restrictive
- Most Common Modifier
- Should be the default choice for methods and attributes
- Only accessible within the same class
## Public
- Least Restrictive
- Accessible by the code of the class and by any code that has initialised an instance of the class
## Protected
- Can be used by all classes that inherit the original class
- Mostly used for internal methods that need to be called or overridden by a subclass