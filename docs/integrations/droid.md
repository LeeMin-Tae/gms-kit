# Factory Droid

Install [Factory Droid](https://docs.factory.ai/cli/getting-started/overview) before setup.
The integration key is `droid`.

## Multi-Install Safety

This integration is declared multi-install safe. See the
[shared multi-install rules](cli.md#can-i-install-multiple-integrations-in-the-same-project).

## Setup

```bash
specify init my-project --integration droid
```

For an existing GMS Kit project, use `specify integration install droid`.
See [integration management](cli.md) for activation, upgrades, and removal.

## Installed Skills

Skills are installed as `.factory/skills/gmskit-<command>/SKILL.md`.
Invoke them in the agent's chat, for example `/gmskit-specify` or
`/gmskit-bug-assess` for the installed bug extension.

Generated skills are both user- and model-invocable.

## Workflow Dispatch

Workflow steps use `droid exec <prompt>`, forwarding `--model` and requesting
`--output-format json` when appropriate. GMS Kit does not add a
permission-bypass flag. Operators can explicitly configure permission flags
through `GMSKIT_INTEGRATION_DROID_EXTRA_ARGS`; those arguments follow Spec
Kit's model/output flags and may override them under duplicate-flag parsing.
There are no integration-specific setup options.
