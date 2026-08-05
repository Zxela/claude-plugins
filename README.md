# claude-plugins

A collection of Claude Code plugins by [zxela](https://github.com/Zxela).

## Plugins

### [homerun](https://github.com/Zxela/claude-create)

Orchestrated development workflow from idea to implementation with native subagents and Agent Teams. See the [homerun repo](https://github.com/Zxela/claude-create) for full documentation.

### [auto-optimize](https://github.com/Zxela/auto-optimize)

Point Claude at something you can score and it iterates on it for you — propose a change, run your test, keep the change only if the metric improved, revert it if not, until it hits your budget, target, or a plateau. See the [auto-optimize repo](https://github.com/Zxela/auto-optimize) for full documentation.

## Structure

Plugins live as git submodules under `plugins/`, which gives you a local checkout of each
plugin's source for development. The `.claude-plugin/marketplace.json` file defines plugin
metadata and versions for the marketplace.

Note that Claude Code clones this repo **without** recursing submodules when it adds the
marketplace, so a submodule path is not a usable `source`. Entries should point at the
plugin's own repo with a `github` source so installs resolve:

```json
"source": { "source": "github", "repo": "Zxela/auto-optimize" }
```

## Installation

Add the marketplace in Claude Code:

```
/plugin marketplace add Zxela/claude-plugins
```

Then install individual plugins (the marketplace name is `zxela-local`, from
`marketplace.json`):

```
/plugin install auto-optimize@zxela-local
/plugin install homerun@zxela-local
```

## Development Setup

```sh
git clone --recurse-submodules https://github.com/Zxela/claude-plugins.git
```

If already cloned without submodules:

```sh
git submodule update --init --recursive
```
