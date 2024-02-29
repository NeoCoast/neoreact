oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g @neocoast/neoreact
$ neoreact COMMAND
running command...
$ neoreact (--version)
@neocoast/neoreact/0.0.0 darwin-arm64 node-v21.6.2
$ neoreact --help [COMMAND]
USAGE
  $ neoreact COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`neoreact hello PERSON`](#neoreact-hello-person)
* [`neoreact hello world`](#neoreact-hello-world)
* [`neoreact help [COMMANDS]`](#neoreact-help-commands)
* [`neoreact plugins`](#neoreact-plugins)
* [`neoreact plugins:install PLUGIN...`](#neoreact-pluginsinstall-plugin)
* [`neoreact plugins:inspect PLUGIN...`](#neoreact-pluginsinspect-plugin)
* [`neoreact plugins:install PLUGIN...`](#neoreact-pluginsinstall-plugin-1)
* [`neoreact plugins:link PLUGIN`](#neoreact-pluginslink-plugin)
* [`neoreact plugins:uninstall PLUGIN...`](#neoreact-pluginsuninstall-plugin)
* [`neoreact plugins reset`](#neoreact-plugins-reset)
* [`neoreact plugins:uninstall PLUGIN...`](#neoreact-pluginsuninstall-plugin-1)
* [`neoreact plugins:uninstall PLUGIN...`](#neoreact-pluginsuninstall-plugin-2)
* [`neoreact plugins update`](#neoreact-plugins-update)

## `neoreact hello PERSON`

Say hello

```
USAGE
  $ neoreact hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/NeoCoast/neoreact/blob/v0.0.0/src/commands/hello/index.ts)_

## `neoreact hello world`

Say hello world

```
USAGE
  $ neoreact hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ neoreact hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/NeoCoast/neoreact/blob/v0.0.0/src/commands/hello/world.ts)_

## `neoreact help [COMMANDS]`

Display help for neoreact.

```
USAGE
  $ neoreact help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for neoreact.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.0.12/src/commands/help.ts)_

## `neoreact plugins`

List installed plugins.

```
USAGE
  $ neoreact plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ neoreact plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/index.ts)_

## `neoreact plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ neoreact plugins add plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ neoreact plugins add

EXAMPLES
  $ neoreact plugins add myplugin 

  $ neoreact plugins add https://github.com/someuser/someplugin

  $ neoreact plugins add someuser/someplugin
```

## `neoreact plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ neoreact plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ neoreact plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/inspect.ts)_

## `neoreact plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ neoreact plugins install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ neoreact plugins add

EXAMPLES
  $ neoreact plugins install myplugin 

  $ neoreact plugins install https://github.com/someuser/someplugin

  $ neoreact plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/install.ts)_

## `neoreact plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ neoreact plugins link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ neoreact plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/link.ts)_

## `neoreact plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ neoreact plugins remove plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ neoreact plugins unlink
  $ neoreact plugins remove

EXAMPLES
  $ neoreact plugins remove myplugin
```

## `neoreact plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ neoreact plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/reset.ts)_

## `neoreact plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ neoreact plugins uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ neoreact plugins unlink
  $ neoreact plugins remove

EXAMPLES
  $ neoreact plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/uninstall.ts)_

## `neoreact plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ neoreact plugins unlink plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ neoreact plugins unlink
  $ neoreact plugins remove

EXAMPLES
  $ neoreact plugins unlink myplugin
```

## `neoreact plugins update`

Update installed plugins.

```
USAGE
  $ neoreact plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/update.ts)_
<!-- commandsstop -->
