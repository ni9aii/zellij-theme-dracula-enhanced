# Dracula Enhanced for Zellij

A slightly tweaked version of the official [Dracula theme](https://draculatheme.com/) for [Zellij](https://zellij.dev/), with one key improvement: **visible text selection**.

## The Problem

The original Zellij Dracula theme uses the terminal background color (`40 42 54`) for selected text background. This makes text selection nearly invisible in most scenarios — you simply can't see what you've selected.

## The Fix

Changed the selection background from `40 42 54` to `68 71 90` (Dracula's "Current Line" color) in all selection contexts:

- `text_selected`
- `table_cell_selected`
- `list_selected`

Everything else — all colors, all UI elements — remains **100% authentic Dracula**.

## Installation

### Option 1: Direct download

```bash
curl -o ~/.config/zellij/themes/dracula-enhanced.kdl \
  https://raw.githubusercontent.com/ni9aii/zellij-theme-dracula-enhanced/main/dracula-enhanced.kdl
```

Then add to your `~/.config/zellij/config.kdl`:

```kdl
theme_dir "~/.config/zellij/themes"
theme "dracula-enhanced"
```

### Option 2: Copy-paste

Copy the contents of `dracula-enhanced.kdl` into your `config.kdl` inside the `themes { ... }` block, then set:

```kdl
theme "dracula-enhanced"
```

## Screenshot

*(TODO: add before/after screenshot)*

## License

Same as Zellij and Dracula — MIT/whatever they use. This is a trivial fork, no copyright claimed.
