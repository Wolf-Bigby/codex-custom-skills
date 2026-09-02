# Codex Custom Skills

This repository contains two reusable Codex skills:

- `remote-sensing-env-writing-v2`: White Group-style writing, revision, diagnosis, and reviewer-response workflows for remote-sensing and environmental-science manuscripts.
- `zz-scientific-plotting`: evidence-safe, publication-ready scientific plotting and figure-review workflows.

## Install on macOS

Clone this repository, then copy or link each skill directory into the Codex skill directory:

```bash
mkdir -p ~/.codex/skills
ln -sfn "$PWD/remote-sensing-env-writing-v2" ~/.codex/skills/remote-sensing-env-writing-v2
ln -sfn "$PWD/zz-scientific-plotting" ~/.codex/skills/zz-scientific-plotting
```

If another agent discovers skills from `~/.agents/skills`, create matching links there as well:

```bash
mkdir -p ~/.agents/skills
ln -sfn "$PWD/remote-sensing-env-writing-v2" ~/.agents/skills/remote-sensing-env-writing-v2
ln -sfn "$PWD/zz-scientific-plotting" ~/.agents/skills/zz-scientific-plotting
```

Restart the Codex session after installation so the skill catalog is refreshed.

## Update

Run `git pull` in the cloned repository. Symlink-based installations immediately use the updated files after the next Codex session starts.

## Repository visibility

Keep the repository private unless you intentionally want to publish these workflows. No software license is included by default.
