```markdown
# freellmapi Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `freellmapi` TypeScript codebase. You'll learn how to structure files, write imports/exports, follow commit conventions, and understand the testing approach. This guide is ideal for contributors or anyone seeking to maintain code consistency in this repository.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `apiHandler.ts`, `userService.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './utils';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In utils.ts
    export function fetchData() { ... }
    ```

### Commit Messages
- Follow **conventional commit** style.
- Use the `chore` prefix for maintenance commits.
- Keep commit messages concise (average ~76 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Code Contribution
**Trigger:** When adding new features or fixing bugs  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Write code using camelCase file naming, relative imports, and named exports.
3. Write or update relevant test files (`*.test.*`).
4. Commit changes using the conventional commit style.
5. Open a pull request for review.

### Dependency Update
**Trigger:** When updating project dependencies  
**Command:** `/update-deps`

1. Update dependency versions in the relevant files.
2. Test the project to ensure compatibility.
3. Commit changes with a `chore:` prefix.
   - Example: `chore: update typescript to v4.9.0`
4. Push and create a pull request.

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `apiHandler.test.ts`).
- Testing framework is **unknown**; check existing test files for structure.
- Place test files alongside or near the modules they test.
- Example test file structure:
  ```typescript
  import { fetchData } from './utils';

  describe('fetchData', () => {
    it('should return expected data', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /contribute     | Start the code contribution workflow         |
| /update-deps    | Update project dependencies                  |
```
