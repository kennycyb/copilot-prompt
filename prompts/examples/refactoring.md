# Code Refactoring Prompt Template

Use this template when you need to refactor or improve existing code.

## Prompt for General Refactoring

```
Please refactor the following code to improve:

[PASTE YOUR CODE HERE]

Focus on:
1. Code readability
2. Maintainability
3. Following best practices
4. Reducing complexity
5. Improving performance

Explain the changes you make and why they improve the code.
```

## Prompt for Design Pattern Application

```
Please refactor this code to use the [PATTERN NAME] pattern:

Current code:
[PASTE YOUR CODE]

Requirements:
- [REQUIREMENT 1]
- [REQUIREMENT 2]

Please show:
1. The refactored code using the pattern
2. Explanation of how the pattern is applied
3. Benefits of this approach
```

## Prompt for Breaking Down Large Functions

```
This function is too complex. Please break it down into smaller, focused functions:

[PASTE YOUR CODE]

Guidelines:
- Each function should have a single responsibility
- Use descriptive function names
- Maintain the same overall behavior
- Improve testability
```

## Prompt for Removing Code Duplication

```
I have code duplication across these files:

File 1:
[PASTE CODE FROM FILE 1]

File 2:
[PASTE CODE FROM FILE 2]

Please:
1. Identify the duplicated logic
2. Extract it into reusable functions/modules
3. Show how to refactor both files to use the shared code
```

## Example Usage

```
Please refactor this code to be more functional and less imperative:

function processUsers(users) {
  let activeUsers = [];
  for (let i = 0; i < users.length; i++) {
    if (users[i].active) {
      activeUsers.push(users[i]);
    }
  }
  
  let userNames = [];
  for (let i = 0; i < activeUsers.length; i++) {
    userNames.push(activeUsers[i].name.toUpperCase());
  }
  
  return userNames;
}

Use modern JavaScript array methods and make it more readable.
```

## Tips

- Be specific about what aspects you want to improve
- Mention any design patterns you'd like to apply
- Specify any constraints (e.g., maintain backward compatibility)
- Include context about how the code is used
- Mention performance requirements if relevant
