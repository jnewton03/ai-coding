# AI Tooling Journey

This repository tracks my journey with AI tooling, documenting experiences, configurations, and best practices for various AI-powered development tools.

## Timeline & Evolution

### Phase 1: ChatGPT (Web UI & Mac App)
- **Use Case**: JIRA ticket creation workflow
- **Process**: 
  - Provided JIRA ticket template to ChatGPT
  - Gave user story summaries
  - Tweaked output and copied to JIRA
- **Plan**: Downgraded from $20/month paid plan to free tier

### Phase 2: GitHub Copilot with VSCode
- **Use Case**: Code assistance and chat mode
- **Benefits**: 
  - Multiple model selection options
  - Integrated VSCode experience
- **GitHub UI Features**:
  - Copilot as code reviewer
  - PR summary generation

### Phase 3: Claude AI (Current)
- **Mac App**: Replaced ChatGPT for JIRA ticket workflow
- **Claude Code**: Game-changing CLI tool
- **Plan**: Upgraded to $100/month MAX plan
- **MCP Integration**: 
  - Added Atlassian MCP server
  - Direct JIRA ticket creation from Claude

## Repository Structure

```
├── README.md                 # This file
├── claude/                   # Claude-specific configurations
│   ├── CLAUDE.md            # Claude instructions
│   └── slash-commands/      # Custom slash commands
├── cursor/                   # Cursor IDE configurations
├── github-copilot/          # GitHub Copilot settings
├── chatgpt/                 # ChatGPT templates
├── mcp-servers/             # MCP server configurations
│   ├── atlassian/          # Atlassian MCP setup
│   └── docker/             # Local Docker MCP configs
└── docs/                    # Best practices and guidelines
    └── best-practices.md   # AI tooling best practices
```

## Next Steps

1. **Local MCP Development**: Set up Docker-based MCPs for:
   - Atlassian integration
   - Slack integration
   - Other internal tooling

2. **Documentation**: Create comprehensive guidelines for company-wide adoption

3. **Best Practices**: Document learnings from [Anthropic's Claude Code best practices](https://www.anthropic.com/engineering/claude-code-best-practices)

## Tools Overview

### Active Tools
- **Claude AI** (MAX Plan - $100/month): Primary AI assistant
- **Claude Code**: CLI development tool
- **Atlassian MCP**: Direct JIRA integration

### Previous/Reduced Usage
- **ChatGPT** (Free tier): Previously used for JIRA tickets
- **GitHub Copilot**: Code assistance in VSCode

## Contributing

This repository serves as both personal documentation and a resource for team adoption of AI tooling. Contributions and suggestions are welcome.

## License

This repository contains personal configurations and documentation. Please respect privacy and company policies when using or sharing content.