# FargoRate Skill

![Version](https://img.shields.io/github/v/tag/rgstephens/fargo-skill?label=version&sort=semver)

A [ClawHub](https://clawhub.io/skills/fargorate) skill for the [FargoRate](https://fargorate.com) billiards rating system. Look up players, calculate match odds, get recommended race lengths, and track rating changes over time.

## Installation

```bash
curl -fsSL https://raw.githubusercontent.com/rgstephens/fargo-skill/main/install.sh | bash
```

Pin a specific version:

```bash
VERSION=v0.1.0 bash <(curl -fsSL https://raw.githubusercontent.com/rgstephens/fargo-skill/main/install.sh)
```

## Commands

| Command | Description |
|---------|-------------|
| `fargo search <name or id>` | Search players by name or FargoRate ID |
| `fargo lookup <id>` | Look up a single player by ID |
| `fargo bulk <id...>` | Look up multiple players at once |
| `fargo odds <r1> <r2> <race1> <race2>` | Calculate match win odds |
| `fargo races <r1> <r2>` | Get recommended race lengths |
| `fargo top` | View top 10 ranked players |
| `fargo setup` | Configure the tool |
| `fargo group` | Manage named groups of player IDs |

## Global Flags

| Flag | Description |
|------|-------------|
| `--db [path]` | Save player data to a local SQLite database |
| `--changes` | Only output players whose rating changed (requires `--db`) |
| `--json` | Output raw JSON |

## Examples

```bash
fargo search "John Smith"
fargo odds 550 480 7 9
fargo races 550 480 --type 0
fargo top --ranking US --gender F
fargo --changes --db bulk --group monday-league
```

## Releases

See [GitHub Releases](https://github.com/rgstephens/fargo-skill/releases) for changelog and version history.
