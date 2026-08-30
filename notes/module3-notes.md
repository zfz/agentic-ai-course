# Module 3

## Model Context Protocol (MCP)

**Without MCP** — each app creates its own tools to connect to each service:

Apps: App 1, App 2, App 3
Tools: Slack, GDrive, GitHub, PostgreSQL

Every app wires up its own integration to every tool → **m × n** integrations

**With MCP** — each app uses a shared MCP server for each tool:

Apps: App 1, App 2, App 3 → shared MCP servers → Slack, GDrive, GitHub, PostgreSQL

Each tool is implemented once as an MCP server, each app implements one MCP client → **m + n** integrations
