### Traditional Testing Shape
Traditionally known as the testing triangle, this testing shape puts [[Unit Testing]] at the core of testing, expecting a majority of cases to be caught at with quick running, isolated tests. A large proportion of the code is also covered by [[Integration Testing]] which tests the previously tested units in conjunction with other units. Finally the fewest tests covered by directly interacting with the UI using [[End-to-End Testing]] techniques that interact with the application using browser manipulation with chromium or selenium based techniques.

![[Testing Triangle.png]]

When using [[Test Driven Development]] this is the most common type of testing shape, as all code will be covered by a high level of unit tests that cover all system behaviour. [[Integration Testing]] can be done in many ways, including [[Contract Testing]], [[Big Bang Testing]]

### Testing Trophy
![[Testing Trophy.jpg]]

### Testing Honeycomb
The testing honeycomb is an approach taken by some companies [like Spotify](https://engineering.atspotify.com/2018/01/testing-of-microservices/) when testing their Microservices. Similarly to the Testing Trophy, its major focus is on the integration tests over any other test. The implementation detail covers such areas as [[Unit Testing]] but does not limit to this form of testing.

![[Testing Honeycomb.png]]