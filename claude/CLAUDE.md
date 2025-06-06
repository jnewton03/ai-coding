# Claude Configuration

This file contains instructions and configurations for Claude AI and Claude Code.

## General Instructions

- Focus on clarity and conciseness in responses
- Always verify before creating new files - prefer editing existing ones
- Never create documentation files unless explicitly requested
- Follow existing code conventions and patterns in the codebase

## JIRA Ticket Template

When creating JIRA tickets, use the following template:

```
## Summary
[One-line summary of the feature/bug/task]

## Description
[Detailed description of what needs to be done]

## Acceptance Criteria
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3

## Technical Notes
[Any technical considerations or implementation details]

## Dependencies
[List any dependencies or blockers]
```

## Claude Code Best Practices

### File Operations
- Always use `Read` before `Edit` to understand context
- Use `Glob` and `Grep` for efficient file searching
- Batch multiple file reads for better performance

### Task Management
- Use TodoWrite/TodoRead tools for complex multi-step tasks
- Mark tasks as in_progress when starting
- Update task status immediately upon completion

### Code Style
- Match existing code conventions
- Verify library availability before importing
- Follow security best practices - never expose secrets

### Git Operations
- Only commit when explicitly requested
- Use meaningful commit messages that explain the "why"
- Include the Claude Code signature in commits

## MCP Server Configuration

### Atlassian MCP
- Enables direct JIRA ticket creation
- Configured for project: [PROJECT_KEY]
- Default issue types: Story, Task, Bug

### Future MCP Integrations
- Slack: For notifications and status updates
- Docker: Local development environments
- Internal tools: Company-specific integrations

## Slash Commands

### Useful Commands
- `/help` - Get help with Claude Code
- `/model` - Check or change the current model
- `/memory` - Manage conversation memory

## References

- [Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)
- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)