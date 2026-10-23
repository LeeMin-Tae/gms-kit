# Trae

Install [Trae](https://www.trae.ai/) in your IDE before setup.
The integration key is `trae`; no separate CLI is required.

## Multi-Install Safety

This integration is declared multi-install safe. See the
[shared multi-install rules](cli.md#can-i-install-multiple-integrations-in-the-same-project).

## Setup

```bash
specify init my-project --integration trae
```

For an existing GMS Kit project, use `specify integration install trae`.
See [integration management](cli.md) for activation, upgrades, and removal.

## Installed Skills

Skills are installed automatically as `.trae/skills/gmskit-<command>/SKILL.md`.
Invoke them in the agent's chat, for example `/gmskit-specify` or
`/gmskit-bug-assess` for the installed bug extension.

The optional `--integration-options="--skills"` flag restates the default;
this integration always scaffolds skills, not legacy command files.

## Workflow Limitation

This integration does not support CLI dispatch for workflow command or prompt
steps; its supported path is the IDE skills interface.
