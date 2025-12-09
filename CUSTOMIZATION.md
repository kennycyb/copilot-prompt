# Customization Guide

This guide will help you customize the Copilot prompt templates for your specific project needs.

## Customizing `.github/copilot-instructions.md`

The workspace instructions file tells Copilot about your project's conventions and preferences.

### What to Include

1. **Language and Framework Specific Guidelines**
   ```markdown
   ## Framework: React + TypeScript
   - Use functional components with hooks
   - Prefer TypeScript interfaces over types
   - Use CSS Modules for styling
   - Follow React best practices from the official documentation
   ```

2. **Project-Specific Patterns**
   ```markdown
   ## Error Handling
   - Use custom AppError class for all errors
   - Always log errors to our logging service
   - Return user-friendly error messages
   ```

3. **Code Organization**
   ```markdown
   ## File Structure
   - Place components in `src/components/`
   - Place utilities in `src/utils/`
   - Use index.ts for barrel exports
   - Keep files under 200 lines
   ```

4. **API Conventions**
   ```markdown
   ## API Design
   - Use RESTful conventions
   - Version all APIs (e.g., /api/v1/)
   - Use camelCase for JSON properties
   - Include pagination for list endpoints
   ```

5. **Testing Requirements**
   ```markdown
   ## Testing
   - Minimum 80% code coverage
   - Test files named *.test.ts
   - Use Jest and React Testing Library
   - Write integration tests for critical paths
   ```

### Example: Python Project

```markdown
# GitHub Copilot Instructions - Python Data Science Project

## Code Style
- Follow PEP 8 style guide
- Use type hints for all function signatures
- Maximum line length: 100 characters
- Use Black for formatting

## Dependencies
- Use pandas for data manipulation
- Use numpy for numerical operations
- Use scikit-learn for ML models
- Pin all dependency versions

## Testing
- Use pytest for all tests
- Place tests in tests/ directory
- Aim for >90% coverage
- Use fixtures for common test data

## Documentation
- Use Google-style docstrings
- Document all public functions and classes
- Include usage examples in docstrings

## Data Handling
- Never commit data files
- Use data/ directory (in .gitignore)
- Validate all input data
- Handle missing values explicitly
```

## Customizing `.vscode/chat.json`

Add custom chat participants for your specific needs.

### Example: Frontend Developer Participant

```json
{
  "id": "frontend-expert",
  "name": "Frontend Expert",
  "description": "Specialized in React, TypeScript, and modern frontend development",
  "systemPrompt": "You are a frontend development expert specializing in:\n- React with TypeScript\n- Modern CSS (Flexbox, Grid, CSS-in-JS)\n- State management with Redux/Zustand\n- Performance optimization\n- Accessibility (WCAG 2.1)\n- Responsive design\n\nProvide modern, best-practice solutions with explanations."
}
```

### Example: DevOps Participant

```json
{
  "id": "devops-expert",
  "name": "DevOps Expert",
  "description": "Expert in CI/CD, containerization, and infrastructure",
  "systemPrompt": "You are a DevOps expert specializing in:\n- Docker and Kubernetes\n- CI/CD pipelines (GitHub Actions, Jenkins)\n- Infrastructure as Code (Terraform, CloudFormation)\n- Monitoring and logging\n- Cloud platforms (AWS, Azure, GCP)\n- Security best practices\n\nProvide production-ready, scalable solutions."
}
```

### Example: Database Expert Participant

```json
{
  "id": "database-expert",
  "name": "Database Expert",
  "description": "Expert in database design, optimization, and queries",
  "systemPrompt": "You are a database expert specializing in:\n- SQL query optimization\n- Database schema design\n- Indexing strategies\n- Performance tuning\n- Migration strategies\n- Both SQL and NoSQL databases\n\nProvide efficient, scalable database solutions."
}
```

## Creating Custom Prompt Templates

### Template Structure

Every prompt template should follow this structure:

```markdown
# [Template Name]

Brief description of when to use this template.

## Prompt

[The actual prompt with placeholders like [PLACEHOLDER]]

## Example Usage

[Concrete example showing the prompt in action]

## Tips

- [Tip 1]
- [Tip 2]
- [Tip 3]

## Variations

[Alternative ways to use the template]
```

