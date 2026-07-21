```markdown
# motia Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `motia` TypeScript codebase. It covers file naming, import/export styles, commit message conventions, and testing patterns. While no specific frameworks or automated workflows are detected, this guide provides best practices and suggested commands for consistent development.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `dataFetcher.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Export Style
- Use **named exports** for functions, constants, and classes.
  - Example:
    ```typescript
    // In userProfile.ts
    export function getUserProfile(id: string) { ... }
    ```

### Commit Messages
- Follow the **Conventional Commits** standard.
- Use the `chore` prefix for maintenance and non-functional changes.
  - Example:
    ```
    chore: update dependencies and fix minor lint issues
    ```

## Workflows

### Code Contribution
**Trigger:** When adding new features, fixing bugs, or making any code changes  
**Command:** `/contribute`

1. Create a new branch for your change.
2. Write code following the coding conventions above.
3. Add or update tests as needed (see Testing Patterns).
4. Commit changes using the conventional commit format.
5. Open a pull request for review.

### Dependency Update
**Trigger:** When dependencies need to be updated  
**Command:** `/update-deps`

1. Run the package manager to update dependencies (e.g., `npm update`).
2. Test the codebase to ensure compatibility.
3. Commit changes with a `chore` prefix.
   - Example: `chore: update typescript to v4.9.0`
4. Push and open a pull request.

## Testing Patterns

- Test files use the `*.test.*` naming pattern.
  - Example: `userProfile.test.ts`
- The specific testing framework is **unknown**; check existing test files for patterns.
- Place test files alongside the code they test or in a designated test directory.

**Example Test File:**
```typescript
// userProfile.test.ts
import { getUserProfile } from './userProfile';

describe('getUserProfile', () => {
  it('returns user data for a valid id', () => {
    // test implementation
  });
});
```

## Commands
| Command         | Purpose                                         |
|-----------------|-------------------------------------------------|
| /contribute     | Start the code contribution workflow            |
| /update-deps    | Update project dependencies                     |
```
