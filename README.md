# xfce4-meta-theme

## xfce4-theme-backup

Backups themes of XFC4 desktop. Example:

```
xfce4-theme-backup mybackup cpio
```

Syntax is:

```
xfce4-theme-backup <name-of-the-archive> {tar|tbz|tbz2|cpio|cpiobz2}
```

and it will save your current themes in the archive file.

## xfc4-meta-theme

Simple BASH-tool saving/loading/listing XFCE4 "meta"-theme. You can save your
current UI (visual) settings, then to load it. It's useful to switch all themes:

- xfce4-panel (currently is not implemented)
- xfce4-desktop
- xfwm4
- xsettings
- thunar (currently is not implemented)
- xfce4-terminal

in one "meta"-theme file treating them as one complex theme.

**It includes even visual settings of a XFCE4 terminal (colors, background...)
as well as window decorations, the desktop settings (wallpaper, etc), icon theme,
cursors...**

Examples:

```
# Save the current theme under its default name:
xfce4-meta-theme -save

# then list all saved:
xfce4-meta-theme -list

# then load some (WITHOUT EXTENSION and FULL PATH: JUST NAME!):
xfce4-meta-theme -load Sunset-Dark
```

The syntax is:

```
xfce4-meta-theme {-list|-save [NAME|PATH]|-load {NAME|PATH|_prev|_last}}
```

I.e., optionally you can pass a name or a full path when you save a meta-theme,
the same - when you load a meta-theme.

When loading meta-themes, you can also use special names like "_prev" and "_last".

All meta-themes are saved by default in: `~/.local/share/xfce4-metathemes`.

## xfce4-terminal-profile

Very similar to `xfce4-meta-theme` but manage only the terminal. It was written
before `xfce4-meta-theme`.

Better use `xfce4-meta-theme`.


Planned: support of array properties.