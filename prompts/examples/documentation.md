# Documentation Generation Prompt Template

Use this template when you need to generate documentation for code, APIs, or projects.

## Prompt for Function/Class Documentation

```
Please generate comprehensive documentation for the following code:

[PASTE YOUR CODE HERE]

Include:
1. Brief description of what it does
2. Parameters with types and descriptions
3. Return value with type and description
4. Usage examples
5. Any exceptions or errors that might be thrown
6. Notes about edge cases or important behavior
```

## Prompt for API Documentation

```
Please create API documentation for the following endpoint:

Endpoint: [METHOD] /api/endpoint/path
Handler code:
[PASTE YOUR CODE HERE]

Include:
1. Endpoint description
2. HTTP method
3. Request parameters (path, query, body)
4. Request body schema
5. Response codes and their meanings
6. Response body schema
7. Example requests and responses
8. Authentication requirements
```

## Prompt for README Generation

```
Please create a comprehensive README.md for this project:

Project purpose: [DESCRIBE PURPOSE]
Tech stack: [LIST TECHNOLOGIES]
Main features: [LIST FEATURES]

Include:
1. Project title and description
2. Features list
3. Installation instructions
4. Usage examples
5. Configuration options
6. Contributing guidelines
7. License information
```

## Tips

- Provide clear context about what you're documenting
- Mention your target audience (developers, end-users, etc.)
- Specify the documentation format you prefer
- Include any existing documentation that should be referenced
