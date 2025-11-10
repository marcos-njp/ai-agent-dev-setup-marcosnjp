# 🚀 AI Agent Developer Environment Setup Verification

**Repository Name:** ai-agent-dev-setup-marcosnjp

---

## 👤 Workshop Details

- **Name:** Nino Justin Marcos
- **Cohort:** AI Agent Development Bootcamp - Week 1

---

## ⚙️ Development Environment Checklist

The following checklist verifies the installation and functionality of the required tools.

### 1. Node.js Installation

✅ **Status:** Verified and installed

- **Command:** `node --version`
- **Version:** v24.9.0
- **Verification:** Core runtime environment confirmed operational

![Node.js Version](./screenshots/Screenshot%202025-11-10%20235330.png)

```bash
node --version
v24.9.0
```

### 2. Git Installation

✅ **Status:** Verified and installed

- **Command:** `git --version`
- **Version:** git version 2.51.0.windows.1
- **Verification:** Version control system confirmed operational

![Git Version](./screenshots/Screenshot%202025-11-10%20235330.png)

```bash
git --version
git version 2.51.0.windows.1
```

### 3. VS Code Insider & GitHub Copilot

✅ **Status:** Verified and operational

- **IDE:** VS Code Insider running with GitHub Copilot enabled
- **GitHub Account:** marcos-njp (GitHub)
- **Verification:** Development environment and integrated AI assistance confirmed functional

![VS Code Insider with GitHub Copilot](./screenshots/Screenshot%202025-11-11%20060948.png)
![VS Code Account](./screenshots/Screenshot%202025-11-11%20061016.png)

---

### 4. Claude Desktop & MCP Connections

✅ **Status:** Verified and operational

- **AI Interface:** Claude Desktop running with all 5 MCP servers connected
- **Connected Servers:**
  - ✅ bootcamp-rag
  - ✅ tech-bootcamp-consultations
  - ✅ rolldice
  - ✅ person-crud
  - ✅ github

![MCP Servers Overview](./screenshots/Screenshot%202025-11-10%20232129.png)

**Verification:** All MCP servers confirmed connected and responsive

---

## 💻 Multi-Channel Protocol (MCP) Server Explanations

### 1. Rolldice

**Purpose and Functionality:**

The Rolldice service provides a simple, deterministic API for generating random numbers or simulating dice rolls. Agents use it for testing stochastic behaviors, demos, and reproducible randomness in workflows (for example, simulating choices or sampling during experiments).

**Screenshot Evidence:**

![Rolldice MCP Server](./screenshots/Screenshot%202025-11-10%20233100.png)
![Rolldice in Action](./screenshots/Screenshot%202025-11-10%20233126.png)

**Configuration:**
- Command: `npx`
- Arguments: `-y mcp-remote https://rolldice.ausbizconsulting.com.au/api/mcp`

---

### 2. Bootcamp RAG (AI Agent)

**Purpose and Functionality:**

The Bootcamp RAG (Retrieval-Augmented Generation) server acts as a hands-on example backend that exposes agent capabilities used in the workshop. It provides knowledge retrieval, workshop documentation access, and task handlers so participants can test integrations, practice requesting agent actions, and validate end-to-end agent workflows.

**Screenshot Evidence:**

![Bootcamp RAG MCP Server](./screenshots/Screenshot%202025-11-10%20232810.png)
![Bootcamp RAG Query](./screenshots/Screenshot%202025-11-10%20232744.png)

**Configuration:**
- Command: `npx`
- Arguments: `-y mcp-remote https://ai-assist.ausbizconsulting.com.au/api/mcp`

**Example Usage:**
- Querying office locations
- Searching bootcamp content
- Accessing student testimonials

---

### 3. Tech Bootcamp Consultations

**Purpose and Functionality:**

This server provides consultation and scheduling capabilities for the tech bootcamp program. It enables booking consultation sessions, managing appointments, accessing mentor availability, and scheduling technical support sessions. This demonstrates how agents can interact with calendar and scheduling systems.

**Screenshot Evidence:**

![Tech Bootcamp Consultations MCP Server](./screenshots/Screenshot%202025-11-10%20232822.png)
![Tech Bootcamp Consultations Running](./screenshots/Screenshot%202025-11-10%20233047.png)
![Tech Bootcamp Query](./screenshots/Screenshot%202025-11-10%20233031.png)

