# Zen Mods

CSS mods for [Zen Browser](https://zen-browser.app/).

> **Disclaimer:** everything in this repo was made with Claude Opus, Anthropic's AI model.

| Mod | What it does |
| --- | --- |
| [Compact Folders](compact-folders/) | Closed sidebar folders become small icon tiles that sit side by side. Hover a tile to see its name. |
| [Hide Spaces](hide-spaces/) | Spaces whose name starts with `.` leave the spaces strip. Hold the mouse on the strip to bring them back. |

## Installing a mod

1. In Zen, open `about:support`, find **Profile Folder** and click **Open Folder**.
2. Create a `chrome` folder there if it doesn't exist.
3. Copy the mod's `chrome.css` into `chrome/` and give it a descriptive name, e.g. `compact-folders.css`.
4. Add an import line for it to `chrome/userChrome.css` (create the file if needed):

   ```css
   @import url("compact-folders.css");
   ```

5. Restart Zen.

If nothing changes, open `about:config`, set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`, and restart again.