### Example: API Integration Template

```markdown
# API Integration Prompt Template

Use this template when integrating with external APIs.

## Prompt

\`\`\`
Create an integration with the [API NAME] API:

Endpoint: [ENDPOINT URL]
Authentication: [TYPE]
Purpose: [WHAT YOU NEED TO DO]

Requirements:
- Handle rate limiting
- Implement retry logic with exponential backoff
- Add proper error handling
- Log all requests and responses
- Add request/response types
- Include unit tests with mocked API

Use [axios/fetch/etc] for HTTP requests.
\`\`\`

## Example Usage

\`\`\`
Create an integration with the GitHub API:

Endpoint: https://api.github.com/repos/{owner}/{repo}
Authentication: Bearer token
Purpose: Fetch repository information and commits

Requirements:
- Handle rate limiting (5000 requests/hour)
- Implement retry logic with exponential backoff
- Add proper error handling for 404, 403, 500
- Log all requests and responses
- Add request/response types
- Include unit tests with mocked API

Use axios for HTTP requests.
\`\`\`

## Tips

- Always check API documentation for rate limits
- Use environment variables for API keys
- Implement circuit breaker for flaky APIs
- Cache responses when appropriate
- Add timeout handling

## Variations

For webhook integrations, add:
- Signature verification
- Idempotency handling
- Event queuing
```

## Project-Specific Templates

Create templates for common tasks in your project:

### Example: Feature Template

```markdown
# New Feature Development Template

Use this when implementing a new feature in our project.

## Prompt

\`\`\`
Implement the [FEATURE NAME] feature:

Requirements:
- [REQ 1]
- [REQ 2]
- [REQ 3]

Follow our project structure:
- API endpoint in src/api/
- Business logic in src/services/
- Database models in src/models/
- Tests in tests/

Include:
1. API endpoint with validation
2. Service layer implementation
3. Database migrations
4. Unit and integration tests
5. API documentation
6. Update CHANGELOG.md
\`\`\`
```

## Language-Specific Customizations

### JavaScript/TypeScript

```markdown
## TypeScript Guidelines
- Prefer interfaces over types for object shapes
- Use strict mode
- Avoid 'any' type
- Use const assertions where appropriate
- Leverage utility types (Pick, Omit, Partial)
```

### Python

```markdown
## Python Guidelines
- Use type hints (PEP 484)
- Follow PEP 8 style guide
- Use dataclasses for data structures
- Prefer list comprehensions over loops
- Use context managers for resource handling
```

### Java

```markdown
## Java Guidelines
- Follow Google Java Style Guide
- Use Optional instead of null
- Prefer composition over inheritance
- Use builder pattern for complex objects
- Follow SOLID principles
```

## Framework-Specific Customizations

### React

```markdown
## React Guidelines
- Use functional components
- Custom hooks for reusable logic
- Use React.memo for expensive components
- Follow hooks rules
- Prefer composition over inheritance
```

### Django

```markdown
## Django Guidelines
- Use class-based views for CRUD
- Keep views thin, logic in models/services
- Use Django ORM, avoid raw SQL
- Use Django migrations
- Follow Django coding style
```

## Maintenance Tips

1. **Review and Update Regularly**: Update instructions as your project evolves
2. **Team Consensus**: Ensure the team agrees on conventions
3. **Keep It Concise**: Focus on the most important guidelines
4. **Be Specific**: Vague instructions lead to inconsistent results
5. **Include Examples**: Show don't just tell

## Testing Your Customizations

After customizing, test with Copilot:

1. Ask Copilot to generate code following your instructions
2. Review if it follows your conventions
3. Refine instructions if needed
4. Share feedback with your team

## Resources

- [Copilot Instructions Documentation](https://docs.github.com/en/copilot/customizing-copilot/adding-custom-instructions-for-github-copilot)
- [VS Code Chat Participants](https://code.visualstudio.com/docs/copilot/copilot-chat)
