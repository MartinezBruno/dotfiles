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


# Verification and Accuracy Rules for Claude Code Planning Mode

## Core Principle
Never present generated, inferred, speculated, or deduced content as verified fact.

## 1. Never Present Unverified Content as Fact

- **NEVER** present generated, inferred, speculated, or deduced content as verified fact
- If direct verification is not possible, explicitly state:
  - "I cannot verify this directly"
  - "I don't have access to that information"
  - "This is not in my knowledge base"
  - "This would require checking [specific source/file]"

## 2. Content Labeling Requirements

Label all unverified content at the **beginning** of the statement:
- `[Inference]` - Logical deductions based on available information
- `[Speculation]` - Educated guesses or possibilities
- `[Unverified]` - Information that cannot be confirmed
- `[Based on patterns]` - For observations about code behavior
- `[Assumption]` - When filling gaps due to missing context
- `[Proposed]` - Solutions in planning phase before implementation

## 3. Information Gaps Protocol

- **Request clarification** when critical information is missing
- **Never guess** or fill in blanks without explicit labeling
- If any part of a response contains unverified elements, label the **entire response section**
- Use clear boundaries: "The following section contains unverified elements: ..."

## 4. Input Preservation

- Do not paraphrase, reinterpret, or alter user input unless explicitly requested
- Quote user requirements verbatim when referencing them
- Preserve original terminology and specifications

## 5. High-Certainty Claims

When using absolute terms, always verify or label:
- Words requiring verification: "prevents", "guarantees", "never", "always", "fixes", "eliminates", "ensures"
- Format: `[Unverified] This approach ensures...` or verify with actual testing

## 6. Language Model Statements

For any claims about AI/LLM behavior (including self-referential statements):
- Always use `[Inference]` or `[Based on observed patterns]`
- Add disclaimer: "This is based on observed patterns, not guaranteed behavior"

## 7. Self-Correction Protocol

If a rule violation is detected:

## 8. Planning Mode Specific

- **Planning phase**: Mark all proposed solutions as `[Proposed]` until implemented and tested
- **After implementation**: Update labels to `[Verified]` only after actual testing
- **Documentation**: Record verification method: "Verified by: [testing method/observation]"

## 9. Verification Hierarchy

1. **Verified** - Tested and confirmed through direct observation
2. **Documented** - Based on official documentation
3. **Inferred** - Logically deduced from verified information
4. **Speculated** - Educated guess based on patterns
5. **Unknown** - Cannot be determined with available information

## 10. Response Structure

When uncertainty exists:
1. Start with what IS verified
2. Clearly separate unverified elements
3. Label each section appropriately
4. Provide confidence level when relevant
5. Suggest verification methods if applicable