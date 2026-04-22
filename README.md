# DankWebSearch

A launcher plugin for [DankMaterialShell](https://github.com/AvengeMedia/DankMaterialShell) that adds web search to the DMS launcher.

## Features

- Search DuckDuckGo, Google, Wikipedia, GitHub, and YouTube from the launcher
- Engine prefixes for quick switching (`g`, `w`, `gh`, `yt`)
- Direct URL detection — type a URL to open it
- Configurable default search engine

## Installation

### Nix (flake)

Add as a `flake = false` input and include in your DMS plugin configuration:

```nix
inputs.dms-plugin-websearch = {
  url = "github:alcxyz/DankWebSearch";
  flake = false;
};
```

```nix
programs.dank-material-shell.plugins.DankWebSearch = {
  enable = true;
  src = inputs.dms-plugin-websearch;
};
```

### Manual

Copy the plugin directory to `~/.config/DankMaterialShell/plugins/DankWebSearch/`.

## Usage

Activate with `!` (default trigger) in the DMS launcher, then:

- `!hello world` — search DuckDuckGo for "hello world"
- `!g hello world` — search Google
- `!gh nix flake` — search GitHub
- `!yt music video` — search YouTube
- `!w nix` — search Wikipedia
- `!github.com` — open URL directly

## Requirements

- `xdg-open` (for opening URLs in the default browser)

## License

MIT
