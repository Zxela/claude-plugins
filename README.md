# claude-plugins

A collection of Claude Code plugins by [zxela](https://github.com/Zxela).

## Plugins

### [homerun](https://github.com/Zxela/claude-create)

Orchestrated development workflow from idea to implementation with native subagents and Agent Teams. See the [homerun repo](https://github.com/Zxela/claude-create) for full documentation.

## Structure

Plugins live as git submodules under `plugins/`. The `.claude-plugin/marketplace.json` file defines plugin metadata and versions for the marketplace.

## Installation

Add the marketplace in Claude Code:

```
/plugin marketplace add Zxela/claude-plugins
```

Then install individual plugins:

```
/plugin install homerun@zxela-claude-plugins
```

## Development Setup

```sh
git clone --recurse-submodules git@github.com:Zxela/claude-plugins.git
```

If already cloned without submodules:

```sh
git submodule update --init --recursive
```
