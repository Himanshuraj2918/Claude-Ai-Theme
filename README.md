# Claude AI Theme for VS Code

A dark + light VS Code theme matching claude.ai's color system: warm terracotta accent
(`#DA7756` / `#C1663F`), cream/near-black neutrals, and one consistent color per token
type (comments, strings, keywords, functions, types, variables, etc).

## Install (no publishing needed)

1. Copy this whole `claude-ai-theme` folder into your VS Code extensions directory:
   - macOS/Linux: `~/.vscode/extensions/`
   - Windows: `%USERPROFILE%\.vscode\extensions\`
2. Restart VS Code.
3. `Cmd/Ctrl+K Cmd/Ctrl+T` → pick **Claude AI Dark** or **Claude AI Light**.

Or, to test without installing: open this folder in VS Code and press **F5** — it
launches an Extension Development Host with the theme already active.

## About the font

Claude.ai's actual headline/body typefaces (Styrene and Tiempos) are licensed
commercial fonts, not available as free web/system fonts — so they can't be bundled
here. Claude's code blocks specifically use **JetBrains Mono**, so that's what this
theme recommends for the editor. Add this to your `settings.json` (global or
per-workspace) to match:

```json
{
  "editor.fontFamily": "'JetBrains Mono', 'SF Mono', Menlo, Consolas, monospace",
  "editor.fontLigatures": true,
  "editor.fontSize": 14
}
```

[Download JetBrains Mono free here](https://www.jetbrains.com/lp/mono/) if you don't
have it installed — the theme still works with any monospace font, this just gets you
closest to the claude.ai look.

To get the best experience with this theme, install the **JetBrains Mono** font before using it in VS Code.

### Steps

1. Download **JetBrains Mono** from the official website.
2. Extract the downloaded ZIP file.
3. Open the extracted folder and navigate to:

   ```text
   fonts/ttf
   ```

4. Locate the font files, such as:

   ```text
   JetBrainsMono-Regular.ttf
   JetBrainsMono-Bold.ttf
   JetBrainsMono-Italic.ttf
   ```

5. Select all the `.ttf` files, right-click, and choose:

   - **Install**, or
   - **Install for all users** (recommended, if available).

6. After the installation is complete, restart **Visual Studio Code**.

## Color reference

| Role | Dark | Light |
|---|---|---|
| Background | `#141413` | `#FAF9F5` |
| Foreground | `#E8E6E3` | `#2C2C2C` |
| Accent (keywords, tags) | `#DA7756` | `#C1663F` |
| Strings | `#B4C494` | `#5C7A3E` |
| Functions | `#7BA88A` | `#4E8264` |
| Types/Classes | `#6FAFA6` | `#3D7D74` |
| Numbers/Constants | `#D6A756` | `#A87A24` |
| Comments | `#7A776E` (italic) | `#9B9689` (italic) |

## Editing further

All colors live in `themes/claude-dark-color-theme.json` and
`themes/claude-light-color-theme.json`. Two sections:
- `colors` — workbench UI (sidebar, tabs, terminal, status bar)
- `tokenColors` / `semanticTokenColors` — syntax highlighting per token type

Change a hex value and reload the window (`Cmd/Ctrl+R` in the Dev Host, or
`Developer: Reload Window` once installed) to see it live.
