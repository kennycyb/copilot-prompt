# Architecture and Design Prompt Template

Use this template when you need help with system design, architecture decisions, or technical planning.

## Prompt for System Design

```
I need to design a system with the following requirements:

Requirements:
- [REQUIREMENT 1]
- [REQUIREMENT 2]
- [REQUIREMENT 3]

Constraints:
- [CONSTRAINT 1]
- [CONSTRAINT 2]

Please provide:
1. High-level architecture diagram (describe components and their relationships)
2. Technology stack recommendations
3. Data flow explanation
4. Scalability considerations
5. Potential challenges and solutions
```

## Prompt for Design Pattern Selection

```
I need to solve the following problem:

Problem: [DESCRIBE THE PROBLEM]

Current approach: [IF ANY]

Please:
1. Suggest appropriate design patterns
2. Explain why each pattern fits
3. Show example implementation
4. Discuss trade-offs
```

## Prompt for Database Schema Design

```
I need to design a database schema for:

Use case: [DESCRIBE USE CASE]

Entities: [LIST ENTITIES]

Relationships: [DESCRIBE RELATIONSHIPS]

Query patterns: [COMMON QUERIES]

Please provide:
1. Entity-Relationship diagram (describe tables and relationships)
2. Table schemas with fields and types
3. Indexing strategy
4. Normalization considerations
5. Migration approach
```

## Prompt for API Design

```
I need to design a REST API for:

Purpose: [DESCRIBE PURPOSE]

Resources: [LIST RESOURCES]

Operations needed:
- [OPERATION 1]
- [OPERATION 2]

Please provide:
1. Endpoint structure
2. HTTP methods and paths
3. Request/response formats
4. Error handling approach
5. Authentication/authorization strategy
6. Versioning strategy
```

## Prompt for Microservices Architecture

```
I'm planning to break down a monolith into microservices:

Current system: [DESCRIBE CURRENT SYSTEM]

Bounded contexts identified:
- [CONTEXT 1]
- [CONTEXT 2]

Please help with:
1. Service boundaries and responsibilities
2. Communication patterns (sync/async)
3. Data management strategy
4. Service discovery approach
5. Deployment strategy
6. Monitoring and observability
```

## Example Usage

```
I need to design a notification system with these requirements:

Requirements:
- Support email, SMS, and push notifications
- Handle 10,000 notifications per minute
- Retry failed notifications
- Track delivery status
- Support scheduled notifications

Please provide:
1. Architecture design with queue-based approach
2. Component breakdown
3. Technology recommendations
4. Failure handling strategy
5. Monitoring approach
```

## Tips

- Be clear about functional and non-functional requirements
- Mention scale expectations (users, data volume, traffic)
- Include any existing systems that need to be integrated
- Specify any technology preferences or constraints
- Mention compliance or security requirements
