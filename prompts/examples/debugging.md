# Debugging Prompt Template

Use this template when you need help debugging issues in your code.

## Prompt for Bug Analysis

```
I'm encountering the following error:

Error message:
[PASTE ERROR MESSAGE]

Stack trace:
[PASTE STACK TRACE]

Code where the error occurs:
[PASTE RELEVANT CODE]

What I've tried:
- [ATTEMPT 1]
- [ATTEMPT 2]

Please help me:
1. Identify the root cause
2. Suggest a fix
3. Explain why this is happening
```

## Prompt for Unexpected Behavior

```
My code is producing unexpected behavior:

Expected behavior:
[DESCRIBE WHAT SHOULD HAPPEN]

Actual behavior:
[DESCRIBE WHAT IS HAPPENING]

Code:
[PASTE YOUR CODE]

Context:
[ANY ADDITIONAL RELEVANT INFORMATION]

Please help identify what's going wrong and how to fix it.
```

## Prompt for Performance Issues

```
I'm experiencing performance issues with this code:

Code:
[PASTE YOUR CODE]

Performance problem:
[DESCRIBE THE ISSUE - e.g., "Takes 5 seconds to process 1000 items"]

Input size/characteristics:
[DESCRIBE THE INPUT]

Please help:
1. Identify performance bottlenecks
2. Suggest optimizations
3. Provide more efficient alternatives
```

## Example Usage

```
I'm getting a "Cannot read property 'name' of undefined" error:

Code:
function getUserName(userId) {
  const user = users.find(u => u.id === userId);
  return user.name;
}

Error occurs when calling: getUserName(999)

Please help me:
1. Understand why this happens
2. Suggest a proper fix with error handling
3. Recommend best practices for similar scenarios
```

## Tips

- Include complete error messages and stack traces
- Provide relevant code context, not just the failing line
- Mention what you've already tried
- Include input data that triggers the issue
- Specify your environment (language version, framework, etc.)
