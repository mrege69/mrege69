I’ll need to search for the most current information on integrating MCP servers with Claude AI using Docker Desktop, as this involves specific implementation details that may have been updated recently.​​​​​​​​​​​​​​​​

# Integrating MCP Servers with Claude Desktop Using Docker Desktop

Based on the latest information, here’s a comprehensive guide to integrate MCP (Model Context Protocol) servers locally using Docker Desktop with Claude Desktop:

## Prerequisites

1. **Docker Desktop** (version 4.48 or newer)
1. **Claude Desktop** - Download from <https://claude.ai/desktop>
1. macOS 11+ or Windows 10/11
1. At least 8GB RAM (16GB recommended)

## Step 1: Enable Docker MCP Toolkit

1. Open Docker Desktop settings and select Beta features 
1. Select “Enable Docker MCP Toolkit” 
1. Click “Apply” and restart Docker Desktop if prompted

## Step 2: Install Claude Desktop

1. Download Claude Desktop from <https://claude.ai/desktop>
1. Install and sign in with your Anthropic account
1. Complete the initial setup

## Step 3: Access MCP Toolkit in Docker Desktop

1. Launch Docker Desktop and select “Extensions” from the left menu 
1. The MCP Toolkit should now be available in the left sidebar

- It may also appear as “Labs: AI Tools for Devs” (recently renamed to Docker MCP Toolkit)

1. Click on “MCP Toolkit” to open the interface

## Step 4: Browse and Add MCP Servers

The MCP Toolkit allows you to enable MCP servers directly through Docker Desktop with straightforward setup, secure execution, and reproducible results 

1. In the MCP Toolkit, select the **“Catalog”** tab
1. Browse available MCP servers such as:

- **GitHub** - Repository management
- **Puppeteer** - Web automation and screenshots
- **Filesystem** - Local file access
- **Kubernetes** - Cluster management
- **Slack** - Team communication
- **Firecrawl** - Web scraping
- **Docker Hub** - Container image management

1. Click the **”+”** icon next to any server to add it
1. Configure required credentials (API keys, tokens) in the server’s **Configuration** tab

## Step 5: Connect Claude Desktop to MCP Toolkit

1. In Docker Desktop’s MCP Toolkit, click “MCP Toolkit” in the left sidebar and click “Connect” under Claude Desktop 
1. This automatically adds configuration to Claude Desktop’s `claude_desktop_config.json` file 
1. Completely quit and restart Claude Desktop

## Step 6: Verify the Connection

1. Open Claude Desktop
1. Check the “Search and tools” menu in the chat input - you should see the MCP_DOCKER server listed and enabled 
1. Alternatively, go to **Claude > Settings > Developer > Edit Config** to view the configuration file

You should see an entry like this in the config:

```json
{
  "mcpServers": {
    "MCP_DOCKER": {
      "command": "docker",
      "args": ["mcp", "gateway", "run"]
    }
  }
}
```

## Step 7: Test Your Setup

Try these example prompts in Claude Desktop:

- “Use the GitHub MCP server to show me my open pull requests”
- “Take a screenshot of <https://example.com> using Puppeteer”
- “List all my Kubernetes pods”
- “Search my filesystem for files containing ‘project’”

Claude will request your permission before executing any actions.

## Key Benefits of Using Docker MCP Toolkit

Security: Code runs in isolated containers, not on your machine, with an audit trail for every execution 

Reproducibility: The same Docker image produces the same results every time, eliminating “works on my machine” issues 

**No Manual Setup**: Zero dependency management or runtime configuration required - you can run a container directly 

**Cross-Platform**: Works identically on macOS and Windows

## Managing MCP Servers

- **View Active Servers**: Check the MCP Toolkit interface in Docker Desktop
- **Add/Remove Servers**: Use the Catalog tab to manage servers
- **Configure Credentials**: Use each server’s Configuration tab
- **Monitor Usage**: View logs and resource usage in Docker Desktop

## Troubleshooting

If the MCP_DOCKER connection doesn’t appear:

1. Ensure Docker Desktop is fully updated (4.48+)
1. Verify MCP Toolkit is enabled in Docker Desktop settings
1. Completely quit and restart both Docker Desktop and Claude Desktop
1. Check the configuration file at: Claude > Settings > Developer > Edit Config
1. Review Docker Desktop logs for any errors

This setup gives Claude powerful capabilities while maintaining security through Docker’s containerization and requiring your approval for all actions.​​​​​​​​​​​​​​​​

<!--
**mrege69/mrege69** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
