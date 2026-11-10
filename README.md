# Omakase Icons

151 free icons, each drawn once and generated in every style: stroke, solid, duotone and two-tone, with rounded or sharp corners, at any stroke weight. MIT licensed.

**[Browse all icons](https://icons.oma-kase.com/icons)** · **[Request an icon](https://github.com/neueworld/omakase-icons/issues/new?template=icon-request.yml)** · **[Report a problem](https://github.com/neueworld/omakase-icons/issues/new?template=bug.yml)**

[![Omakase Icons: one drawing, every style](https://icons.oma-kase.com/opengraph-image)](https://icons.oma-kase.com)

## Install

```bash
npm i @uv-foundry/icons-react    # React
npm i @uv-foundry/icons-vue      # Vue 3
npm i @uv-foundry/icons-svelte   # Svelte 5
npm i @uv-foundry/icons-core     # any framework, or plain SVG strings
```

```jsx
import { HomeIcon } from '@uv-foundry/icons-react';

<HomeIcon />
<HomeIcon variant="solid" corner="sharp" size={16} />
```

Every package takes the same options:

| Option | Values | Default |
|---|---|---|
| `variant` | `stroke`, `solid`, `duotone`, `twotone` | `stroke` |
| `corner` | `rounded`, `sharp` | `rounded` |
| `size` | any number of pixels | `24` |
| `strokeWidth` | 1 to 2.25 | fits the size: 2.25 at 16px, 1.8 at 20px, 1.5 at 24px |
| `color` | any CSS colour | `currentColor` |
| `title` | accessible label | none (the icon is hidden from screen readers) |

At 16px and 20px the icons use a drawing snapped to that size's pixel grid, so thin lines stay sharp.

## Use it from an AI coding tool

The MCP server lets Claude Code, Cursor and other assistants search the real catalog, so they never import an icon that doesn't exist. No sign-in.

```bash
claude mcp add --transport http omakase-icons https://icons.oma-kase.com/mcp
```

Setup for other tools: [icons.oma-kase.com/mcp-server](https://icons.oma-kase.com/mcp-server)

## Plain SVG files

The [`svg/`](svg) folder has every icon as a standalone file, by style and corner: `svg/<style>/<corner>/<name>.svg`. [`icons.json`](icons.json) lists every icon name.

## Request an icon or report a problem

- **[Request an icon](https://github.com/neueworld/omakase-icons/issues/new?template=icon-request.yml)** that is missing from the set. Requests decide what gets drawn next.
- **[Report a problem](https://github.com/neueworld/omakase-icons/issues/new?template=bug.yml)** with an icon that looks wrong or does not render.

## What's in this repository

This repository holds the published icons: the SVG files, the icon list, the licence and the [changelog](CHANGELOG.md). It is generated from our drawing source on every release, so please open an issue rather than a pull request.

## License

[MIT](LICENSE). Free for personal and commercial use, with no attribution required in your product.

Version 0.6.1. Made by [Omakase](https://oma-kase.com).
