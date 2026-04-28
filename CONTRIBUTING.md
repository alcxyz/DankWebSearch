# Contributing to DankQuickSearch

## Development setup

Prerequisites: [DankMaterialShell](https://github.com/AvengeMedia/DankMaterialShell) >= 1.4.0

```bash
git clone https://github.com/alcxyz/DankQuickSearch.git
cd DankQuickSearch
```

For development, symlink the plugin into the DMS plugins directory:

```bash
ln -s "$(pwd)" ~/.config/DankMaterialShell/plugins/DankQuickSearch
```

Reload after changes:

```bash
dms ipc call plugins reload dankQuickSearch
```

## Project structure

- `plugin.json` -- plugin manifest (id, type, trigger, permissions)
- `DankQuickSearch.qml` -- main launcher component (getItems, executeItem)
- `DankQuickSearchSettings.qml` -- settings UI

## Making changes

1. Fork the repo and create a branch from `dev`
2. Make your changes
3. Test by reloading the plugin in DMS
4. Open a pull request against `dev`

## Commit messages

Use conventional-ish prefixes to keep history scannable:

- `feat:` new feature
- `fix:` bug fix
- `docs:` documentation only
- `chore:` maintenance, CI, dependencies
- `refactor:` code changes that don't add features or fix bugs

## Releasing

Releases are automated via GitHub Actions. The `version` field in `plugin.json` is the single source of truth.

To cut a release:

1. Bump the `version` field in `plugin.json` on `dev`
2. Merge `dev` into `main`
3. CI automatically creates the git tag and a GitHub release

### Version numbering

Follow [semver](https://semver.org/):

- **Patch** (`v0.1.x`): bug fixes, minor tweaks
- **Minor** (`v0.x.0`): new features, non-breaking changes
- **Major** (`vx.0.0`): breaking changes

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
