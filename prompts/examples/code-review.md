# Code Review Prompt Template

Use this template when you need to review code for quality, security, and best practices.

## Prompt

```
Please review the following code:

[PASTE YOUR CODE HERE]

Focus on:
1. Code quality and adherence to best practices
2. Potential bugs or edge cases
3. Security vulnerabilities
4. Performance concerns
5. Code readability and maintainability
6. Suggestions for improvement

Please provide specific, actionable feedback.
```

## Example Usage

When reviewing a function, be specific about what you want reviewed:

```
Please review this authentication function:

function authenticateUser(username, password) {
  const user = db.query("SELECT * FROM users WHERE username = '" + username + "'");
  if (user && user.password === password) {
    return { success: true, token: generateToken(user) };
  }
  return { success: false };
}

Focus particularly on security issues.
```

## Tips

- Be specific about what aspects you want reviewed
- Provide context about the codebase if relevant
- Mention any specific concerns you have
- Include related code if it helps with understanding
