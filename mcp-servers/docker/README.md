# Docker-based MCP Servers

This directory contains Docker configurations for running MCP servers locally.

## Quick Start

1. **Copy environment file**
   ```bash
   cp .env.example .env
   ```

2. **Configure environment variables**
   Edit `.env` with your actual credentials

3. **Start services**
   ```bash
   # Start only Atlassian MCP
   docker-compose up -d mcp-atlassian
   
   # Start all services (with profiles)
   docker-compose --profile slack --profile github up -d
   ```

## Available Services

### Atlassian MCP (Active)
- Port: 3001
- Integrates with JIRA and Confluence
- Requires API token from Atlassian

### Slack MCP (Planned)
- Port: 3002
- Profile: `slack`
- Will enable Slack messaging and notifications

### GitHub MCP (Planned)
- Port: 3003
- Profile: `github`
- Will provide repository and issue management

### Internal Tools MCP (Planned)
- Port: 3004
- Profile: `internal`
- Custom integration for company-specific tools

## Configuration

### Claude Desktop Integration
Add to your Claude Desktop configuration:

```json
{
  "mcpServers": {
    "atlassian-docker": {
      "command": "docker",
      "args": ["exec", "-i", "mcp-atlassian", "node", "/app/server.js"]
    }
  }
}
```

### Health Checks
All services include health checks:
```bash
# Check service health
curl http://localhost:3001/health
```

## Development

### Building Custom MCP
```bash
# Build internal MCP
docker-compose build mcp-internal
```

### Logs
```bash
# View logs for a service
docker-compose logs -f mcp-atlassian
```

### Debugging
```bash
# Access container shell
docker exec -it mcp-atlassian /bin/sh
```

## Security Best Practices

1. **Never commit `.env` file**
2. **Use Docker secrets for production**
3. **Limit container permissions**
4. **Regular security updates**
5. **Network isolation**

## Troubleshooting

### Port Conflicts
If ports are already in use:
1. Change port mapping in docker-compose.yml
2. Update Claude Desktop configuration

### Connection Issues
1. Verify Docker is running
2. Check container logs
3. Ensure environment variables are set
4. Test health endpoint

### Permission Errors
1. Check API token validity
2. Verify service accounts have required permissions
3. Review Docker user permissions