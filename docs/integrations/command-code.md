# Command Code

Install [Command Code](https://commandcode.ai/docs) before setup.
The integration key is `command-code`.

## Multi-Install Safety

This integration is declared multi-install safe. See the
[shared multi-install rules](cli.md#can-i-install-multiple-integrations-in-the-same-project).

## Setup

```bash
specify init my-project --integration command-code
```

For an existing GMS Kit project, use `specify integration install command-code`.
See [integration management](cli.md) for activation, upgrades, and removal.

## Installed Skills

Skills are installed as `.commandcode/skills/gmskit-<command>/SKILL.md`.
Invoke them in the agent's chat with a dollar prefix, for example
`$gmskit-specify` or `$gmskit-bug-assess` for the installed bug extension.

## Options and Workflow Dispatch

The optional `--integration-options="--skills"` flag restates the default;
this integration always scaffolds skills.

Workflow steps use `command-code -p <prompt>`, with `--model` when configured
and `--output-format json` when structured output is requested.
