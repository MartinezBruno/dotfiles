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

