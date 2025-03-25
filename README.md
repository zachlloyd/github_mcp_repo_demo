# GitHub MCP Repository Demo

A Model Context Protocol (MCP) tool for interacting with GitHub repositories. This tool provides functionality to look up repository information and issues using the MCP protocol.

## Features

- Fetch repository metadata using MCP resources (`github://{owner}/{repo}/info`)
- Look up repository issues using MCP tools (`lookup_github_issues`)
- Configurable GitHub API authentication
- Built using the official MCP Python SDK

## Setup

1. Clone the repository:
```bash
git clone https://github.com/zachlloyd/github_mcp_repo_demo.git
cd github_mcp_repo_demo
```

2. Create and activate a virtual environment:
```bash
python3.11 -m venv venv
source venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. (Optional) Set up GitHub authentication:
```bash
export GITHUB_TOKEN=your_github_token
```

## Running the Server

Start the server with:
```bash
python src/server.py
```

By default, the server runs on `http://127.0.0.1:8080`. You can configure the host and port using environment variables:
```bash
export MCP_HOST=0.0.0.0
export MCP_PORT=9000
```

## Usage Examples

### Fetching Repository Information

Using the MCP resource endpoint:
```
github://owner/repo/info
```

### Looking Up Issues

Using the `lookup_github_issues` tool with input:
```json
{
    "repository_url": "https://github.com/owner/repo",
    "state": "open",
    "limit": 10
}
```

## Development

This project uses the Model Context Protocol (MCP) Python SDK. For more information about MCP and its capabilities, visit the [MCP Python SDK repository](https://github.com/modelcontextprotocol/python-sdk).

## License

MIT License

