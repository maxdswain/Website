---
title: "Code Executor MCP"
description: "A Go MCP server for session-scoped Python execution in isolated Docker containers."
summary: "Give agents a Python execution tool with session-scoped packages, bounded Docker containers and automatic cleanup."
weight: 30
featureimage: "project-logos/terminal.svg"
showBreadcrumbs: true
---

{{< lead >}}
A Python execution tool for agents, with each MCP session assigned its own isolated Docker container.
{{< /lead >}}

{{< keywordList >}}
{{< keyword icon="skill-go" >}}Go{{< /keyword >}}
{{< keyword icon="skill-modelcontextprotocol" >}}MCP{{< /keyword >}}
{{< keyword icon="skill-python" >}}Python{{< /keyword >}}
{{< keyword icon="docker" >}}Docker{{< /keyword >}}
{{< /keywordList >}}

I built **Code Executor MCP** as a Go server using MCP's Streamable HTTP transport. Its `execute_python` tool accepts Python code and optional package requirements, then returns the program's standard output.

{{< button href="https://github.com/maxdswain/code-executor-mcp" >}}GitHub repository{{< /button >}}

## Session lifecycle

{{< mermaid >}}
sequenceDiagram
    accTitle: A Python execution session
    accDescr: The MCP server assigns a dedicated container, returns the Python program's output and destroys the container when the session ends.
    participant C as MCP client
    participant S as Go server
    participant D as Container
    C->>S: Open session
    S->>D: Reserve from pool
    C->>S: execute_python
    S->>D: Run Python offline
    D-->>S: Standard output
    S-->>C: Tool result
    C->>S: End session
    S->>D: Destroy container
{{< /mermaid >}}

The client can call `execute_python` repeatedly in the same session. If a call requests packages, the server installs them with uv before disconnecting the network and running the code. Calls are serialised, and installed packages stay in that session’s container until it is destroyed.

## Explore further

- [Configuration and deployment guidance](https://github.com/maxdswain/code-executor-mcp#readme)
- [Pool lifecycle and concurrency tests](https://github.com/maxdswain/code-executor-mcp/tree/main/tests/docker)
