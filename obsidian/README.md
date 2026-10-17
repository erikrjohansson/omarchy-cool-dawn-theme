# Cool Dawn for Obsidian (AnuPpuccin)

A small CSS snippet that adds the **Cool Dawn** palette (deep green-gray surfaces and sage accents) to the
[AnuPpuccin](https://github.com/AnubisNekhet/AnuPpuccin) Obsidian theme, so the
notes app matches the Omarchy desktop.

## What it changes

| Part of AnuPpuccin | Source |
|---|---|
| Surfaces: `base`, `mantle`, `crust`, `surface0-2` | `colors.toml` of this theme (`background`, `dark_background`, `darker_background`, `lighter_background`, `selection`, `hyprland_inactive_border`) |
| Neutral text: `text`, `subtext0-1`, `overlay0-2` | `colors.toml` (`bright_foreground`, `foreground`, `light_foreground`, `dark_foreground`, `hyprland_active_border`); `overlay0` is interpolated |
| Interface accent (`--ctp-accent`) | `accent` = `#A9C6B7` |
| The 14 colour accents (headings, callouts, Rainbow Folders, tags...) | **unchanged** - same values as AnuPpuccin's *Material Mint* flavour |

The Omarchy palettes are almost monochrome, so mapping their "red/green/blue/..."
entries onto Obsidian's coloured elements would make headings, callouts and
folders hard to tell apart. Keeping the accent colours untouched gives a themed
workspace without losing that information.

## Install

1. Install the AnuPpuccin theme and the *Style Settings* community plugin.
2. Copy [`cool-dawn-anuppuccin.css`](cool-dawn-anuppuccin.css) into `<your-vault>/.obsidian/snippets/`.
3. *Settings -> Appearance -> CSS snippets*: enable `cool-dawn-anuppuccin`.
4. *Style Settings -> Cool Dawn (AnuPpuccin companion)*: toggle **Cool Dawn palette**.

The palette only applies in dark mode.

## Notes

- The snippet is self-contained: it does **not** need AnuPpuccin's
  `extended-colorschemes.css`. It overrides the `--ctp-ext-*` variables that
  AnuPpuccin's flavours already read, scoped to the `anp-cool-dawn` body class that the
  toggle sets.
- Prefer one entry in AnuPpuccin's own "Dark theme flavor" drop-down? Copy the
  variable block into `extended-colorschemes.css` under a
  `.theme-dark.anp-theme-ext-dark.ctp-cool-dawn` selector and add a
  matching option to its `@settings` header.
