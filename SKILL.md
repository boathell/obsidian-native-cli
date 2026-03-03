---
name: obsidian-native-cli
description: Maintain Obsidian vaults and notes through the native `obsidian` CLI. Use when creating, reading, editing, moving, searching, tagging, task tracking, property management, daily note workflows, templates, link analysis, history recovery, sync/publish operations, workspace or theme or plugin management, vault switching, and developer/debug workflows in Obsidian from terminal commands.
---

# Obsidian Native CLI

## Overview

Use Obsidian native CLI as the default path for terminal-based vault maintenance.
Use quick lookup first, then drill into the official command reference when exact behavior matters.

## Load References

1. Read `references/command-index.md` for a complete quick index of documented commands, parameters, and flags.
2. Read `references/obsidian-cli-official.md` for exact command behavior, examples, and troubleshooting notes.
3. Read `references/commands.json` when a structured command catalog is needed.

## Prepare Environment

1. Confirm Obsidian desktop app is running or let first CLI command launch it.
2. Confirm CLI is enabled in **Settings -> General -> Command line interface**.
3. Confirm target vault and current working directory before mutating files.

## Build Commands Correctly

1. Put `vault=<name-or-id>` before the command when targeting a specific vault.
2. Use `file=<name>` for wikilink-style resolution.
3. Use `path=<path-from-vault-root>` for exact file targeting.
4. Pass parameters as `key=value`, quote values with spaces, and encode multiline content with `\\n`.
5. Pass flags without values, such as `open`, `newtab`, `overwrite`, `total`.
6. Add `--copy` when clipboard output is explicitly useful.

## Execute Maintenance Playbooks

### Daily and capture workflows

Use `daily`, `daily:path`, `daily:read`, `daily:append`, `daily:prepend`, `tasks daily`, `task daily` for journaling and daily task maintenance.

### File lifecycle workflows

Use `create`, `read`, `append`, `prepend`, `open`, `move`, `rename`, `delete`, `files`, `folders`, `file`, `folder` for note creation and refactoring.

### Knowledge hygiene workflows

Use `search`, `search:context`, `links`, `backlinks`, `unresolved`, `orphans`, `deadends`, `outline`, `tags`, `tag`, `aliases`, `properties`, `property:set`, `property:remove`, `property:read` for structure, metadata, and link quality.

### Recovery and sync workflows

Use `diff`, `history`, `history:read`, `history:restore`, `sync:history`, `sync:read`, `sync:restore`, `publish:*` commands to inspect and recover versions or manage publication state.

### Workspace and customization workflows

Use `vaults`, `vault:open`, `workspace`, `workspaces`, `workspace:*`, `tabs`, `tab:open`, `themes`, `theme:*`, `snippets`, `snippet:*`, `plugins`, `plugin:*` for environment management.

### Developer and automation workflows

Use `commands`, `command`, `hotkeys`, `hotkey`, `devtools`, `dev:*`, `eval` to inspect runtime state and automate debugging tasks.

## Apply Safety Rules

1. Inspect target first with read/list commands before destructive operations.
2. Treat `delete permanent`, `history:restore`, `sync:restore`, `publish:remove`, `plugin:uninstall`, `theme:uninstall`, and `workspace:delete` as high-risk commands.
3. Show impacted file paths and versions before executing batch or irreversible changes.
4. Verify result with follow-up commands such as `read`, `history`, `sync:status`, `publish:status`, or `search`.
