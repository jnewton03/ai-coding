# AI Tooling Best Practices

A collection of best practices and guidelines for effectively using AI development tools.

## General Principles

### 1. Context is King
- Always provide clear, specific context
- Include relevant code snippets, error messages, and requirements
- Reference specific files and line numbers when discussing code

### 2. Iterative Development
- Break complex tasks into smaller, manageable steps
- Review and test each change before proceeding
- Use version control to track AI-assisted changes

### 3. Tool Selection
- Choose the right tool for the task:
  - **Claude Code**: Complex file operations, refactoring
  - **GitHub Copilot**: In-line code suggestions
  - **Claude/ChatGPT**: Planning, documentation, explanations

## Claude Code Best Practices

### File Operations
```bash
# Good: Read before edit
claude read src/app.js
claude edit src/app.js

# Bad: Edit without context
claude edit src/app.js
```

### Task Management
- Use todo lists for multi-step operations
- Mark tasks as completed immediately
- Keep one task in_progress at a time

### Commit Messages
- Let Claude analyze changes before committing
- Ensure messages explain "why" not just "what"
- Review auto-generated messages before accepting

## JIRA Integration Tips

### Template Usage
1. Create a standard template in CLAUDE.md
2. Provide user story summary
3. Review and adjust generated ticket
4. Use MCP for direct creation when available

### Effective Summaries
- Start with the business value
- Include technical context
- List clear acceptance criteria
- Note any dependencies upfront

## MCP Server Best Practices

### Security
- Never store credentials in config files
- Use environment variables for sensitive data
- Implement proper access controls
- Regular security audits

### Docker Setup
```yaml
# Example docker-compose for local MCPs
version: '3.8'
services:
  mcp-atlassian:
    image: mcp/atlassian:latest
    environment:
      - JIRA_URL=${JIRA_URL}
      - JIRA_TOKEN=${JIRA_TOKEN}
    ports:
      - "3000:3000"
```

## Code Review with AI

### Pre-Review Checklist
- [ ] Run linters and formatters
- [ ] Execute test suite
- [ ] Check for security issues
- [ ] Verify no secrets exposed

### AI-Assisted Review
1. Use GitHub Copilot for automated review
2. Ask Claude for specific concerns
3. Focus AI on complex logic
4. Human review remains essential

## Prompt Engineering

### Effective Prompts
```
# Good
"Refactor the getUserData function in src/api/users.js to use async/await 
instead of promises, maintaining all error handling"

# Bad
"Fix the user function"
```

### Context Inclusion
- Current file path
- Related files
- Error messages
- Expected behavior
- Constraints or requirements

## Performance Optimization

### Batch Operations
- Group related file reads
- Combine similar edits
- Use search tools efficiently

### Token Management
- Be concise in prompts
- Request specific outputs
- Use file paths instead of pasting code

## Team Collaboration

### Documentation
- Document AI tool configurations
- Share effective prompts
- Maintain best practices guide
- Regular knowledge sharing sessions

### Standardization
- Agree on tool stack
- Create shared templates
- Establish review processes
- Define AI usage policies

## Common Pitfalls to Avoid

1. **Over-reliance**: AI assists, doesn't replace thinking
2. **Context Loss**: Always verify AI understands requirements
3. **Security Risks**: Never share sensitive data
4. **Quality Drift**: Maintain code standards
5. **Documentation Gaps**: Keep human-readable docs

## Measuring Success

### Metrics to Track
- Development velocity
- Code quality metrics
- Bug reduction rate
- Time saved on repetitive tasks

### Continuous Improvement
- Regular retrospectives
- Tool evaluation cycles
- Process refinement
- Team feedback loops

## Resources

- [Anthropic Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)
- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [MCP Protocol Specification](https://modelcontextprotocol.io)
- Internal wiki: [Your Company AI Guidelines]

## Contributing

To add to these best practices:
1. Document your experience
2. Include specific examples
3. Cite sources when applicable
4. Submit PR for team review