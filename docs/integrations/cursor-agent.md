# Cursor

Install [Cursor](https://cursor.sh/) before setup.
The integration key is `cursor-agent`; no separate CLI is required for IDE setup.

## Multi-Install Safety

This integration is declared multi-install safe. See the
[shared multi-install rules](cli.md#can-i-install-multiple-integrations-in-the-same-project).

## Setup

```bash
specify init my-project --integration cursor-agent
```

For an existing GMS Kit project, use `specify integration install cursor-agent`.
See [integration management](cli.md) for activation, upgrades, and removal.

## Installed Skills

Skills are installed as `.cursor/skills/gmskit-<command>/SKILL.md`.
Invoke them in Cursor's chat, for example `/gmskit-specify` or
`/gmskit-bug-assess` for the installed bug extension.

## Options and Workflow Permissions

The optional `--integration-options="--skills"` flag restates the default;
this integration always scaffolds skills. Native events use
`.cursor/hooks.json`; `--events false` disables GMS Kit event handlers.
See [runtime events](cli.md#runtime-events).

Workflow command and prompt steps additionally require the `cursor-agent` CLI.
Dispatch uses `-p --trust --approve-mcps --force`: these flags bypass workspace
trust prompts and approve MCP loading and tool actions. Run workflows only in
a project where you intend to grant those permissions. A configured `--model`
and requested `--output-format json` are forwarded.