**Configuration:**
- Command: `npx`
- Arguments: `-y mcp-remote https://ai-assist.ausbizconsulting.com.au/api/mcp`

---

### 4. GitHub

**Purpose and Functionality:**

The GitHub MCP server enables direct interaction with GitHub repositories through the Model Context Protocol. It provides capabilities for repository management, file operations, issue tracking, pull request management, and commit history access. This server demonstrates how AI agents can integrate with version control systems to automate development workflows, manage code repositories, and interact with collaborative development platforms.

**Screenshot Evidence:**

![GitHub MCP Server](./screenshots/Screenshot%202025-11-10%20232129.png)
![GitHub Profile Lookup](./screenshots/Screenshot%202025-11-10%20232235.png)
![GitHub Repositories](./screenshots/Screenshot%202025-11-10%20232324.png)
![GitHub Repository Details](./screenshots/Screenshot%202025-11-10%20232341.png)

**Configuration:**
- Command: `npx`
- Arguments: `-y @modelcontextprotocol/server-github`

**Example Usage:**
- Profile lookup (Username: marcos-njp)
- Repository listing and management
- Accessing repository information

---

### 5. Person CRUD (Database Operations)

**Purpose and Functionality:**

The Person CRUD MCP server demonstrates basic database operations (Create, Read, Update, Delete) for managing user records. It provides a practical example of how AI agents can interact with databases to perform standard CRUD operations, making it an excellent learning tool for understanding data persistence and management in AI agent workflows.

**Screenshot Evidence:**

![Person CRUD - List Users](./screenshots/Screenshot%202025-11-10%20225038.png)
![Person CRUD - Create User](./screenshots/Screenshot%202025-11-10%20225156.png)
![Person CRUD - User Created](./screenshots/Screenshot%202025-11-10%20225227.png)
![Person CRUD - Update User](./screenshots/Screenshot%202025-11-10%20225325.png)
![Person CRUD - User Updated](./screenshots/Screenshot%202025-11-10%20225353.png)
![Person CRUD - Delete User](./screenshots/Screenshot%202025-11-10%20225427.png)
![Person CRUD - User Deleted](./screenshots/Screenshot%202025-11-10%20225445.png)

**Operations Demonstrated:**
- **List:** Retrieved all 11 people in the database
- **Create:** Created new user "Grape Juice" with email and phone
- **Update:** Modified email from grapejuice@gmail.com to juicegrape@gmail.com
- **Delete:** Removed user from database

---

## 📝 Troubleshooting Notes

### Issues Encountered

**Status:** Only encountered an error with the Github token. It was fixed easily.

### Setup Process

All 4 MCP servers connected successfully. Configuration was straightforward with proper JSON formatting in `claude_desktop_config.json`.

### Key Success Factors

- ✅ Ensured Node.js was properly installed before configuring MCP servers
- ✅ Validated JSON syntax in configuration file
- ✅ Restarted Claude Desktop after configuration changes
- ✅ Verified network connectivity for remote servers
- ✅ Properly configured GitHub Personal Access Token for GitHub MCP server
- ✅ Used correct MCP remote URLs for bootcamp services

### Configuration File Location

Windows: `%APPDATA%\Claude\claude_desktop_config.json`

### Tips for Success

1. **JSON Validation:** Always validate your JSON configuration before restarting Claude Desktop
2. **Server Order:** The order of servers in the configuration doesn't matter
3. **Remote Servers:** Ensure stable internet connection for remote MCP servers
4. **GitHub Token:** Store your GitHub Personal Access Token securely
5. **Restart Required:** Always restart Claude Desktop after modifying the configuration

---

## 📂 Repository Structure

```
ai-agents-wk1/
├── screenshots/          # All verification screenshots
├── mcp-configs/         # MCP server configuration files
├── README.md            # This file
└── VERIFICATION.md      # Detailed verification proof
```

---

## 🔗 Useful Links

- [GitHub Repository](https://github.com/marcos-njp/ai-agent-dev-setup-marcosnjp)
- [Model Context Protocol Documentation](https://modelcontextprotocol.io/)
- [Claude Desktop](https://claude.ai/download)
- [VS Code Insider](https://code.visualstudio.com/insiders/)

---

## 📄 License

This repository is part of the AI Agent Development Bootcamp - Week 1 deliverable.

---

**Last Updated:** October 18, 2025
