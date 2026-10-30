# Sumi for Pi

A dark theme for [Pi](https://pi.dev) and [oh-my-pi](https://github.com/can1357/oh-my-pi) (`omp`): ink-black surfaces with a muted teal accent. It uses the same palette as the [Sumi Omarchy theme](https://github.com/suvikyi/omarchy-sumi-theme).

## Install for Pi

The repo is a Pi package:

```bash
pi install git:github.com/suvikyi/pi-sumi-theme
```

Then pick `sumi` in `/settings`, or copy `themes/sumi.json` to
`~/.pi/agent/themes/sumi.json` instead.

## Install for oh-my-pi

oh-my-pi only discovers themes in `~/.omp/agent/themes`; themes inside installed
plugins are not scanned, so install the file directly:

```bash
mkdir -p ~/.omp/agent/themes
curl -fsSL https://raw.githubusercontent.com/suvikyi/pi-sumi-theme/main/themes/sumi.json \
  -o ~/.omp/agent/themes/sumi.json
```

Then pick `sumi` in `/settings` → Appearance → Dark Theme, or set it directly:

```bash
omp config set theme.dark sumi
```

Sumi is dark-only. If you also want it in the light slot, set `theme.light` to
`sumi` as well.

For development, symlink the file instead of copying it:

```bash
ln -sf "$PWD/themes/sumi.json" ~/.omp/agent/themes/sumi.json
```

## Terminal background

A theme cannot set your terminal's background. For the full look, set the terminal profile background to `#121212` (and the foreground to `#dadad5`).

## Palette

| Role | Color |
| --- | --- |
| Background | `#121212` |
| Darker background | `#080808` |
| Panel | `#202020` |
| Foreground | `#dadad5` |
| Accent | `#72aba4` |
| Accent (bright) | `#87c1bb` |
| Selection | `#2d4541` |
| Red | `#e87366` |
| Green | `#8ca882` |
| Yellow | `#c69963` |
| Blue | `#85a2be` |
| Magenta | `#c08da7` |

The theme maps this palette onto the full oh-my-pi token set: markdown, tool blocks, diffs, syntax highlighting, thinking levels, bash/python mode, status line, and HTML export.

## Files

- `themes/sumi.json` — the theme
- `package.json` — Pi/omp package manifest
