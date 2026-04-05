 MCP Servers — Complete Documentation

This document describes all 4 MCP servers configured for this AI Agent Developer environment.

---

Server 1: Rolldice

| Property | Value |
|---|---|
| Name | `rolldice` |
| Package | `mcp-dice` |
| Launch method | `uvx mcp-dice` |
| Authentication | None required |
| Status | ✅ Connected |

Purpose
Rolldice is a lightweight MCP server for rolling dice in standard tabletop RPG notation. It serves as the "Hello World" of MCP server setup — its simplicity makes it ideal for verifying that your MCP infrastructure, Node.js path, and Claude Desktop configuration are all working before moving to more complex servers.

Available Tools
| Tool | Description | Example Input |
|---|---|---|
| `roll_dice` | Rolls dice using standard notation | `"2d6+3"`, `"1d20"`, `"4d8"` |

---

Server 2: Bootcamp AI Agent

| Property | Value |
|---|---|
| Name | `bootcamp` |
| Launch method | `node C:\Users\KURT\bootcamp-server\index.js` |
| Authentication | None required |
| Status | ✅ Connected |

Purpose
The Bootcamp AI Agent server exposes practical utility tools demonstrating how business logic can be wrapped in MCP and made available to Claude as executable capabilities.

Available Tools
| Tool | Description |
|---|---|
| `todo_add` | Add a new task |
| `todo_list` | List all current tasks |
| `todo_complete` | Mark a task done by ID |
| `todo_delete` | Delete a task by ID |
| `calculate` | Perform arithmetic |
| `greet` | Greet a user by name |
| `tell_joke` | Return a random programming joke |
| `random_number` | Generate a number in a range |

---

Server 3: Google Calendar

| Property | Value |
|---|---|
| Name | `google-calendar` |
| Package | `@anthropic-ai/mcp-server-google-calendar` |
| Launch method | `npx -y @anthropic-ai/mcp-server-google-calendar` |
| Authentication | Google OAuth 2.0 |
| Status | ✅ Connected |

Purpose
Gives Claude direct read/write access to Google Calendar, transforming it from an advisor into an executor that can actually book meetings and manage schedules.

Available Tools
| Tool | Description |
|---|---|
| `gcal_list_events` | List events in a time range |
| `gcal_create_event` | Create a new calendar event |
| `gcal_update_event` | Update an existing event |
| `gcal_delete_event` | Delete an event |
| `gcal_find_meeting_times` | Find mutual free time across attendees |

---

Server 4: GitHub

| Property | Value |
|---|---|
| Name | `github` |
| Package | `@modelcontextprotocol/server-github` |
| Launch method | `npx -y @modelcontextprotocol/server-github` |
| Authentication | GitHub Personal Access Token |
| Status | ✅ Connected |

Purpose
Gives Claude direct access to GitHub repositories, issues, pull requests, and code — enabling full software delivery workflows from within Claude Desktop.

Available Tools
| Tool | Description |
|---|---|
| `create_or_update_file` | Create or update a file in a repo |
| `get_file_contents` | Read a file's contents |
| `push_files` | Push multiple files in one commit |
| `create_issue` | Open a new issue |
| `create_pull_request` | Open a pull request |
| `list_commits` | View commit history |

---

Summary Table

| Server | Auth Required | Key Use Case |
|---|---|---|
| Rolldice | ❌ None | Verify MCP setup |
| Bootcamp AI Agent | ❌ None | Task & utility management |
| Google Calendar | ✅ OAuth 2.0 | Scheduling & booking |
| GitHub | ✅ PAT Token | Code & repo management |