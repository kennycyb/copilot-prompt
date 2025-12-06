# Security Analysis Prompt Template

Use this template when you need to analyze code for security vulnerabilities.

## Prompt for Security Review

```
Please perform a comprehensive security analysis on this code:

[PASTE YOUR CODE HERE]

Check for:
1. SQL Injection vulnerabilities
2. Cross-Site Scripting (XSS) risks
3. Authentication/Authorization issues
4. Sensitive data exposure
5. Input validation gaps
6. Insecure dependencies
7. Hardcoded secrets or credentials
8. Insecure cryptographic practices
9. CSRF vulnerabilities
10. Path traversal vulnerabilities

For each issue found:
- Explain the vulnerability
- Show the problematic code
- Provide a secure alternative
- Rate severity (Critical/High/Medium/Low)
```

## Prompt for Dependency Security Check

```
Please analyze these dependencies for security issues:

Package.json / requirements.txt / etc:
[PASTE DEPENDENCY FILE]

Check for:
1. Known vulnerabilities (CVEs)
2. Outdated packages
3. Deprecated packages
4. License issues
5. Suggest secure alternatives if needed
```

## Prompt for Authentication Security

```
Review this authentication implementation for security:

[PASTE AUTHENTICATION CODE]

Focus on:
1. Password hashing (use bcrypt, scrypt, or Argon2)
2. Session management
3. Token security (JWT, etc.)
4. Rate limiting
5. Brute force protection
6. Password reset security
7. Multi-factor authentication readiness
```

## Prompt for API Security

```
Review this API endpoint for security:

[PASTE API CODE]

Check for:
1. Authentication requirements
2. Authorization checks
3. Input validation
4. Output encoding
5. Rate limiting
6. CORS configuration
7. API key management
8. Request size limits
```

## Example Usage

```
Please perform a comprehensive security analysis on this login function:

function login(req, res) {
  const { username, password } = req.body;
  const query = `SELECT * FROM users WHERE username = '${username}'`;
  const user = db.query(query);
  
  if (user && user.password === password) {
    // SECURITY ISSUE: Hardcoded secret - DO NOT DO THIS
    const token = jwt.sign({ id: user.id }, 'secret123');
    res.json({ token });
  } else {
    res.status(401).json({ error: 'Invalid credentials' });
  }
}

Check all OWASP Top 10 vulnerabilities.
```

## Security Checklist Template

```
Create a security checklist for [type of application]:

Application type: [web app/API/mobile app/etc]
Tech stack: [list technologies]

Include checks for:
- Authentication & Authorization
- Data Protection
- Input Validation
- Output Encoding
- Cryptography
- Error Handling
- Logging & Monitoring
- Third-party Components
- Configuration
- Infrastructure Security
```

## Tips

- Specify the technology stack (helps identify specific vulnerabilities)
- Mention compliance requirements (GDPR, PCI-DSS, HIPAA, etc.)
- Include threat model if you have one
- Ask for OWASP Top 10 specific checks
- Request both immediate fixes and long-term improvements

## Common Security Patterns to Request

### Secure Password Hashing
```
Show me how to implement secure password hashing using bcrypt in [language]
```

### Input Sanitization
```
Add input sanitization to prevent XSS in this code:
[PASTE CODE]
```

### SQL Injection Prevention
```
Convert this query to use parameterized statements:
[PASTE SQL QUERY CODE]
```

### Secure Token Generation
```
Generate a cryptographically secure random token for [PURPOSE]
Use [LANGUAGE] built-in crypto library
```

## Resources to Mention

- OWASP Top 10
- CWE (Common Weakness Enumeration)
- SANS Top 25
- Security-specific linting tools for your language
