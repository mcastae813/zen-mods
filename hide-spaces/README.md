# Hide Spaces

Hides chosen spaces from the spaces strip at the bottom of Zen's sidebar, without deleting them.

- Rename a space so its name starts with `.` and its icon leaves the strip. Example: `Personal` → `.Personal` (right-click the space icon → **Edit Space**). Works right away, no restart. Rename it back to unhide it.
- The active space is never hidden, so the icon of a hidden space still shows while you're in it.
- Hold the mouse on the strip for a moment and the hidden spaces slide in, so you can click or right-click them. Move the mouse away and they're gone again.
- Only the strip changes: tabs, sync, keyboard shortcuts (Ctrl+Alt+Right / Ctrl+Alt+Left still cycle through every space), swipe gestures and **Manage Spaces…** still see every space.

## Settings

Edit the variables at the top of `chrome.css`:

| Variable | Default | Controls |
| --- | --- | --- |
| `--hs-reveal-delay` | `1s` | How long to hold the mouse on the strip before hidden spaces appear. `999s` = never. |
| `--hs-button-size` | `30px` | Zen's space-button size. Use `32px` on macOS. |

## Hiding by exact name (optional)

If you'd rather not rename a space, add its exact name to the `:is(...)` list in `chrome.css`, one per line with the comma first:

```css
:is(
  [tooltiptext^="."]
  , [tooltiptext="Personal"]
)
```

Names are case-sensitive. This way needs a full Zen restart after each change.

## Install

Download `hide-spaces.css` from the [latest release](https://github.com/mcastae813/zen-mods/releases), or use `chrome.css` from this folder, then follow [Installing a mod](../README.md#installing-a-mod).

## Notes

- Works alongside the store mod *Hide Inactive Workspaces*.
- `userChrome.css` is a user-level stylesheet, so every rule that has to beat Zen's own CSS uses `!important`.

---

Made with Claude Opus, Anthropic's AI model.
