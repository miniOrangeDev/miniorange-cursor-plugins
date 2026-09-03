# MCP Server for WordPress

Connect your WordPress site to Cursor via the miniOrange MCP gateway. Cursor
can use the abilities exposed by your WordPress [Abilities API](https://make.wordpress.org/core/)
to perform actions on your WordPress site directly from an AI-assisted workflow.

## What's included

- `mcp.json`: registers the `wordpress` MCP server, pointed at the miniOrange
  gateway (`https://gateway.miniorange.ai/v2/mcp`).

## Privacy & terms

- Privacy policy: <https://plugins.miniorange.com/privacy-policy-for-security-mcp-server>
- Terms of service: <https://www.miniorange.com/terms-and-policies/terms-of-service>

The gateway only processes the WordPress data needed to fulfill the specific
ability/action requested by the agent (e.g., reading or updating a post) and
does not sell or share that data with third parties.

## Requirements

- A WordPress site with the miniOrange Secure MCP Server plugin (or
  equivalent Abilities API bridge) installed and connected to the gateway.

## Authentication

The gateway authenticates using OAuth 2.1 with Dynamic Client Registration
(DCR) — no API key or bearer token needs to be configured in `mcp.json`. On
first connection, Cursor will discover the gateway's OAuth metadata, register
itself as a client automatically, and prompt you to sign in and authorize
access to your WordPress site in the browser.

## Usage

Once authorized, Cursor will connect to the `wordpress` MCP server and expose
the abilities your WordPress site publishes (for example: managing posts,
pages, users, or settings) as tools the agent can call during a chat.
