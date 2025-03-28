# GitHub Development Standards Guide

## Branch Naming Standards

### Branch Prefix Categories
- `feature/` - For new features and enhancements
- `bugfix/` - For bug fixes
- `hotfix/` - For urgent production fixes
- `release/` - For release branches
- `docs/` - For documentation updates
- `refactor/` - For code refactoring
- `test/` - For testing-related changes

### Branch Naming Convention
- Use lowercase letters, numbers, and hyphens only
- Format: `{prefix}/{ticket-number}-{brief-description}`
- Examples:
  - `feature/GH-123-user-authentication`
  - `bugfix/GH-456-fix-login-validation`
  - `hotfix/GH-789-security-patch`

## Commit Message Standards

### Commit Message Structure
```
<type>(<scope>): <subject>

<body>

<footer>
```

### Commit Types
- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation changes
- `style` - Formatting, missing semicolons, etc.
- `refactor` - Code refactoring
- `test` - Adding tests
- `chore` - Maintenance tasks

### Commit Message Guidelines
- Subject line should be 50 characters or less
- Use imperative mood ("Add feature" not "Added feature")
- No period at the end of subject line
- Body should explain what and why, not how
- Reference issue numbers in footer

### Examples
```
feat(auth): implement OAuth2 authentication

- Add OAuth2 provider integration
- Include user profile sync
- Setup secure token storage

Closes #123
```

## Pull Request Standards

### PR Title Format
- Format: `[Type] Brief description`
- Example: `[Feature] Add user authentication system`

### PR Description Template
```markdown
## Description
Brief description of changes

## Changes Made
- Detailed bullet points of changes

## Testing
- Description of testing performed

## Screenshots
If applicable

## Checklist
- [ ] Tests added/updated
- [ ] Documentation updated
- [ ] Code follows style guidelines
- [ ] Self-review completed
```

## Code Review Standards

### Review Checklist
1. Code Functionality
   - Meets requirements
   - Handles edge cases
   - Error handling implemented

2. Code Quality
   - Follows coding standards
   - Properly documented
   - No duplicate code
   - Efficient implementation

3. Testing
   - Unit tests included
   - Integration tests if needed
   - Edge cases covered

### Review Comments
- Be constructive and specific
- Explain reasoning for suggested changes
- Use a respectful tone
- Reference documentation or examples when applicable

## Repository Standards

### Repository Structure
```
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
├── docs/
├── src/
├── tests/
├── .gitignore
├── README.md
└── CONTRIBUTING.md
```

### Essential Files
1. README.md
   - Project description
   - Setup instructions
   - Usage examples
   - Contributing guidelines link

2. CONTRIBUTING.md
   - Development setup
   - Coding standards
   - Pull request process
   - Testing guidelines

3. .gitignore
   - IDE files
   - Build artifacts
   - Dependencies
   - Environment files

## Git Workflow

### Recommended Flow
1. Create feature branch from `develop`
2. Make changes and commit regularly
3. Keep branch updated with `develop`
4. Submit PR when ready
5. Address review comments
6. Merge after approval
7. Delete feature branch

### Protected Branches
- `main` - Production code
- `develop` - Development code
- `release/*` - Release candidates

Remember to enforce these standards through:
- Branch protection rules
- PR templates
- Automated checks
- Code review policies
