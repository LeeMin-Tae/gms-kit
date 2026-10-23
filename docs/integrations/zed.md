# Zed

Install [Zed](https://zed.dev/) before setup.
The integration key is `zed`; no separate CLI is required.

## Multi-Install Safety

This integration is not declared multi-install safe. See the
[shared multi-install rules](cli.md#can-i-install-multiple-integrations-in-the-same-project).

## Setup

```bash
specify init my-project --integration zed
```

For an existing GMS Kit project, use `specify integration install zed`.
See [integration management](cli.md) for activation, upgrades, and removal.

## Installed Skills

Skills are installed as `.agents/skills/gmskit-<command>/SKILL.md`.
Invoke them in the agent's chat, for example `/gmskit-specify` or
`/gmskit-bug-assess` for the installed bug extension.
This directory is shared with other integrations, so do not assume their
generated skills can coexist without overlap.

## Workflow Limitation

This integration does not support CLI dispatch for workflow command or prompt
steps. It installs editor skills only and has no integration-specific setup
options; a `--skills` flag is not needed or declared.
