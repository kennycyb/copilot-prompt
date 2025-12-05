# Test Writing Prompt Template

Use this template when you need to generate tests for your code.

## Prompt for Unit Tests

```
Please write comprehensive unit tests for the following code:

[PASTE YOUR CODE HERE]

Include tests for:
1. Happy path scenarios
2. Edge cases
3. Error conditions
4. Boundary conditions
5. Invalid inputs

Use [TESTING FRAMEWORK NAME] and follow existing test patterns in the project.
```

## Prompt for Integration Tests

```
Please write integration tests for the following component:

[PASTE YOUR CODE HERE]

Test the integration between:
- [COMPONENT A]
- [COMPONENT B]

Include:
1. Setup and teardown procedures
2. Mock/stub strategies for external dependencies
3. Assertions that verify the integration works correctly
4. Error handling scenarios
```

## Prompt for Test Cases (No Code Yet)

```
I'm planning to implement [FEATURE DESCRIPTION].

Please suggest test cases that should be covered, including:
1. Functional test cases
2. Edge cases
3. Error scenarios
4. Performance considerations
5. Security test cases

Format as a checklist.
```

## Example Usage

```
Please write unit tests for this validation function:

function validateEmail(email) {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
}

Include tests for:
- Valid email addresses
- Invalid formats
- Edge cases (empty string, null, undefined)
- Special characters

Use Jest framework.
```

## Tips

- Specify the testing framework you're using
- Mention any mocking libraries (e.g., Jest, Sinon, Mockito)
- Include context about what the code does
- Specify coverage goals if you have them
- Reference existing test patterns in your codebase
