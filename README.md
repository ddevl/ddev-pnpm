[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/ddev/ddev-pnpm/actions/workflows/tests.yml/badge.svg)](https://github.com/ddev/ddev-pnpm/actions/workflows/tests.yml) 
[![last commit](https://img.shields.io/github/last-commit/ddev/ddev-pnpm)](https://github.com/ddev/ddev-pnpm/commits)
[![release](https://img.shields.io/github/v/release/ddev/ddev-pnpm)](https://github.com/ddev/ddev-pnpm/releases/latest)

## DDEV pnpm

## Overview

[pnpm](https://pnpm.io/) is a fast, disk space efficient package manager.

This add-on integrates `pnpm` into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get ddev/ddev-pnpm
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev pnpm` | Run pnpm from within the web container |

Please refer to the documentation at [pnpm.io](https://pnpm.io)

## Advanced Customization

By default, this add-on assumes your `package.json` is in the root of the DDEV project.

In a monorepo that doesn't have a root level `package.json`, e.g.

```md
.
├── .ddev
├── backend/
│   └── composer.json
└── frontend/
    └── package.json
```

To configure this addon to run `pnpm` commands for this example project, set a `PNPM_DIRECTORY` environment variable to `frontend`:

```bash
ddev dotenv set .ddev/.env.web --pnpm-directory=frontend
```

Make sure to commit the `.ddev/.env.web` file to version control.

## Credits

**Contributed and maintained by [@rellafella](https://github.com/rellafella)**
