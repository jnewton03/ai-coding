# Atlassian MCP Server Configuration

This directory documents the Atlassian MCP integration for Claude AI. The **recommended approach** is using Atlassian's official remote MCP server (beta).

## 🚀 Recommended: Remote MCP Server (Beta)

Atlassian provides an official remote MCP server that requires no local setup:

### Setup Instructions
1. Follow the official guide: [Using the Atlassian Remote MCP Server (beta)](https://community.atlassian.com/forums/Atlassian-Platform-articles/Using-the-Atlassian-Remote-MCP-Server-beta/ba-p/3005104)
2. Configure in Claude Desktop settings
3. No Docker or local installation required!

### Benefits
- ✅ Zero maintenance - Atlassian handles updates
- ✅ No local resources needed
- ✅ Official support from Atlassian
- ✅ Automatic security updates
- ✅ Direct API integration

## 🔧 Alternative: Local MCP Server

If you need custom modifications or prefer local control:

1. **Environment Variables**
   ```bash
   export ATLASSIAN_API_TOKEN="your-api-token"
   export JIRA_BASE_URL="https://your-domain.atlassian.net"
   export JIRA_DEFAULT_PROJECT="PROJ"
   export CONFLUENCE_BASE_URL="https://your-domain.atlassian.net/wiki"
   export CONFLUENCE_DEFAULT_SPACE="SPACE"
   ```

2. **Generate API Token**
   - Go to https://id.atlassian.com/manage-profile/security/api-tokens
   - Create new API token
   - Store securely in environment

3. **Configure Claude Desktop (Local)**
   ```json
   {
     "mcpServers": {
       "atlassian": {
         "command": "npx",
         "args": ["@modelcontextprotocol/server-atlassian"],
         "env": {
           "ATLASSIAN_API_TOKEN": "your-token",
           "JIRA_BASE_URL": "https://your-domain.atlassian.net"
         }
       }
     }
   }
   ```

4. **Docker Option**
   See [Docker setup](../docker/README.md) for containerized deployment

## Usage Examples

### Create JIRA Issue
```
Claude, create a JIRA story for implementing user authentication with the following details:
- OAuth2 integration
- Session management
- Password reset flow
```

### Search Issues
```
Find all open bugs assigned to me in the current sprint
```

### Update Issue
```
Add a comment to PROJ-123 with the deployment status
```

## Supported Operations

- **Create Issue**: Stories, Tasks, Bugs, Epics
- **Update Issue**: Modify fields, add comments
- **Search Issues**: JQL queries
- **Get Issue**: Retrieve full details
- **Transition Issue**: Move through workflow

## Security Notes

- Never commit API tokens
- Use environment variables only
- Rotate tokens regularly
- Limit token permissions to required scope

## Troubleshooting

1. **Connection Failed**
   - Verify API token is valid
   - Check network connectivity
   - Ensure correct base URL

2. **Permission Denied**
   - Verify token has required permissions
   - Check project access rights
   - Confirm issue type availability

3. **Field Errors**
   - Review custom field configurations
   - Validate required fields
   - Check field permissions