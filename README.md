# miniOrange Cursor plugins

Cursor Marketplace plugins published by miniOrange, scaffolded from
[cursor/plugin-template](https://github.com/cursor/plugin-template).

## Plugins

- **[mcp-server-for-wordpress](plugins/mcp-server-for-wordpress)**: connects
  Cursor to a WordPress site through the miniOrange MCP gateway
  (`https://gateway.miniorange.ai/v2/mcp`), exposing WordPress Abilities API
  actions as tools.

## Repo layout

- `.cursor-plugin/marketplace.json`: marketplace metadata and the list of
  published plugins.
- `plugins/*/.cursor-plugin/plugin.json`: per-plugin manifest (`name`,
  `displayName`, `author`, `description`, `keywords`, `license`, `version`).
- `docs/add-a-plugin.md`: steps for adding another plugin to this repo.
- `scripts/validate-template.mjs`: validates manifests before submission.

## Publisher terms compliance

This repo is scaffolded to align with the
[Cursor Marketplace Publisher Terms](https://cursor.com/marketplace-publisher-terms):

- `LICENSE` and each `plugin.json`'s `license` field use MIT (a permissive
  license, per §3.3 — GPL/AGPL/LGPL are not permitted).
- Docs refer to the product as "Cursor" only (§4.6 brand guidelines).
- Each plugin's README links its privacy policy and terms of service so
  they're visible to Marketplace users (§4.2).
- Plugins are free to install and use through the Marketplace, with no fees
  charged to users, directly or indirectly (§3.1).

Before submitting, you still need to apply at
[cursor.com/marketplace/publish](https://cursor.com/marketplace/publish) —
Anysphere reviews the application and the plugin's code before approval.

## Validate before submitting

```bash
node scripts/validate-template.mjs
```

## Submission checklist

- Each plugin has a valid `.cursor-plugin/plugin.json`.
- Plugin names are unique, lowercase, and kebab-case.
- `.cursor-plugin/marketplace.json` entries map to real plugin folders.
- All frontmatter metadata is present in rule, skill, agent, and command files.
- Logos are committed and referenced with relative paths.
- `node scripts/validate-template.mjs` passes.
- Repository link is ready for submission to the Cursor team.
