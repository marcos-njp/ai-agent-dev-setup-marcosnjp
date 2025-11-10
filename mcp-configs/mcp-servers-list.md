# 🔌 MCP Servers Configuration List

This document provides detailed information about all 4 MCP (Multi-Channel Protocol) servers configured for the AI Agent Development Bootcamp.

---

## 1. Rolldice Server

**Server Name:** `rolldice`

**Connection Type:** Remote MCP Server

**Endpoint:** `https://rolldice.ausbizconsulting.com.au/api/mcp`

**Command Configuration:**
```json
{
  "command": "npx",
  "args": ["-y", "mcp-remote", "https://rolldice.ausbizconsulting.com.au/api/mcp"]
}
```

**Purpose and Functionality:**
The Rolldice service provides a simple, deterministic API for generating random numbers or simulating dice rolls. AI agents use it for:
- Testing stochastic behaviors in agent workflows
- Demonstrations and examples
- Reproducible randomness in experiments
- Simulating choices or sampling during agent operations

**Use Cases:**
- Random number generation for testing
- Dice roll simulations
- Probability demonstrations
- Decision-making simulations

---

## 2. Bootcamp RAG (AI Agent)

**Server Name:** `bootcamp-rag`

**Connection Type:** Remote MCP Server

**Endpoint:** `https://ai-assist.ausbizconsulting.com.au/api/mcp`

**Command Configuration:**
```json
{
  "command": "npx",
  "args": ["-y", "mcp-remote", "https://ai-assist.ausbizconsulting.com.au/api/mcp"]
}
```

**Purpose and Functionality:**
The Bootcamp RAG (Retrieval-Augmented Generation) server acts as a hands-on example backend that exposes agent capabilities used in the workshop. It provides:
- RAG-based knowledge retrieval
- Workshop-specific documentation access
- Task handlers and orchestration endpoints
- Real-world service API examples

**Use Cases:**
- Testing agent integrations
- Practicing agent action requests
- Validating end-to-end agent workflows
- Accessing bootcamp documentation and resources

---

## 3. Tech Bootcamp Consultations

**Server Name:** `tech-bootcamp-consultations`

**Connection Type:** Remote MCP Server

**Endpoint:** `https://ai-assist.ausbizconsulting.com.au/api/mcp`

**Command Configuration:**
```json
{
  "command": "npx",
  "args": ["-y", "mcp-remote", "https://ai-assist.ausbizconsulting.com.au/api/mcp"]
}
```

**Purpose and Functionality:**
This server provides consultation and scheduling capabilities for the tech bootcamp program. It enables:
- Booking consultation sessions
- Managing appointments
- Accessing mentor availability
- Scheduling technical support sessions

**Use Cases:**
- Schedule one-on-one consultations
- Book technical support sessions
- Manage bootcamp appointments
- Access mentor calendars

---

## 4. GitHub

**Server Name:** `github`

**Connection Type:** NPM Package MCP Server

**Package:** `@modelcontextprotocol/server-github`

**Command Configuration:**
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-github"],
  "env": {
    "GITHUB_PERSONAL_ACCESS_TOKEN": "<your-token-here>"
  }
}
```

**Purpose and Functionality:**
The GitHub MCP server enables direct interaction with GitHub repositories through the Model Context Protocol. It provides:
- Repository management and navigation
- File operations (read, write, update, delete)
- Issue tracking and management
- Pull request creation and review
- Commit history access and analysis
- Branch management operations

**Use Cases:**
- Automated repository operations
- Code review and analysis
- Issue and PR management
- Version control integration
- Collaborative development workflows
- Repository documentation updates

**Authentication:**
Requires a GitHub Personal Access Token with appropriate permissions for repository access.

---

## 📊 Server Summary

| Server Name | Type | Status | Primary Use |
|------------|------|--------|-------------|
| rolldice | Remote | ✅ Active | Random number generation |
| bootcamp-rag | Remote | ✅ Active | Knowledge retrieval & documentation |
| tech-bootcamp-consultations | Remote | ✅ Active | Scheduling & consultations |
| github | NPM Package | ✅ Active | Repository & version control |

---

## 🔧 Configuration Notes

- Remote servers (rolldice, bootcamp-rag, tech-bootcamp-consultations) use `npx -y mcp-remote` for connection
- GitHub server uses `npx -y @modelcontextprotocol/server-github` with authentication
- All servers are configured in `claude-desktop-config.json`
- Servers are automatically connected when Claude Desktop starts
- GitHub server requires GITHUB_PERSONAL_ACCESS_TOKEN environment variable

---

**Last Updated:** November 10, 2025
