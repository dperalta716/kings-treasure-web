# Output Patterns for Skills

Two main approaches for ensuring consistent, high-quality outputs:

## 1. Template Pattern

Provide structured formats for responses. Adjust strictness based on requirements:

### Strict Templates

Use for rigid requirements like API responses or data formats:

```markdown
## Output Format

```json
{
  "status": "[success|error]",
  "data": {
    "field1": "value1",
    "field2": "value2"
  },
  "message": "Description of result"
}
```
```

### Flexible Templates

Use when adaptation adds value:

```markdown
## Suggested Report Structure

**Title**: [Clear, descriptive title]

**Executive Summary**: [1-2 paragraphs highlighting key points]

**Key Findings**:
- Finding 1
- Finding 2
- Finding 3

**Recommendations**:
1. Recommendation with rationale
2. Recommendation with rationale

**Conclusion**: [Brief wrap-up]

*Note: Adapt this structure based on context and requirements*
```

## 2. Examples Pattern

Demonstrate desired output quality through input/output pairs. Examples help Claude understand the desired style and level of detail more clearly than descriptions alone.

**Example: Commit Messages**

```markdown
## Commit Message Format

Use the conventional commits format:

**Input**: Added user authentication with JWT tokens and password hashing

**Output**:
```
feat(auth): implement JWT-based user authentication

- Add JWT token generation and validation
- Implement bcrypt password hashing
- Create login and registration endpoints
- Add auth middleware for protected routes
```

**Input**: Fixed bug where pagination broke on mobile devices

**Output**:
```
fix(pagination): resolve mobile display issues

- Fix responsive breakpoints for pagination controls
- Adjust touch target sizes for mobile
- Test pagination across various screen sizes
```
```

## Combining Patterns

For best results, combine templates with examples:

- **Templates** establish structure and required elements
- **Examples** clarify tone, detail level, and stylistic expectations

This dual approach ensures both consistency and quality in outputs.
