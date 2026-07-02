```markdown
# lmstudio-js Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions found in the `lmstudio-js` TypeScript repository. You'll learn about file naming, import/export styles, commit message habits, and how to write and run tests. While no specific frameworks or automated workflows are detected, this guide will help you maintain consistency and productivity in this codebase.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myModule.ts`, `userProfile.ts`

### Import Style
- Use **relative imports** for modules.
  - Example:
    ```typescript
    import { myFunction } from './myFunction';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In myModule.ts
    export function doSomething() { ... }

    // In another file
    import { doSomething } from './myModule';
    ```

### Commit Messages
- Freeform style, no enforced prefixes.
- Average commit message length: ~41 characters.
  - Example:  
    ```
    Fix bug in user authentication flow
    ```

## Workflows

### Adding a New Module
**Trigger:** When you need to add a new feature or utility.
**Command:** `/add-module`

1. Create a new TypeScript file using camelCase (e.g., `newFeature.ts`).
2. Write your code using named exports.
3. Import your module using a relative path where needed.

### Refactoring Code
**Trigger:** When improving or restructuring existing code.
**Command:** `/refactor`

1. Identify the code to refactor.
2. Update file names to camelCase if necessary.
3. Ensure all imports are relative and exports are named.
4. Update references in other files accordingly.

### Writing Tests
**Trigger:** When adding or updating features.
**Command:** `/write-test`

1. Create a test file with the pattern `*.test.*` (e.g., `myFunction.test.ts`).
2. Write your tests (testing framework is not specified; follow existing patterns).
3. Place the test file alongside the module or in a designated test directory.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `example.test.ts`).
- The testing framework is not specified; review existing test files for style and structure.
- Place test files near the code they test or in a dedicated test folder.

  Example:
  ```typescript
  // myFunction.test.ts
  import { myFunction } from './myFunction';

  describe('myFunction', () => {
    it('should return true for valid input', () => {
      expect(myFunction('valid')).toBe(true);
    });
  });
  ```

## Commands
| Command        | Purpose                                         |
|----------------|-------------------------------------------------|
| /add-module    | Scaffold a new module with proper conventions   |
| /refactor      | Refactor code to match repository standards     |
| /write-test    | Create a test file for a module or function     |
```
