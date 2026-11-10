# MCP Server for Joomla

Connect your Joomla site to Cursor via the miniOrange MCP gateway. Cursor exposes the MCP tools your site administrator has enabled in the JOOMAI MCP dashboard (articles, menus, modules, media, extensions, system checks, and more).

## What's included

- `**mcp.json**` — Registers the Joomla MCP server, pointed at the miniOrange gateway (`https://joomla.mcp.miniorange.ai/mcp`).

## Privacy & terms

- [Privacy policy](https://plugins.miniorange.com/joomla/secure-mcp-server-privacy-policy)
- [Terms of service](https://www.miniorange.com/terms-and-policies/terms-of-service)

The gateway only processes the Joomla data needed to fulfill the specific action requested by the agent (for example, reading or updating a articles) and does not delete or update bulk data.

## Requirements

- A Joomla site with the miniOrange Secure MCP Server plugin installed and connected to the gateway.

## Authentication

The gateway authenticates using **OAuth 2.1** with **Dynamic Client Registration (DCR)** - no API key or bearer token needs to be configured in `mcp.json`. On first connection, Cursor will discover the gateway's OAuth metadata, register itself as a client automatically, and prompt you to sign in and authorize access to your joomla site in the browser.

## Usage

Once authorized, Cursor will connect to the Joomla MCP server and enabled tools can include articles, menus, modules, plugins, languages, tags, banners, read-only or administrative checks. Each call runs as the signed-in Joomla user and respects Joomla ACL.