# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the code

```bash
python main.py
```

## Development environment

This project includes a devcontainer configuration (`.devcontainer/`) built on Ubuntu 24.04 with [`mise`](https://mise.jdx.dev/) installed for managing language/tool versions. `mise` is activated in both bash and zsh inside the container.

The `mise.toml` installs [`chezmoi`](https://www.chezmoi.io/) (latest), a dotfiles manager. After container creation, `scripts/setup` runs automatically to trust the `mise.toml` configuration.

> Note: `scripts/setup` hardcodes the path `/workspaces/test-code/mise.toml`. If the devcontainer workspace folder name differs (e.g. `intro-web-dev`), update that path accordingly.
