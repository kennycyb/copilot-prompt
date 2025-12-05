# Migration and Upgrade Prompt Template

Use this template when you need to migrate code between versions, frameworks, or languages.

## Prompt for Framework Migration

```
Help me migrate this code from [OLD FRAMEWORK] to [NEW FRAMEWORK]:

[PASTE YOUR CODE]

Requirements:
1. Maintain existing functionality
2. Follow [NEW FRAMEWORK] best practices
3. Update dependencies
4. Preserve business logic
5. Add migration notes for team

Provide:
- Migrated code
- List of breaking changes
- New dependencies needed
- Testing recommendations
```

## Prompt for Language Migration

```
Convert this code from [SOURCE LANGUAGE] to [TARGET LANGUAGE]:

[PASTE CODE]

Maintain:
- Same functionality
- Similar code structure where possible
- Idiomatic [TARGET LANGUAGE] patterns

Include:
1. Converted code
2. Explanation of key differences
3. Dependency equivalents
4. Performance considerations
```

## Prompt for Version Upgrade

```
Upgrade this code from [LIBRARY/FRAMEWORK] version [OLD] to version [NEW]:

[PASTE CODE]

Address:
1. Deprecated APIs
2. Breaking changes
3. New recommended patterns
4. Performance improvements available
5. Security updates

Include migration guide and any necessary code changes.
```

## Prompt for Database Migration

```
Help me migrate this database schema:

Current: [DATABASE TYPE/VERSION]
Target: [DATABASE TYPE/VERSION]

Schema:
[PASTE SCHEMA OR DESCRIBE]

Include:
1. Migration scripts
2. Data transformation logic
3. Index migration
4. Rollback plan
5. Performance considerations
```

## Example Usage - React Migration

```
Help me migrate this code from React Class Component to React Hooks:

class UserProfile extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      user: null,
      loading: true
    };
  }

  componentDidMount() {
    this.fetchUser();
  }

  fetchUser = async () => {
    const user = await api.getUser(this.props.userId);
    this.setState({ user, loading: false });
  }

  render() {
    const { user, loading } = this.state;
    if (loading) return <Spinner />;
    return <div>{user.name}</div>;
  }
}

Follow React hooks best practices.
```

## Example Usage - Python Migration

```
Convert this Python 2 code to Python 3:

import urllib2

def fetch_data(url):
    response = urllib2.urlopen(url)
    return response.read()

data = fetch_data('http://api.example.com')
print data

Update all Python 2 specific syntax and libraries.
```

## Prompt for API Version Migration

```
Migrate API calls from version [OLD] to version [NEW]:

Current API calls:
[PASTE CODE WITH API CALLS]

API changes documentation:
[LINK OR PASTE KEY CHANGES]

Provide:
1. Updated API calls
2. Request/response format changes
3. New error handling
4. Backward compatibility approach
```

## Prompt for Build Tool Migration

```
Migrate build configuration from [OLD TOOL] to [NEW TOOL]:

Current configuration:
[PASTE CONFIG]

Requirements:
- Same build output
- Equivalent plugins/loaders
- Similar dev experience
- Improved performance if possible

Provide complete new configuration.
```

## Prompt for Testing Framework Migration

```
Migrate these tests from [OLD FRAMEWORK] to [NEW FRAMEWORK]:

[PASTE TESTS]

Maintain:
- Same test coverage
- Similar test structure
- All assertions

Update to use [NEW FRAMEWORK] conventions and best practices.
```

## Prompt for Authentication Migration

```
Migrate authentication from [OLD SYSTEM] to [NEW SYSTEM]:

Current implementation:
[PASTE CODE]

Requirements:
- Maintain security level
- Support existing users
- Minimal downtime
- Data migration plan

Include:
1. New authentication code
2. User data migration script
3. Transition strategy
4. Rollback plan
```

## Incremental Migration Template

```
Create a plan for incrementally migrating from [OLD] to [NEW]:

Codebase size: [SIZE/COMPLEXITY]
Timeline: [AVAILABLE TIME]
Team size: [NUMBER]
Constraints: [LIST CONSTRAINTS]

Provide:
1. Step-by-step migration plan
2. Coexistence strategy (running both systems)
3. Risk mitigation
4. Testing strategy
5. Rollback points
```

## Example - ORM Migration

```
Migrate these Sequelize models to Prisma:

const User = sequelize.define('User', {
  id: {
    type: DataTypes.INTEGER,
    primaryKey: true,
    autoIncrement: true
  },
  email: {
    type: DataTypes.STRING,
    unique: true,
    allowNull: false
  },
  posts: {
    type: DataTypes.VIRTUAL,
    get() {
      return this.getPosts();
    }
  }
});

Include Prisma schema and migration files.
```

## Tips

- Always ask for a migration plan for large codebases
- Request both forward and rollback strategies
- Ask about data migration separately from code migration
- Specify timeline and constraints
- Request testing recommendations
- Ask for potential risks and mitigation strategies

## Migration Checklist Template

```
Create a migration checklist for moving from [OLD] to [NEW]:

Include:
- [ ] Dependency updates
- [ ] Code changes needed
- [ ] Configuration updates
- [ ] Database migrations
- [ ] Test updates
- [ ] Documentation updates
- [ ] Deployment changes
- [ ] Team training needs
- [ ] Rollback procedure
- [ ] Success criteria
```

## Common Migration Scenarios

### Package Manager Migration
```
Migrate from npm to [yarn/pnpm]:

Requirements:
- Convert lock files
- Update CI/CD scripts
- Update documentation

Provide step-by-step migration instructions.
```

### State Management Migration
```
Migrate from Redux to Zustand/Context API:
- Current Redux setup: [PASTE]
- Maintain same state structure
```

### CSS Framework Migration
```
Migrate styles from [OLD FRAMEWORK] to [NEW FRAMEWORK]:
- Current styles: [PASTE]
- Maintain visual appearance
```

## Post-Migration Validation

```
After migrating to [NEW SYSTEM], help me validate:

1. Create test cases to verify equivalence
2. Performance comparison approach
3. Edge cases to check
4. Monitoring metrics to track
```
