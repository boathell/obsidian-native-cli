# Obsidian CLI Command Index

Source: [https://help.obsidian.md/cli](https://help.obsidian.md/cli)
Snapshot date: 2026-03-03

This index is generated from the official CLI documentation and aims to include all documented commands, parameters, and flags.

Global argument patterns (apply across many commands):
- `vault=<name|id>` (must be placed before command)
- `file=<name>` (wikilink-style resolution)
- `path=<path>` (exact vault-relative path)
- `--copy` (copy command output to clipboard)

Total commands: 115

| Section | Command | Parameters | Flags |
| --- | --- | --- | --- |
| General commands | `help` | `<command>` | - |
| General commands | `version` | - | - |
| General commands | `reload` | - | - |
| General commands | `restart` | - | - |
| Bases | `bases` | - | - |
| Bases | `base:views` | - | - |
| Bases | `base:create` | `file=<name>`, `path=<path>`, `view=<name>`, `name=<name>`, `content=<text>` | `open`, `newtab` |
| Bases | `base:query` | `file=<name>`, `path=<path>`, `view=<name>`, `format=json|csv|tsv|md|paths` | - |
| Bookmarks | `bookmarks` | `format=json|tsv|csv` | `total`, `verbose` |
| Bookmarks | `bookmark` | `file=<path>`, `subpath=<subpath>`, `folder=<path>`, `search=<query>`, `url=<url>`, `title=<title>` | - |
| Command palette | `commands` | `filter=<prefix>` | - |
| Command palette | `command` | `id=<command-id>` | - |
| Command palette | `hotkeys` | `format=json|tsv|csv` | `total`, `verbose` |
| Command palette | `hotkey` | `id=<command-id>` | `verbose` |
| Daily notes | `daily` | `paneType=tab|split|window` | - |
| Daily notes | `daily:path` | - | - |
| Daily notes | `daily:read` | - | - |
| Daily notes | `daily:append` | `content=<text>`, `paneType=tab|split|window` | `inline`, `open` |
| Daily notes | `daily:prepend` | `content=<text>`, `paneType=tab|split|window` | `inline`, `open` |
| File history | `diff` | `file=<name>`, `path=<path>`, `from=<n>`, `to=<n>`, `filter=local|sync` | - |
| File history | `history` | `file=<name>`, `path=<path>` | - |
| File history | `history:list` | - | - |
| File history | `history:read` | `file=<name>`, `path=<path>`, `version=<n>` | - |
| File history | `history:restore` | `file=<name>`, `path=<path>`, `version=<n>` | - |
| File history | `history:open` | `file=<name>`, `path=<path>` | - |
| Files and folders | `file` | `file=<name>`, `path=<path>` | - |
| Files and folders | `files` | `folder=<path>`, `ext=<extension>` | `total` |
| Files and folders | `folder` | `path=<path>`, `info=files|folders|size` | - |
| Files and folders | `folders` | `folder=<path>` | `total` |
| Files and folders | `open` | `file=<name>`, `path=<path>` | `newtab` |
| Files and folders | `create` | `name=<name>`, `path=<path>`, `content=<text>`, `template=<name>` | `overwrite`, `open`, `newtab` |
| Files and folders | `read` | `file=<name>`, `path=<path>` | - |
| Files and folders | `append` | `file=<name>`, `path=<path>`, `content=<text>` | `inline` |
| Files and folders | `prepend` | `file=<name>`, `path=<path>`, `content=<text>` | `inline` |
| Files and folders | `move` | `file=<name>`, `path=<path>`, `to=<path>` | - |
| Files and folders | `rename` | `file=<name>`, `path=<path>`, `name=<name>` | - |
| Files and folders | `delete` | `file=<name>`, `path=<path>` | `permanent` |
| Links | `backlinks` | `file=<name>`, `path=<path>`, `format=json|tsv|csv` | `counts`, `total` |
| Links | `links` | `file=<name>`, `path=<path>` | `total` |
| Links | `unresolved` | `format=json|tsv|csv` | `total`, `counts`, `verbose` |
| Links | `orphans` | - | `total` |
| Links | `deadends` | - | `total` |
| Outline | `outline` | `file=<name>`, `path=<path>`, `format=tree|md|json` | `total` |
| Plugins | `plugins` | `filter=core|community`, `format=json|tsv|csv` | `versions` |
| Plugins | `plugins:enabled` | `filter=core|community`, `format=json|tsv|csv` | `versions` |
| Plugins | `plugins:restrict` | - | `on`, `off` |
| Plugins | `plugin` | `id=<plugin-id>` | - |
| Plugins | `plugin:enable` | `id=<id>`, `filter=core|community` | - |
| Plugins | `plugin:disable` | `id=<id>`, `filter=core|community` | - |
| Plugins | `plugin:install` | `id=<id>` | `enable` |
| Plugins | `plugin:uninstall` | `id=<id>` | - |
| Plugins | `plugin:reload` | `id=<id>` | - |
| Properties | `aliases` | `file=<name>`, `path=<path>` | `total`, `verbose`, `active` |
| Properties | `properties` | `file=<name>`, `path=<path>`, `name=<name>`, `sort=count`, `format=yaml|json|tsv` | `total`, `counts`, `active` |
| Properties | `property:set` | `name=<name>`, `value=<value>`, `type=text|list|number|checkbox|date|datetime`, `file=<name>`, `path=<path>` | - |
| Properties | `property:remove` | `name=<name>`, `file=<name>`, `path=<path>` | - |
| Properties | `property:read` | `name=<name>`, `file=<name>`, `path=<path>` | - |
| Publish | `publish:site` | - | - |
| Publish | `publish:list` | - | `total` |
| Publish | `publish:status` | - | `total`, `new`, `changed`, `deleted` |
| Publish | `publish:add` | `file=<name>`, `path=<path>` | `changed` |
| Publish | `publish:remove` | `file=<name>`, `path=<path>` | - |
| Publish | `publish:open` | `file=<name>`, `path=<path>` | - |
| Random notes | `random` | `folder=<path>` | `newtab` |
| Random notes | `random:read` | `folder=<path>` | - |
| Search | `search` | `query=<text>`, `path=<folder>`, `limit=<n>`, `format=text|json` | `total`, `case` |
| Search | `search:context` | `query=<text>`, `path=<folder>`, `limit=<n>`, `format=text|json` | `case` |
| Search | `search:open` | `query=<text>` | - |
| Sync | `sync` | - | `on`, `off` |
| Sync | `sync:status` | - | - |
| Sync | `sync:history` | `file=<name>`, `path=<path>` | `total` |
| Sync | `sync:read` | `file=<name>`, `path=<path>`, `version=<n>` | - |
| Sync | `sync:restore` | `file=<name>`, `path=<path>`, `version=<n>` | - |
| Sync | `sync:open` | `file=<name>`, `path=<path>` | - |
| Sync | `sync:deleted` | - | `total` |
| Tags | `tags` | `file=<name>`, `path=<path>`, `sort=count`, `format=json|tsv|csv` | `total`, `counts`, `active` |
| Tags | `tag` | `name=<tag>` | `total`, `verbose` |
| Tasks | `tasks` | `file=<name>`, `path=<path>`, `status="<char>"`, `format=json|tsv|csv` | `total`, `done`, `todo`, `verbose`, `active`, `daily` |
| Tasks | `task` | `ref=<path:line>`, `file=<name>`, `path=<path>`, `line=<n>`, `status="<char>"` | `toggle`, `daily`, `done`, `todo` |
| Templates | `templates` | - | `total` |
| Templates | `template:read` | `name=<template>`, `title=<title>` | `resolve` |
| Templates | `template:insert` | `name=<template>` | - |
| Themes and snippets | `themes` | - | `versions` |
| Themes and snippets | `theme` | `name=<name>` | - |
| Themes and snippets | `theme:set` | `name=<name>` | - |
| Themes and snippets | `theme:install` | `name=<name>` | `enable` |
| Themes and snippets | `theme:uninstall` | `name=<name>` | - |
| Themes and snippets | `snippets` | - | - |
| Themes and snippets | `snippets:enabled` | - | - |
| Themes and snippets | `snippet:enable` | `name=<name>` | - |
| Themes and snippets | `snippet:disable` | `name=<name>` | - |
| Unique notes | `unique` | `name=<text>`, `content=<text>`, `paneType=tab|split|window` | `open` |
| Vault | `vault` | `info=name|path|files|folders|size` | - |
| Vault | `vaults` | - | `total`, `verbose` |
| Vault | `vault:open` | `name=<name>` | - |
| Web viewer | `web` | `url=<url>` | `newtab` |
| Wordcount | `wordcount` | `file=<name>`, `path=<path>` | `words`, `characters` |
| Workspace | `workspace` | - | `ids` |
| Workspace | `workspaces` | - | `total` |
| Workspace | `workspace:save` | `name=<name>` | - |
| Workspace | `workspace:load` | `name=<name>` | - |
| Workspace | `workspace:delete` | `name=<name>` | - |
| Workspace | `tabs` | - | `ids` |
| Workspace | `tab:open` | `group=<id>`, `file=<path>`, `view=<type>` | - |
| Workspace | `recents` | - | `total` |
| Developer commands | `devtools` | - | - |
| Developer commands | `dev:debug` | - | `on`, `off` |
| Developer commands | `dev:cdp` | `method=<CDP.method>`, `params=<json>` | - |
| Developer commands | `dev:errors` | - | `clear` |
| Developer commands | `dev:screenshot` | `path=<filename>` | - |
| Developer commands | `dev:console` | `limit=<n>`, `level=log|warn|error|info|debug` | `clear` |
| Developer commands | `dev:css` | `selector=<css>`, `prop=<name>` | - |
| Developer commands | `dev:dom` | `selector=<css>`, `attr=<name>`, `css=<prop>` | `total`, `text`, `inner`, `all` |
| Developer commands | `dev:mobile` | - | `on`, `off` |
| Developer commands | `eval` | `code=<javascript>` | - |
