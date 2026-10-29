# github_homepage — preview instructions

Static personal homepage for GitHub Pages (`https://<username>.github.io/`).
No framework, no build step, no dependencies: plain HTML + CSS + a few lines of vanilla JS.

## Files

```
github_homepage/
├── index.html   # entire page content (must stay at repo root)
├── style.css    # all styling, responsive, dark theme
└── README.md    # this file
```

There is no `package.json` and no lockfile because nothing is installed or compiled.

## Preview it locally

**Option A — just open the file (works offline):**

- Windows: double-click `index.html`, or run
  `Start-Process .\index.html` in PowerShell from this folder.
- macOS: `open index.html`
- Linux: `xdg-open index.html`

**Option B — serve it like GitHub Pages does (recommended):**

```bash
# Python 3 (already on most machines)
python -m http.server 8000
# then open http://localhost:8000/
```

```bash
# or with Node.js
npx serve .
```

Stop the server with `Ctrl+C`. Opening `index.html` and serving it give the same result here,
because all paths are relative and no cookies/storage are used.

## Publish on GitHub Pages

1. Create a **public** repository named exactly `<username>.github.io`.
2. Put `index.html`, `style.css` (and optionally this README) in the repository **root**.
3. Push to the `main` branch.
4. Repository → **Settings → Pages** → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)` → **Save**.
5. Wait 1–2 minutes, then open `https://<username>.github.io/`.

## Editing the content

- Name / headline: the `.hero` block in `index.html`.
- Sections: `#about`, `#now`, `#work`, `#contact` in `index.html`.
- GitHub link: replace `https://github.com/keqianniu` with your real profile URL.
- Colours and spacing: the `:root` custom properties at the top of `style.css`.

Keep student ID, home address, phone number, email address and any private homework out of this
public repository.
