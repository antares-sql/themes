# Antares SQL themes

Themes for [Antares SQL](https://github.com/antares-sql/antares). A theme sets the colors of the interface **and** of the code editor, and can also change corner radii, border widths, the focus ring and the scrollbars (useful for accessibility themes).

## Install a theme

1. Open the folder of the theme below and download its `theme.json`.
2. In Antares open **Settings → Themes → Import from file** and pick the file.

Imported themes can be exported or removed from the same page. Themes need a version of Antares with theme support.

## Create a theme

A theme is a JSON file. Everything except `id`, `name` and `appearance` is optional: missing values are taken from the built-in dark or light theme.

```json
{
  "$schema": "https://raw.githubusercontent.com/antares-sql/themes/main/schema/theme.schema.json",
  "id": "my-theme",
  "name": "My theme",
  "appearance": "dark",
  "author": "Your name",
  "colors": { "bg-app": "#101418", "text": "#e6e6e6" },
  "shape": { "radius": "0.2rem" },
  "editor": {
    "colors": { "background": "#101418", "foreground": "#e6e6e6" },
    "syntax": { "keyword": { "color": "#ff9e64", "fontWeight": "bold" } }
  }
}
```

- **No code needed:** the [web theme editor](https://antares-sql.app/theme-editor) shows a live Antares window: click an element, change its colors, then export the JSON. It can start from the built-in themes or from any theme of this gallery.
- **Start from a complete theme:** [base/dark.json](base/dark.json) and [base/light.json](base/light.json) contain every value of the built-in themes. Every theme can also be exported from Antares (**Settings → Themes → Export**).
- **Try it while you work:** import it in Antares, edit the file and import it again (same `id` replaces it).
- **The schema** ([schema/theme.schema.json](schema/theme.schema.json)) lists every token: editors such as VS Code complete and check the file thanks to the `$schema` line.
- **Colors** are hex, `rgb()`/`rgba()`/`hsl()`/`hsla()` or CSS color names. `accent` means the color of the connection folder: themes can use it but never change it. Free CSS, `url()` and `var()` are not accepted.
- **Accessibility:** keep text readable (WCAG contrast 4.5:1 for text on its background). The text size is a separate Antares setting, so a theme doesn't need to change it.

## Publish a theme

1. Fork this repository and add `themes/<id>/theme.json` (the folder name is the theme `id`).
2. Add `themes/<id>/preview.png`: a screenshot of Antares with the theme, 1024×800, with a query tab, its results and the explorer visible.
3. Run `npm install` and `npm run build`: it validates the theme and generates its README and the index.
4. Open a pull request.

The themes tagged `ace` are the code editor themes Antares inherited from the Ace editor (BSD-3-Clause), turned into complete themes.

## Themes

<!-- THEMES:START -->
| Theme | Appearance | Preview |
|---|---|---|
| [Ambiance](themes/ambiance) | 🌙 Dark | <img src="themes/ambiance/preview.png" width="240"> |
| [Chaos](themes/chaos) | 🌙 Dark | <img src="themes/chaos/preview.png" width="240"> |
| [Chrome](themes/chrome) | ☀️ Light | <img src="themes/chrome/preview.png" width="240"> |
| [Clouds](themes/clouds) | ☀️ Light | <img src="themes/clouds/preview.png" width="240"> |
| [Clouds Midnight](themes/clouds-midnight) | 🌙 Dark | <img src="themes/clouds-midnight/preview.png" width="240"> |
| [Cobalt](themes/cobalt) | 🌙 Dark | <img src="themes/cobalt/preview.png" width="240"> |
| [Crimson Editor](themes/crimson-editor) | ☀️ Light | <img src="themes/crimson-editor/preview.png" width="240"> |
| [Dark Color-Blind Safe](themes/dark-color-blind-safe) | 🌙 Dark | <img src="themes/dark-color-blind-safe/preview.png" width="240"> |
| [Dawn](themes/dawn) | ☀️ Light | <img src="themes/dawn/preview.png" width="240"> |
| [Dracula](themes/dracula) | 🌙 Dark | <img src="themes/dracula/preview.png" width="240"> |
| [Dreamweaver](themes/dreamweaver) | ☀️ Light | <img src="themes/dreamweaver/preview.png" width="240"> |
| [Eclipse](themes/eclipse) | ☀️ Light | <img src="themes/eclipse/preview.png" width="240"> |
| [GitHub](themes/github) | ☀️ Light | <img src="themes/github/preview.png" width="240"> |
| [Green on Black](themes/gob) | 🌙 Dark | <img src="themes/gob/preview.png" width="240"> |
| [Gruvbox](themes/gruvbox) | 🌙 Dark | <img src="themes/gruvbox/preview.png" width="240"> |
| [High Contrast Dark](themes/high-contrast-dark) | 🌙 Dark | <img src="themes/high-contrast-dark/preview.png" width="240"> |
| [High Contrast Light](themes/high-contrast-light) | ☀️ Light | <img src="themes/high-contrast-light/preview.png" width="240"> |
| [Idle Fingers](themes/idle-fingers) | 🌙 Dark | <img src="themes/idle-fingers/preview.png" width="240"> |
| [IPlastic](themes/iplastic) | ☀️ Light | <img src="themes/iplastic/preview.png" width="240"> |
| [KatzenMilch](themes/katzenmilch) | ☀️ Light | <img src="themes/katzenmilch/preview.png" width="240"> |
| [krTheme](themes/kr-theme) | 🌙 Dark | <img src="themes/kr-theme/preview.png" width="240"> |
| [Kuroir](themes/kuroir) | ☀️ Light | <img src="themes/kuroir/preview.png" width="240"> |
| [Light Color-Blind Safe](themes/light-color-blind-safe) | ☀️ Light | <img src="themes/light-color-blind-safe/preview.png" width="240"> |
| [Merbivore](themes/merbivore) | 🌙 Dark | <img src="themes/merbivore/preview.png" width="240"> |
| [Mono Industrial](themes/mono-industrial) | 🌙 Dark | <img src="themes/mono-industrial/preview.png" width="240"> |
| [Monokai](themes/monokai) | 🌙 Dark | <img src="themes/monokai/preview.png" width="240"> |
| [Nord Dark](themes/nord-dark) | 🌙 Dark | <img src="themes/nord-dark/preview.png" width="240"> |
| [Pastel on Dark](themes/pastel-on-dark) | 🌙 Dark | <img src="themes/pastel-on-dark/preview.png" width="240"> |
| [Solarized Dark](themes/solarized-dark) | 🌙 Dark | <img src="themes/solarized-dark/preview.png" width="240"> |
| [Solarized Light](themes/solarized-light) | ☀️ Light | <img src="themes/solarized-light/preview.png" width="240"> |
| [SQL Server](themes/sqlserver) | ☀️ Light | <img src="themes/sqlserver/preview.png" width="240"> |
| [Terminal](themes/terminal) | 🌙 Dark | <img src="themes/terminal/preview.png" width="240"> |
| [TextMate](themes/textmate) | ☀️ Light | <img src="themes/textmate/preview.png" width="240"> |
| [Tomorrow](themes/tomorrow) | ☀️ Light | <img src="themes/tomorrow/preview.png" width="240"> |
| [Tomorrow Night](themes/tomorrow-night) | 🌙 Dark | <img src="themes/tomorrow-night/preview.png" width="240"> |
| [Tomorrow Night Blue](themes/tomorrow-night-blue) | 🌙 Dark | <img src="themes/tomorrow-night-blue/preview.png" width="240"> |
| [Tomorrow Night Bright](themes/tomorrow-night-bright) | 🌙 Dark | <img src="themes/tomorrow-night-bright/preview.png" width="240"> |
| [Tomorrow Night 80s](themes/tomorrow-night-eighties) | 🌙 Dark | <img src="themes/tomorrow-night-eighties/preview.png" width="240"> |
| [Twilight](themes/twilight) | 🌙 Dark | <img src="themes/twilight/preview.png" width="240"> |
| [Vibrant Ink](themes/vibrant-ink) | 🌙 Dark | <img src="themes/vibrant-ink/preview.png" width="240"> |
| [Xcode](themes/xcode) | ☀️ Light | <img src="themes/xcode/preview.png" width="240"> |
<!-- THEMES:END -->

## Maintainers

`schema/` (`theme.schema.json` and `tokens.json`, the token catalog read by the web editor) and `base/` are generated from the Antares sources, which are the reference for the tokens:
`node scripts/themeKit.js <path of this repository>` in the Antares repository. Previews can be regenerated with the real app:
`node scripts/themePreviews.js <path of this repository> [ids...]` (see the script for the setup).
