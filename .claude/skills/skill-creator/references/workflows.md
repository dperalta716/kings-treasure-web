# Workflow Patterns for Skills

## Sequential Workflows

For complex tasks that involve multiple distinct steps, structure your skill with a clear sequential workflow.

**Pattern:**

```markdown
## Workflow Overview

1. **Step 1: Initial Setup** - Prepare the environment and gather requirements
2. **Step 2: Core Processing** - Execute the main task
3. **Step 3: Validation** - Verify the output meets requirements
4. **Step 4: Finalization** - Clean up and deliver results
```

**Example: PDF Form Filling**

```markdown
## PDF Form Filling Workflow

1. **Analyze Form** - Read PDF structure and identify form fields
2. **Collect Data** - Gather required information from user or data source
3. **Fill Fields** - Populate form fields with collected data
4. **Validate** - Ensure all required fields are properly filled
5. **Save** - Generate and save the completed PDF
```

## Conditional Workflows

For tasks with decision points and multiple paths, use conditional logic to guide Claude through the appropriate branch.

**Pattern:**

```markdown
## Decision Point

If [condition], then:
- Path A steps...

Otherwise:
- Path B steps...
```

**Example: Content Creation**

```markdown
## Content Workflow

**Determine the task type:**

### If creating new content:
1. Gather requirements and specifications
2. Create outline or structure
3. Generate content
4. Review and refine

### If editing existing content:
1. Read and analyze existing content
2. Identify areas for improvement
3. Make targeted edits
4. Verify changes maintain consistency
```

Both patterns emphasize clarity and explicit step-by-step guidance to help Claude understand the intended execution flow.
