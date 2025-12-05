# Quick Reference: Common Copilot Prompts

This file contains quick, copy-paste ready prompts for common development tasks.

## Code Generation

### Generate a Function
```
Create a function that [describe what it should do]
Include error handling and input validation
```

### Generate a Class
```
Create a [ClassName] class that:
- [Feature 1]
- [Feature 2]
- [Feature 3]
Follow [language] best practices
```

### Generate API Endpoint
```
Create a REST API endpoint:
- Method: [GET/POST/PUT/DELETE]
- Path: /api/[resource]
- Purpose: [describe purpose]
Include validation and error handling
```

## Code Explanation

### Explain Code
```
Explain what this code does in simple terms:
[paste code]
```

### Explain Complex Logic
```
Break down this complex logic step by step:
[paste code]
Include what each part does and why
```

## Code Improvement

### Optimize Performance
```
Optimize this code for better performance:
[paste code]
Explain the improvements made
```

### Improve Readability
```
Make this code more readable and maintainable:
[paste code]
Use clear variable names and add necessary comments
```

### Add Error Handling
```
Add comprehensive error handling to this code:
[paste code]
Handle edge cases and invalid inputs
```

## Testing

### Quick Unit Test
```
Write unit tests for this function:
[paste code]
Include happy path and edge cases
```

### Test Coverage
```
What test cases are missing for this code?
[paste code]
List them as a checklist
```

## Documentation

### Add Code Comments
```
Add helpful comments to this code:
[paste code]
Focus on explaining the why, not the what
```

### Generate JSDoc/Docstring
```
Generate [JSDoc/Python docstring/Javadoc] for:
[paste code]
```

### Quick README Section
```
Create a README section for [feature/component]
Include usage examples
```

## Debugging

### Find the Bug
```
There's a bug in this code. Find it:
[paste code]
Expected: [describe expected behavior]
Actual: [describe actual behavior]
```

### Explain Error
```
Explain this error message:
[paste error]
And suggest how to fix it
```

## Refactoring

### Extract Method
```
Extract the [describe logic] into a separate method:
[paste code]
```

### Remove Duplication
```
Refactor this code to remove duplication:
[paste code]
```

### Apply Design Pattern
```
Refactor this using the [pattern name] pattern:
[paste code]
```

## Security

### Security Review
```
Review this code for security vulnerabilities:
[paste code]
```

### Sanitize Input
```
Add input sanitization to prevent [XSS/SQL injection/etc]:
[paste code]
```

## Database

### Write SQL Query
```
Write a SQL query to [describe what you need]
Database: [PostgreSQL/MySQL/etc]
```

### Optimize Query
```
Optimize this SQL query:
[paste query]
```

## Git

### Write Commit Message
```
Write a commit message for these changes:
[describe changes]
```

### Generate Changelog
```
Generate a changelog entry for:
[describe feature/fix]
```

## Tips for Effective Prompts

1. **Be Specific**: Instead of "improve this code", say "optimize this code for memory usage"
2. **Provide Context**: Include relevant information about your project, framework, or constraints
3. **Include Examples**: Show examples of what you want when possible
4. **Iterate**: Start with a basic prompt and refine based on the response
5. **Use Follow-ups**: Ask clarifying questions if the initial response isn't quite right

## Prompt Engineering Patterns

### Chain of Thought
```
Let's solve this step by step:
1. [First step]
2. [Second step]
3. [Third step]
[Your question]
```

### Role-Based
```
Act as a [expert in X]. 
[Your specific request]
```

### Constraint-Based
```
[Your request]
Requirements:
- [Constraint 1]
- [Constraint 2]
- [Constraint 3]
```

### Example-Based
```
[Your request]
Here's an example of what I want:
[Provide example]
Now do the same for:
[Your specific case]
```
