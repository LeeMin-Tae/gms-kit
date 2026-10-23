# Devin for Terminal

Install [Devin for Terminal](https://cli.devin.ai/docs) before setup.
The integration key is `devin`.

## Multi-Install Safety

This integration is not declared multi-install safe. See the
[shared multi-install rules](cli.md#can-i-install-multiple-integrations-in-the-same-project).

## Setup

```bash
specify init my-project --integration devin
```

For an existing GMS Kit project, use `specify integration install devin`.
See [integration management](cli.md) for activation, upgrades, and removal.

## Installed Skills

Skills are installed as `.devin/skills/gmskit-<command>/SKILL.md`.
Invoke them in the agent's chat, for example `/gmskit-specify` or
`/gmskit-bug-assess` for the installed bug extension.

## Options and Workflow Dispatch

The optional `--integration-options="--skills"` flag restates the default;
this integration always scaffolds skills. Native events use
`.devin/hooks.v1.json`; `--events false` disables GMS Kit event handlers.
See [runtime events](cli.md#runtime-events).

Workflow steps use `devin -p <prompt>` and forward a configured `--model`.
Devin's adapter returns plain-text stdout even when structured output is
requested; it does not add a JSON-output flag.
