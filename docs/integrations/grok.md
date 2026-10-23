# Grok Build

Install [Grok Build](https://docs.x.ai/build/overview) before setup.
The integration key is `grok`.

## Multi-Install Safety

This integration is declared multi-install safe. See the
[shared multi-install rules](cli.md#can-i-install-multiple-integrations-in-the-same-project).

## Setup

```bash
specify init my-project --integration grok
```

For an existing GMS Kit project, use `specify integration install grok`.
See [integration management](cli.md) for activation, upgrades, and removal.

## Installed Skills

Skills are installed as `.grok/skills/gmskit-<command>/SKILL.md`.
Invoke them in the agent's chat, for example `/gmskit-specify` or
`/gmskit-bug-assess` for the installed bug extension.

## Workflow Permissions

Workflow steps use `grok -p <prompt> --always-approve`, which automatically
approves tool executions. Run workflows only where that permission is intended.
A configured `--model` and requested `--output-format json` are forwarded.
There are no integration-specific setup options.
