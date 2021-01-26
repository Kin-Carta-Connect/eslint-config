# K+C ESLint config

> The K+C recommended shareable config for ESLint.

It turns on all the possible errors rules within eslint based on our JS styleguide.

Use it as is or as a foundation for your own config. You can extend or clone and change.

## Installation

```bash
npm install -D @kinandcarta/eslint-config
```

## Usage

This package includes the following configurations:

* @kinandcarta/eslint-config - The base code style guide.
* @kinandcarta/eslint-config/node - To be used in addition to "@kinandcarta/eslint-config" configuration by projects that use Node.
* @kinandcarta/eslint-config/jest - To be used in addition to "@kinandcarta/eslint-config" configuration by projects that use [jest](https://facebook.github.io/jest/).
* @kinandcarta/eslint-config/react - To be used in addition to "@kinandcarta/eslint-config" configuration by projects that react [React](https://facebook.github.io/react/).

If you've installed `@kinandcarta/eslint-config` locally within your project, just set your eslint config to:

```json
{
  "extends": "@kinandcarta/eslint-config"
}
```

or if you are working on a Node script:

```json
{
  "extends": [
		"@kinandcarta/eslint-config"
		"@kinandcarta/eslint-config/node"
  ]
}
```

If you've globally installed @kinandcarta/eslint-config using the -g flag, then you'll need to use the absolute path to @kinandcarta/eslint-config in your config e.g.

```bash
{
  "extends": "/absolute/path/to/@kinandcarta/eslint-config"
}
```

You can also simply use the globally installed configuration name instead of the absolute path:

```json
{
  "extends": "@kinandcarta/eslint-config"
}
```

### Extending the config

Simply add a "rules" key to your config, then add your overrides and additions there.

For example, to change the comma-dangle rule to off:

```json
{
  "extends": "@kinandcarta/eslint-config",
  "rules": {
    "comma-dangle": "off",
  }
}
```

## Deploy

To deploy a new version, make sure you have a clean `node_modules` folder and then install the npm modules:

```bash
npm i --no-package-lock
```

The repository uses sematic release with the conventionalcommits preset to deploy releases.

Details regarding these types can be found in the official [CONTRIBUTING](CONTRIBUTING.md) guide.

## Complementary tools

### Editor plugins

* Sublime Text 3:
  * [SublimeLinter-eslint](https://github.com/roadhump/SublimeLinter-eslint)
  * [Build Next](https://github.com/albertosantini/sublimetext-buildnext)
* Vim:
  * [ALE](https://github.com/w0rp/ale)
  * [Syntastic](https://github.com/vim-syntastic/syntastic/tree/master/syntax_checkers/javascript)
* Emacs: [Flycheck](http://www.flycheck.org/) supports ESLint with the [javascript-eslint](http://www.flycheck.org/en/latest/languages.html#javascript) checker.
* Eclipse Orion: ESLint is the [default linter](https://dev.eclipse.org/mhonarc/lists/orion-dev/msg02718.html)
* Eclipse IDE: [Tern ESLint linter](https://github.com/angelozerr/tern.java/wiki/Tern-Linter-ESLint)
* TextMate 2: [ESLint Bundle](https://github.com/natesilva/javascript-eslint.tmbundle)
* Atom: [linter-eslint](https://atom.io/packages/linter-eslint)
* IntelliJ IDEA, RubyMine, WebStorm, PhpStorm, PyCharm, AppCode, Android Studio, 0xDBE: [ESLint Plugin](https://plugins.jetbrains.com/plugin/7494-eslint)
* Visual Studio Code: [ESLint Extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
* Brackets: Included and [Brackets ESLint](https://github.com/brackets-userland/brackets-eslint)

More integration tools can be found here https://eslint.org/docs/user-guide/integrations

### Find eslint rules

Find eslint rules that are not configured in your eslint config. This is useful to see what else is new and what is deprecated or updated.

Running this in your root folder will show the list.

```bash
npx eslint-find-rules
```

More info here https://github.com/sarbbottam/eslint-find-rules

### Inspiration

This config is heavily inspired by the following configs and tools:

- https://github.com/airbnb/javascript

## [Changelog](CHANGELOG.md)
