## Repository-Specific Instructions
- **ALWAYS check for CLAUDE.md file in the current project directory**
- If project CLAUDE.md exists (or local version as CLAUDE.local.md), follow those instructions in addition to these global ones
- Project-specific instructions take precedence over global ones

# Commit Message Convention

Use Conventional Commits format: `type(scope): description`

## Commit Process
- **ALWAYS ask user to confirm the commit message before executing**
- Generate the message following the convention below
- Show the proposed message and wait for user approval before creating the commit
- NEVER add Claude as co-author or any other claude data to the commit

## Types
- **feat**: New features
- **fix**: Bug fixes
- **docs**: Documentation changes
- **style**: Code style changes (formatting, semicolons, etc.)
- **refactor**: Code refactoring without changing functionality
- **test**: Adding or modifying tests
- **chore**: Build tasks, dependency updates, maintenance

## Scope
- Use lowercase
- Be specific but concise
- Examples: auth, ui, api, database, config, test, components

## Description
- Use lowercase
- Start with verb in imperative mood
- No period at the end
- Keep under 50 characters

## Examples
feat(auth): add login validation
fix(ui): correct button alignment
docs(readme): update setup instructions
chore(deps): bump react to 18.2.0
refactor(api): simplify user service
test(calc): add completion message
style(components): fix indentation

# Git Flow Instructions

This project uses Git Flow workflow with the **git-flow extension**.

## Setup
- Verify git-flow is initialized: `git flow init`
- Use git-flow extension commands for all operations

## Git Flow Commands
- **Features:**
  - Start: `git flow feature start <name>`
  - Finish: `git flow feature finish <name>`
  - Publish: `git flow feature publish <name>`

- **Releases:**
  - Start: `git flow release start <version>`
  - Finish: `git flow release finish <version>`

- **Hotfixes:**
  - Start: `git flow hotfix start <version>`
  - Finish: `git flow hotfix finish <version>`

## Branch Naming Process
- **ALWAYS ask user to confirm branch name before creating**
- Propose a descriptive name based on the task/feature
- Wait for user approval or modification before executing git-flow commands
- Use kebab-case for branch names (e.g., user-authentication, fix-login-bug)

## Workflow Rules
1. **Always use git-flow commands** instead of manual git operations
2. Features branch from develop, merge back to develop
3. Releases branch from develop, merge to main and develop
4. Hotfixes branch from main, merge to main and develop
5. Use descriptive names for features/releases/hotfixes

## Branch Analysis
Check current branch and suggest appropriate git-flow actions:
- On feature branch: suggest `git flow feature finish`
- On develop: suggest `git flow feature start` or `git flow release start`
- On main: suggest `git flow hotfix start`

Claude Code Commands
Claude Code handles naming automatically
claude "create a feature for user login system"
→ Proposes: git flow feature start user-login-system
→ Waits for your confirmation

# Claude Code generates commits automatically
claude "commit these changes"
→ Analyzes changes
→ Do not adds Claude as co-author
→ Proposes: feat(auth): add user login validation
→ Waits for your confirmation
