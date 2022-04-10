oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g @evtity/cli
$ ev COMMAND
running command...
$ ev (--version)
@evtity/cli/0.0.0 linux-x64 node-v14.15.1
$ ev --help [COMMAND]
USAGE
  $ ev COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`ev hello PERSON`](#ev-hello-person)
* [`ev hello world`](#ev-hello-world)
* [`ev help [COMMAND]`](#ev-help-command)
* [`ev plugins`](#ev-plugins)
* [`ev plugins:install PLUGIN...`](#ev-pluginsinstall-plugin)
* [`ev plugins:inspect PLUGIN...`](#ev-pluginsinspect-plugin)
* [`ev plugins:install PLUGIN...`](#ev-pluginsinstall-plugin-1)
* [`ev plugins:link PLUGIN`](#ev-pluginslink-plugin)
* [`ev plugins:uninstall PLUGIN...`](#ev-pluginsuninstall-plugin)
* [`ev plugins:uninstall PLUGIN...`](#ev-pluginsuninstall-plugin-1)
* [`ev plugins:uninstall PLUGIN...`](#ev-pluginsuninstall-plugin-2)
* [`ev plugins update`](#ev-plugins-update)

## `ev hello PERSON`

Say hello

```
USAGE
  $ ev hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Whom is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/evtity/evtity-cli.git/https://github.com/evtity/evtity-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `ev hello world`

Say hello world

```
USAGE
  $ ev hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `ev help [COMMAND]`

Display help for ev.

```
USAGE
  $ ev help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for ev.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `ev plugins`

List installed plugins.

```
USAGE
  $ ev plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ ev plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `ev plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ ev plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ ev plugins add

EXAMPLES
  $ ev plugins:install myplugin 

  $ ev plugins:install https://github.com/someuser/someplugin

  $ ev plugins:install someuser/someplugin
```

## `ev plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ ev plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ ev plugins:inspect myplugin
```

## `ev plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ ev plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ ev plugins add

EXAMPLES
  $ ev plugins:install myplugin 

  $ ev plugins:install https://github.com/someuser/someplugin

  $ ev plugins:install someuser/someplugin
```

## `ev plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ ev plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.

EXAMPLES
  $ ev plugins:link myplugin
```

## `ev plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ ev plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ ev plugins unlink
  $ ev plugins remove
```

## `ev plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ ev plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ ev plugins unlink
  $ ev plugins remove
```

## `ev plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ ev plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ ev plugins unlink
  $ ev plugins remove
```

## `ev plugins update`

Update installed plugins.

```
USAGE
  $ ev plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
