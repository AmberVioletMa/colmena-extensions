# Colmena extensions: the approved list

`index.json` is the list of reviewed extensions that Colmena and Rooms offer with one click. Each entry is pinned to the
exact commit that was reviewed and to the hash of its files, so what was reviewed is exactly what gets installed.
The format of an extension and of this list: [EXTENSIONS.md](https://github.com/AmberVioletMa/colmena/blob/master/EXTENSIONS.md).

## Add yours

1. Make your extension in its own GitHub repository, with a `colmena-extension.json` at its root (parts: `service`,
   `pages`, `world`, `assets`; an assets pack says which world it is for).
2. Try it: anyone can install it from its link (Colmena: Settings → Extensions → Install from a link; it shows as
   "not reviewed").
3. Open a pull request here adding its entry to `index.json`: `id`, `name`, `description`, `repo`, `parts`, the
   `commit` to review and its `tree_sha256` (in a Colmena folder: `python -c "import extensions; print(extensions.tree_hash('path/to/your/extension'))"`
   on a clean copy of that commit, without `.git`).
4. Once reviewed and merged, it shows in everyone's Extensions. New versions: a pull request moving the commit and hash.
