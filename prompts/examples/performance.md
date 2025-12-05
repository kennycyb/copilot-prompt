# Performance Optimization Prompt Template

Use this template when you need to optimize code for better performance.

## Prompt for Performance Analysis

```
Analyze the performance of this code and suggest optimizations:

[PASTE YOUR CODE HERE]

Consider:
1. Time complexity
2. Space complexity
3. Algorithm efficiency
4. Database query optimization
5. Memory usage
6. Network calls
7. Caching opportunities
8. Parallel processing possibilities

Provide:
- Current performance issues
- Optimized code
- Explanation of improvements
- Expected performance gain
```

## Prompt for Database Query Optimization

```
Optimize this database query:

Query:
[PASTE QUERY]

Schema:
[DESCRIBE RELEVANT TABLES AND INDEXES]

Current performance:
- Execution time: [TIME]
- Rows scanned: [NUMBER]

Provide:
1. Optimized query
2. Index recommendations
3. Explain plan analysis
4. Expected improvement
```

## Prompt for Algorithm Optimization

```
Improve the time/space complexity of this algorithm:

[PASTE CODE]

Current complexity: O([CURRENT_COMPLEXITY, e.g., n²])
Target: [DESIRED COMPLEXITY or "best possible"]

Provide:
1. More efficient algorithm
2. Complexity analysis (before/after)
3. Trade-offs explanation
4. When to use which approach
```

## Prompt for Frontend Performance

```
Optimize this frontend code for better performance:

[PASTE CODE]

Focus on:
1. Rendering performance
2. Bundle size reduction
3. Lazy loading opportunities
4. Image optimization
5. Code splitting
6. Memoization
7. Virtual scrolling (if applicable)
8. Debouncing/throttling
```

## Prompt for API Performance

```
Optimize this API endpoint for better performance:

[PASTE CODE]

Current issues:
- [ISSUE 1, e.g., "slow response time"]
- [ISSUE 2, e.g., "high CPU usage"]

Consider:
1. Query optimization
2. Caching strategies
3. Pagination
4. Compression
5. Connection pooling
6. Async processing
```

## Example Usage

```
Analyze the performance of this code and suggest optimizations:

function findDuplicates(arr) {
  const duplicates = [];
  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[i] === arr[j] && !duplicates.includes(arr[i])) {
        duplicates.push(arr[i]);
      }
    }
  }
  return duplicates;
}

Array size: typically 10,000+ elements
Current execution time: ~5 seconds

Provide a solution with better time complexity.
```

## Prompt for Caching Strategy

```
Design a caching strategy for this code:

[PASTE CODE]

Context:
- Data changes: [frequency]
- Cache invalidation needs: [when]
- Cache size constraints: [if any]

Recommend:
1. What to cache
2. Cache type (memory/Redis/CDN/etc)
3. TTL (time to live)
4. Cache invalidation strategy
5. Implementation code
```

## Prompt for Load Testing Scenarios

```
Suggest load testing scenarios for:

Application: [DESCRIPTION]
Critical paths: [LIST PATHS]
Expected load: [NUMBERS]

Include:
1. Test scenarios
2. Performance metrics to track
3. Acceptance criteria
4. Bottleneck prediction
```

## Profiling Request

```
Help me profile this code to find performance bottlenecks:

[PASTE CODE]

Language/Framework: [SPECIFY]

Suggest:
1. Profiling tools to use
2. What metrics to measure
3. How to interpret results
4. Common bottlenecks to look for
```

## Tips

- Provide context about data size and frequency
- Mention current performance metrics if available
- Specify performance targets
- Include information about hardware/environment constraints
- Ask about trade-offs (e.g., speed vs memory)

## Common Performance Patterns

### Memoization
```
Add memoization to this function:
[PASTE CODE]
```

### Lazy Loading
```
Implement lazy loading for this component/module:
[PASTE CODE]
```

### Debouncing/Throttling
```
Add debouncing to this event handler:
[PASTE CODE]
Target delay: [MS]
```

### Batch Processing
```
Convert this to process items in batches:
[PASTE CODE]
Batch size: [NUMBER]
```

## Performance Metrics to Request

- Time complexity (Big O notation)
- Space complexity
- Actual execution time
- Memory usage
- Database query count
- Network request count
- Bundle size (for frontend)
- First Contentful Paint (FCP)
- Time to Interactive (TTI)
- Largest Contentful Paint (LCP)
