# MD_files

Personal Markdown notes, plus `index.html`: an offline viewer and editor for them. No server, no build step, no internet connection.

Start with the [welcome note](notes/welcome.md), or copy the [note template](templates/note.md).

## Layout

| Path | What goes there |
|:-----|:----------------|
| `notes/` | Notes, in subfolders by topic as the collection grows |
| `templates/` | Starting points to copy for new notes |
| `assets/` | Images referenced from notes |
| `index.html` | The viewer and editor |
| `licenses/` | Licenses for the two fonts embedded in `index.html` |
| `.github/workflows/pages.yml` | Publishes `index.html` (not the notes) to GitHub Pages |

## Daily use

1. **Pull** in GitHub Desktop so you start from the latest version.
2. Open `index.html` in **Chrome or Edge**, select **Open folder**, and pick this repo's folder.
3. Read, search (`Ctrl K`), and edit (`Ctrl E`). Edits save straight to the `.md` files.
4. **Commit and push** in GitHub Desktop when you finish a session.

The tool remembers the folder. After a browser restart it may ask you to select **Reconnect** once.

If a file changes on disk while it is open (a pull, or another editor), the tool notices. Saving over it asks whether to keep your version or load the disk version.

## Web version

The viewer is also published at <https://azjester.github.io/MD_files/>. It is the same `index.html`, so it works without a local copy of the tool. In Chrome or Edge, **Open folder** still edits the files in your local clone. Nothing is uploaded.

The browser keeps the remembered folder and any imported copies per address, so the web version and the local `index.html` each have their own.

The site carries only `index.html` and the font licenses. Notes are not published to it. A push to `main` that changes `index.html` redeploys the site.

## Writing notes

- Link to another note with a relative path: `[range notes](../notes/range.md)`. Links work in the tool and on GitHub.
- Link to a heading with `#`: `[setup](setup.md#install)`.
- Put images in `assets/` and reference them relatively: `![diagram](../assets/diagram.png)`.
- Front matter at the top of a note (`title:`, `tags:`) shows as a key/value block.
- Renaming or moving a note from inside the tool updates links that point to it.

## Other browsers

Firefox and Safari cannot write to local folders. Use **Import** there instead. It keeps a copy inside the browser. Bring edits back with **Export as ZIP** and copy the files over the repo folder.

## Visibility

Anything committed to a public repo is readable by anyone. Keep this repo private if the notes are personal.

Making the repo private takes the web version offline unless the account has a paid GitHub plan. On a paid plan the site stays public, which is fine because it never contains notes.
