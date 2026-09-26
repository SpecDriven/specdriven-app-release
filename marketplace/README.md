# SpecDriven plugin marketplace

The plugin marketplace SpecDriven reads by default (Settings → Plugins →
Marketplaces): `marketplace.json`, the index, and each plugin as a zip file
under `plugins/`. Every index row names the plugin, its version,
description, category, plugin api and its zip, pinned to the zip's sha256.
The app checks the zip against it before it unpacks anything.

Installing a plugin is a consent step first: the app shows the plugin's
name, version, description and the permissions its manifest declares, and
notes that it runs in the app's own process with the app's rights.

## Deploying a plugin

Plugins are developed in any repository (SpecDriven's own are in
[SpecDriven/plugins](https://github.com/SpecDriven/plugins)) and deployed
here with the `specdriven` command. From a checkout of
[specdriven-app](https://github.com/SpecDriven/specdriven-app) beside this
repository:

```sh
bun src/index.ts plugin build ../plugins/plugins/models
bun src/index.ts plugin deploy ../plugins/plugins/models --to ../specdriven-app-release/marketplace
```

`plugin deploy` zips the built plugin (`package.json`, `dist/`, README and
LICENSE), writes it to `plugins/<id>-<version>.zip`, lists it in
`marketplace.json` and deletes the zip of the version it replaces. Commit
and push to publish; installed plugins pick the new version up with Update.
