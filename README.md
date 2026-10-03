# HowToFix CLI — release artifacts

This repository holds **release artifacts only** for the HowToFix coding agent CLI.

There is no source code here. HowToFix is proprietary software: the source lives
in a private repository, and this repository exists so the CLI can be installed
and updated without publishing it as open source.

## Install

Requires **Node 22.19 or newer** (`node --version`).

From the npm registry:

```sh
npm install -g howtofixcli
```

Or from the tarball attached to the latest release:

```sh
npm install -g ./howtofixcli-0.3.0.tgz
```

Check it:

```sh
howtofix --version
```

If `howtofix` is not on your `PATH`, your npm prefix is not on it:

```sh
npm config get prefix
export PATH="$(npm config get prefix)/bin:$PATH"
```

## First run

```
howtofix
```

Then connect your howtofix.id account:

```
/connect
```

It opens <https://howtofix.id/console/token>, asks for the token, verifies it
against the gateway, pulls the model list, and picks a model that answers. After
that, describe what you want in plain language:

```
fix the failing test in src/auth
```

## Releases

Each release carries the installable `.tgz` as an asset, built from the private
source. Download the newest one, or use the registry.

## Licence

Proprietary. See [LICENSE](LICENSE). Installing this package grants the right to
run it; it grants no right to the source, and redistribution and modification are
not permitted.

For licensing enquiries: <https://howtofix.id>
