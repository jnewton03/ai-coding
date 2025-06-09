# AI Development Configs

Version-controlled configurations for AI development tools.

## 🚀 Quick Setup

```bash
# Claude configuration
ln -sf ~/path/to/repo/claude/CLAUDE.md ~/.claude/CLAUDE.md

# Cursor rules (copy to project)
cp ~/path/to/repo/cursor/.cursorrules ./
```

## 📁 Contents

- **`claude/`** - Claude AI configurations with 11 core principles
- **`cursor/`** - Cursor IDE rules and settings  
- **`mcp-servers/`** - Model Context Protocol server configs
- **`best-practices/`** - Simple development guidelines

## 🔗 Tool-Specific Usage

### Claude Configuration
```bash
# Link global configuration
ln -sf ~/path/to/repo/claude/CLAUDE.md ~/.claude/CLAUDE.md
```

### Cursor Rules
```bash
# Copy to project directory
cp ~/path/to/repo/cursor/.cursorrules ./
```

### MCP Servers
See individual directories in `mcp-servers/` for setup instructions.

## 🎯 Philosophy

This repository follows the KISS principle: Keep It Simple, Stupid. 
- Minimal configuration files
- Clear setup instructions  
- Focus on practical usage over documentation
- Easy to understand and maintain

## 📚 Additional Resources

- [Best Practices](best-practices/README.md) - Simple development guidelines
- [Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)
- [MCP Protocol](https://modelcontextprotocol.io)