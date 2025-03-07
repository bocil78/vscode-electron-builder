# Electron Builder for Visual Studio Code

[![The MIT License](https://flat.badgen.net/badge/license/MIT/orange)](http://opensource.org/licenses/MIT)
[![GitHub](https://flat.badgen.net/github/release/idleberg/vscode-electron-builder)](https://github.com/idleberg/vscode-electron-builder/releases)
[![Visual Studio Marketplace](https://vsmarketplacebadge.apphb.com/installs-short/idleberg.electron-builder.svg?style=flat-square)](https://marketplace.visualstudio.com/items?itemName=idleberg.electron-builder)
[![CI](https://img.shields.io/github/workflow/status/idleberg/vscode-electron-builder/CI?style=flat-square)](https://github.com/idleberg/vscode-electron-builder/actions)

Build system for [Electron Builder](https://www.electron.build/).

## Installation

### Extension Marketplace

Launch Quick Open, paste the following command, and press <kbd>Enter</kbd>

`ext install electron-builder`

### Packaged Extension

Download the package extension from the the [release page](https://github.com/idleberg/vscode-electron-builder/releases) and install it from the command-line:

```bash
$ code --install-extension path/to/electron-builder-*.vsix
```

Alternatively, you can download the packaged extension from the [Open VSX Registry](https://open-vsx.org/) or install it using the [`ovsx`](https://www.npmjs.com/package/ovsx) command-line tool:

```bash
$ ovsx get idleberg.electron-builder
```

### Clone Repository

Change to your Visual Studio Code extensions directory:

```bash
# Windows
$ cd %USERPROFILE%\.vscode\extensions

# Linux & macOS
$ cd ~/.vscode/extensions/
```

Clone repository as `electron-builder`:

```bash
$ git clone https://github.com/idleberg/vscode-electron-builder electron-builder
```

## Usage

### Prerequisites

By default, `electron-builder` is expected to be installed as a local `dependency`. Alternatively, you can specify the path to `electron-builder` in your [user settings](https://code.visualstudio.com/docs/customization/userandworkspace).

Electron Builder expects your project to include the [`electron`](https://www.npmjs.com/package/electron) module as a `devDependency`. Likewise, if you want to work with TOML configurations, you need to install the [`toml`](https://www.npmjs.com/package/toml) module as a `devDependency`.

### Building

You can run the _Electron Builder: Build_ from the [command-palette](https://code.visualstudio.com/docs/editor/codebasics#_command-palette) or from the title menu when opening a configuration file. When no such file has been opened, your workspace will be scanned for eligible configurations.

Configuration Precedence:

- extension settings using `--config` option
- `package.json` with `build` field
- `electron-builder.yml`
- `electron-builder.yaml`
- `electron-builder.json`
- `electron-builder.toml` (requires [`toml`](https://www.npmjs.com/package/toml))
- `electron-builder.js`

### Options

#### `pathToElectronBuilder`

Type: `string`  
Default: `${workspaceFolder}/node_modules/.bin/electron-builder`

Path to your `electron-builder`, defaults to your locally installed dependency

#### `electronBuilderArguments`

Type: `string[]`  
Default: `[]`

Custom arguments for electron builder

## Related

- [vscode-nsis](https://marketplace.visualstudio.com/items?itemName=idleberg.nsis)

## License

This work is licensed under [The MIT License](https://opensource.org/licenses/MIT)
