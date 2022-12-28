**Automated Testing**

1. Unit Tests
2. Integration tests
3. End-to-end e2e tests

_Unit Tests_
individual building blocks (functions, components)
Projects typically have dozens, hundreds of unit tests
Most common and important

_Integration Tests_
Combination of unit blocks
Projects typically contain a couple of integration tests

_End-to-End e2e tests_
Testing entire scenarios as user would experience them - e.g. logging a user in, then going to a certain page.
Projects typically contain a few e2e tests

_What to Test & How?_
. What
Small blocks, focused, test one thing
Reason for failure clear

. How
Success and error cases which could occur, test rare results

_Required Tools & Setup_ - where and how do we write these test?
Tool for running our tests and asserting results - pass or fail. (pop. Jest)
In react app need a simulation for automatic tests to interact with them - simulate browser. (pop. React Testing Library)

Create-react-app sets up and installs Jest and React Testing Library

**Writing Tests - The Three "A"s**

1. Arrange - Set up test data, test conditions, and test environment.
2. Act - Run logic that should be tested (e.g. execute function, simulate button click etc.)
3. Assert - Compare execution results with expected results.

_test, expect_
both globally available.

_render, screen_
render the function/component
screen gives access to virtual DOM
screen.get gives error if not found.
screen.query won't; can check if something is not in the document - failed search is purpose.
screen.find will return a promise, if element is eventually on screen.

**Test Suites**
Organizing tests

describe('description of category to which tests will belong e.g. <Greeting/> / 'Greeting Component', () => {
. put entire test here.
})

Components ->
. Greeting.js
. Greeting.test.js

Put multiple tests in the describe function to group tests into Test Suites.
