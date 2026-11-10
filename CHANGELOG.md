# Changelog

Also at https://icons.oma-kase.com/changelog

## 0.6.0 (2026-11-10): Sharper at small sizes

This release is about how the icons look on screen, most of all at 16px.

## Sharper at 16, 20 and 24px

One drawing can't sit on the pixel grid at every size, so thin lines used to blur. The build now makes a copy of each icon for 16px and 20px, moved onto that size's pixel grid, and the 24px drawing is snapped too. You get the right one automatically from the `size` you set.

Across the whole set, the share of blurred pixels drops from about 79% to 70% on standard screens and from 48% to 34% on high-density screens.

![All icons at 16px: before on the left, after on the right](https://icons.oma-kase.com/changelog/0.6.0/sharper-16px.png)

To make this work, the default stroke at small sizes is slightly heavier: 16px and 20px now draw a 1.5px line, the same as 24px. The default `strokeWidth` is 2.25 at 16px (was 2) and 1.8 at 20px (was 1.75). If you set `strokeWidth` yourself, nothing changes for you, and you get the 24px drawing at the weight you asked for.

## Solid icons keep their curves

Circles cut out of solid icons, like the lens of the camera or the centre of the gear, came out as rounded squares. They are now round.

## 13 icons redrawn

We now measure every icon against a written set of drawing rules: size, centring, and whether gaps stay open at 16px. Thirteen icons failed and were redrawn:

- **Gaps that closed at 16px:** folder, smartphone, calculator, barcode, paperclip and toggle-left.
- **Off centre:** play, key and crown.
- **Outside the canvas at small sizes:** user-plus and thermometer.
- **Too small:** close.
- **Refresh** has a new arrowhead that joins the arc cleanly.

Paperclip changed most: it is now upright.

![The redrawn icons: before on top, after below](https://icons.oma-kase.com/changelog/0.6.0/redrawn.png)

## One new icon

**Umbrella** joins the set, bringing it to 151.

## A new site

[icons.oma-kase.com](https://icons.oma-kase.com) has a new design: a hero that shows one drawing turning into every style, an icon browser with a detail panel and size guides, and a darker dark mode.

## Upgrading

Install the new version as usual. Three things to know:

- Icons at 16px and 20px look slightly bolder unless you set `strokeWidth`.
- The 13 redrawn icons look different, paperclip and refresh most of all.
- Each icon carries a little more data, about 640 bytes, for the 16px and 20px drawings.

## 0.5.1 (2026-11-08): A changelog, a roadmap and a dark mode

No icon changes in this release. It's about making the library easier to find, follow and use.

![The new changelog page in dark mode](https://icons.oma-kase.com/changelog/0.5.1/changelog-dark.png)

## Follow every release

- **Changelog.** Every release gets its own page with the new icons and a picture of what changed. Subscribe with the [RSS feed](https://icons.oma-kase.com/changelog/rss.xml).
- **Roadmap.** See what we're working on now, what's next and what we're exploring on the [roadmap](https://icons.oma-kase.com/roadmap).
- **FAQ.** Answers on licensing, installation, styles, accessibility and the MCP server in the [FAQ](https://icons.oma-kase.com/faq).
- **About.** Why we draw every icon once, on the [About](https://icons.oma-kase.com/about) page.

## Dark mode

The site now has a dark theme in the Omakase night palette. It follows your system setting, and the switch in the header remembers your choice.

## SVG code on every icon page

Every icon page now shows the SVG code with a copy button, next to the downloads for all 8 styles.

## Clearer npm packages

Each package now has its own description and keywords, so you can find it by searching npm for your framework. The READMEs link to the changelog, roadmap and FAQ, and spell out the license: free for commercial use, with no attribution needed in your product.

Releases are now published straight from our build pipeline with npm trusted publishing, so no long-lived publish token exists that could leak.

## 0.5.0 (2026-11-08): 150 icons, Vue and Svelte, and an MCP server for AI coding tools

## 50 new icons

Developer tools (code, terminal, git, database, server), money (banknote, coins, landmark, calculator, euro), commerce and shipping, health, and more calendar, map and zoom controls.

## "Off" icons that work in every style

`bell-off`, `mic-off`, `video-off`, `wifi-off` and `cloud-off` use a new slash that cuts a clean gap through the icon underneath. The gap stays clear in solid and duotone too.

## Install from npm

Every framework gets the same options: `variant`, `corner`, `size`, `strokeWidth`, `color` and `title`.

```bash
npm i @uv-foundry/icons-react
npm i @uv-foundry/icons-vue
npm i @uv-foundry/icons-svelte
npm i @uv-foundry/icons-core
```

All four packages share one renderer, so an icon looks identical in React, Vue, Svelte and plain SVG. Each icon is its own export, so your bundle only includes the icons you use.

## An MCP server for AI coding tools

AI assistants often guess icon names that don't exist. Connect the Omakase MCP server and your assistant searches the real catalog and gets working code for your framework. If it asks for an icon that doesn't exist, it gets the closest real matches instead of a broken import.

```bash
claude mcp add --transport http omakase-icons https://icons.oma-kase.com/mcp
```

No account or API key needed.

## Smaller files

SVG files are now optimised at build time and average about 430 bytes.

## 0.4.0 (2026-11-08): The first 100 icons, every style from one drawing

The first public set: 100 icons that cover the screens most products start with, from navigation and forms to media, commerce and files.

## One drawing, every style

Each icon is drawn once as a skeleton on a 24px grid. Every style is generated from that drawing, so a solid icon always matches its stroke version exactly:

- **Stroke**, **solid**, **duotone** and **twotone**
- **Rounded** or **sharp** corners
- Five stroke weights, from 1 to 2

## Weight that adapts to size

Thin lines blur on small screens. Icons now pick their stroke weight from their size: 2 at 16px, 1.75 at 20px and 1.5 at 24px and above. You can still set your own weight.

## Built for the UAE from day one

The set includes the new UAE dirham symbol (`currency-aed`), drawn to match the rest of the icons.

## Where to get them

- An explorer at icons.oma-kase.com with search, style controls and a page for every icon
- SVG downloads in every style
- A React component for every icon
