<div align="center">
  <img
    src="installed-check.svg"
    width="650"
    height="auto"
    alt="installed-check"
  />
</div>

<div align="center">

[![npm version](https://img.shields.io/npm/v/installed-check.svg?style=flat)](https://www.npmjs.com/package/installed-check)
[![npm downloads](https://img.shields.io/npm/dm/installed-check.svg?style=flat)](https://www.npmjs.com/package/installed-check)
[![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg)](https://github.com/voxpelli/eslint-config)
[![Follow @voxpelli@mastodon.social](https://img.shields.io/mastodon/follow/109247025527949675?domain=https%3A%2F%2Fmastodon.social&style=social)](https://mastodon.social/@voxpelli)

</div>

Checks that the installed modules comply fulfill the requirements of package.json.

By default checks both engine and module versions against requirements.

## Usage

### Command line

```sh
npm install -g installed-check
```

Then run it at the root of your project to validate the installed dependencies:

```sh
installed-check
```

### As npm script

```sh
npm install --save-dev installed-check
```

```json
"scripts": {
  "test": "installed-check"
}
```

### Programmatic use

Use [installed-check-core](https://github.com/voxpelli/node-installed-check-core)

## Options

* `--engine-check` / `-e` – if set `installed-check` will check that the installed modules comply with the [engines requirements](https://docs.npmjs.com/files/package.json#engines) of the package.json and suggest an alternative requirement if the installed modules don't comply. If set, the default checks will be disabled.
* `--engine-ignore` / `-i` – if set then the specified module names won't be included in the engine check. `engineIgnores` should an array of module names while the CLI flags should be set once for each module name.
* `--engine-no-dev` / `-d` – if set then dev dependencies won't be included in the engine check.
* `--version-check` / `-c` – if set `installed-check` will check that the installed modules comply with the version requirements set for it the package.json. If set, the default checks will be disabled.

### Additional command line options

* `--help` / `-h` – prints all available flags
* `--strict` / `-s` – treats warnings as errors
* `--verbose` / `-v` – prints warnings and notices

## Similar modules

* [`knip`](https://github.com/webpro/knip) – finds unused files, dependencies and exports in your JavaScript and TypeScript projects – a great companion module to `installed-check`
