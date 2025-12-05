# Usage Examples

This file demonstrates how to use the templates in this repository.

## Example 1: Using Copilot Instructions

When you copy `.github/copilot-instructions.md` to your project, Copilot will automatically follow those guidelines when providing suggestions.

**Before** (generic suggestion):
```javascript
// Copilot might suggest:
function handleUser(data) {
  const user = data.user;
  // ...
}
```

**After** (with custom instructions about error handling):
```javascript
// Copilot will suggest including error handling:
function handleUser(data) {
  try {
    if (!data || !data.user) {
      throw new AppError('Invalid user data');
    }
    const user = data.user;
    // ...
  } catch (error) {
    logger.error('Error handling user:', error);
    throw error;
  }
}
```

## Example 2: Using Chat Participants

In VS Code Copilot Chat, use `@` to reference custom participants:

### Code Review
```
@code-review Please review this authentication function for security issues
```

Copilot will focus specifically on security vulnerabilities, best practices, and provide detailed feedback.

### Documentation
```
@documentation Generate comprehensive API documentation for this endpoint
```

Copilot will create structured documentation with parameters, responses, and examples.

### Testing
```
@test-writer Create unit tests for this validation function with edge cases
```

Copilot will generate comprehensive tests including boundary conditions and error cases.

## Example 3: Using Prompt Templates

### Code Review Template in Action

**Input** (using code-review.md template):
```
Please review the following code:

function calculateTotal(items) {
  let total = 0;
  for (let i = 0; i < items.length; i++) {
    total += items[i].price * items[i].quantity;
  }
  return total;
}

Focus on:
1. Code quality and adherence to best practices
2. Potential bugs or edge cases
3. Performance concerns
```

**Expected Output**:
- Suggestions for input validation
- Edge case handling (empty array, invalid items)
- Modern JavaScript alternatives (reduce, map)
- Type safety recommendations

### Documentation Template in Action

**Input** (using documentation.md template):
```
Please generate comprehensive documentation for the following code:

function fetchUserData(userId, options = {}) {
  const { includeOrders = false, includeProfile = true } = options;
  // ... implementation
}

Include:
1. Brief description
2. Parameters with types
3. Return value
4. Usage examples
```

**Expected Output**:
Complete JSDoc or similar documentation with all requested sections.

### Testing Template in Action

**Input** (using testing.md template):
```
Please write comprehensive unit tests for this code:

function isValidEmail(email) {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
}

Include tests for:
1. Valid email addresses
2. Invalid formats
3. Edge cases
4. Null/undefined inputs

Use Jest framework.
```

**Expected Output**:
```javascript
describe('isValidEmail', () => {
  it('should return true for valid email addresses', () => {
    expect(isValidEmail('test@example.com')).toBe(true);
    expect(isValidEmail('user.name@domain.co.uk')).toBe(true);
  });

  it('should return false for invalid formats', () => {
    expect(isValidEmail('notanemail')).toBe(false);
    expect(isValidEmail('@example.com')).toBe(false);
    expect(isValidEmail('test@')).toBe(false);
  });

  it('should handle edge cases', () => {
    expect(isValidEmail('')).toBe(false);
    expect(isValidEmail(' ')).toBe(false);
  });

  it('should handle null and undefined', () => {
    expect(isValidEmail(null)).toBe(false);
    expect(isValidEmail(undefined)).toBe(false);
  });
});
```

## Example 4: Customizing for Your Project

### Step 1: Copy Files
```bash
cp -r .github /path/to/your/project/
cp -r .vscode /path/to/your/project/
```

### Step 2: Customize Instructions
Edit `.github/copilot-instructions.md`:
```markdown
# GitHub Copilot Instructions - My E-commerce Project

## Framework: Next.js + TypeScript

- Use server components by default
- Client components only when necessary
- Use App Router, not Pages Router
- Follow Next.js 14 best practices

## State Management

- Use Zustand for global state
- React Context for theme/user context only
- No Redux in this project

## API Calls

- All API calls through our custom `apiClient` wrapper
- Include error handling with custom ErrorBoundary
- Add loading states for all async operations

## Styling

- Use Tailwind CSS exclusively
- No inline styles
- Mobile-first responsive design
- Follow our design system in /docs/design-system.md
```

### Step 3: Test with Copilot

Ask Copilot to generate code:
```
Create a product card component
```

Copilot will now follow your custom instructions and create a component using:
- Next.js 14 conventions
- TypeScript
- Tailwind CSS
- Your project's patterns

## Example 5: Using Quick Reference

The `QUICK_REFERENCE.md` file provides copy-paste ready prompts:

**Quick Test Generation**:
```
Write unit tests for this function:
[paste code]
Include happy path and edge cases
```

**Quick Optimization**:
```
Optimize this code for better performance:
[paste code]
Explain the improvements made
```

**Quick Documentation**:
```
Generate JSDoc for:
[paste code]
```

## Example 6: Team Workflow

1. **Setup Phase** (once per project):
   - Team lead customizes `.github/copilot-instructions.md`
   - Commits to repository
   - All team members benefit automatically

2. **Development Phase**:
   - Developer writes code
   - Uses chat participants for review: `@code-review check this function`
   - Uses templates for documentation
   - Uses quick reference for common tasks

3. **Review Phase**:
   - Reviewer uses code-review template to create consistent feedback
   - Developer uses refactoring template to improve based on feedback

## Tips for Maximum Benefit

1. **Start with Instructions**: Set up workspace instructions first
2. **Use Chat Participants**: Leverage specialized participants for specific tasks
3. **Keep Templates Handy**: Bookmark prompt templates for quick access
4. **Iterate**: Refine prompts based on results
5. **Share with Team**: Build a shared knowledge base of effective prompts

## Common Workflows

### New Feature Development
1. Use architecture template to design the feature
2. Use documentation template to spec out the API
3. Implement the code with Copilot assistance
4. Use testing template to create comprehensive tests
5. Use code-review template before submitting PR

### Bug Fixing
1. Use debugging template to analyze the issue
2. Fix the bug with Copilot suggestions
3. Use testing template to add regression tests
4. Use code-review template to verify the fix

### Refactoring
1. Use refactoring template to improve code structure
2. Use performance template if optimizing for speed
3. Use testing template to ensure no regression
4. Use documentation template to update docs

## Measuring Success

Track these metrics after implementing these templates:

- **Code Quality**: Fewer bugs reported
- **Development Speed**: Faster feature delivery
- **Test Coverage**: Increased coverage percentage
- **Documentation**: More comprehensive docs
- **Team Consistency**: More uniform code style
- **Onboarding**: Faster new developer ramp-up
