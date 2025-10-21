[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/envsa/ddev-pnpm/actions/workflows/tests.yml/badge.svg)](https://github.com/envsa/ddev-pnpm/actions/workflows/tests.yml) 
[![last commit](https://img.shields.io/github/last-commit/ddev/ddev-addon-template)](https://github.com/ddev/ddev-addon-template/commits)
[![release](https://img.shields.io/github/v/release/ddev/ddev-addon-template)](https://github.com/ddev/ddev-addon-template/releases/latest)

<div align="center">
    <a href="https://ddev.com/">
        <img src="https://raw.githubusercontent.com/ddev/ddev/master/images/ddev-logo.svg" alt="DDEV logo" height="80">
    </a>
    <a href="https://pnpm.io">
        <img src="https://avatars.githubusercontent.com/u/21320719?s=200&v=4" alt="pnpm Logo" height="80">
    </a>
    <h1 align="center">ddev-pnpm</h1>
</div>

## Overview

This add-on integrates pnpm into your [DDEV](https://ddev.com/) project.

## Installation
```bash
ddev add-on get envsa/ddev-pnpm
ddev restart
```

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

To configure this addon to run PNPM commands for this example project, set a `PNPM_DIRECTORY` environment variable to `frontend`. For example: `.ddev/.env`

```env
PNPM_DIRECTORY=frontend
```

## Credits
**Contributed and maintained by @rellafella**
