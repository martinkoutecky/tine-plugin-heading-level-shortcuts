# Heading level shortcuts for Tine

A behavioral port of Richard Yu's MIT-licensed [Logseq heading-level shortcuts](https://github.com/vipzhicheng/logseq-plugin-heading-level-shortcuts), pinned to revision `40b5a57577d4ab168dea38614eebe3b42085b665`.

![The original plugin's heading shortcut demonstration](https://raw.githubusercontent.com/vipzhicheng/logseq-plugin-heading-level-shortcuts/40b5a57577d4ab168dea38614eebe3b42085b665/screencast.gif)

## How to use it

Install and enable the plugin, edit a block, then press `Ctrl+Alt+0` through `Ctrl+Alt+6` (`Cmd+Alt` on macOS). Level 0 clears the heading. The commands also appear in Ctrl-K and in **Settings -> Keyboard shortcuts**, where every chord can be changed.

The original plugin defaults to `Cmd/Ctrl+0…6`. Tine reserves `Cmd/Ctrl+1…9` for focusing numbered panes, so this port adds Alt instead of silently overriding a core navigation shortcut. You can remap either command if you prefer the original binding.

Markdown headings use `#` prefixes. Org blocks use Logseq's `heading` block property. Tine supplies only the focused block's id, exact text, parent/depth, and format; the plugin cannot read other blocks. Changes use an expected-text host effect, normal Undo, and Tine's conflict-safe save path.

## Development and safety

Build with `cargo build --release`, then run Tine's `plugin:check` on this directory. This AI-primary port has no filesystem, network, DOM, process, or arbitrary graph access. The original and this port are MIT-licensed; see `LICENSE`.
