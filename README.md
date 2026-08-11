# Personal site

Static site — three files, no build step, no dependencies.

```
index.html
style.css
favicon.svg
```

## Put it on GitHub Pages

1. Create a repo named `aschleigh.github.io` (use your actual GitHub username — that name is what
   gets you the root URL instead of a subpath).
2. Drop `index.html`, `style.css`, and `favicon.svg` in the root of the repo and push.
3. Repo → **Settings** → **Pages** → Source: **Deploy from a branch**, Branch: `main`, folder `/ (root)`.
4. Wait a minute. It'll be live at `https://aschleigh.github.io`.

From the command line:

```bash
git init
git add .
git commit -m "Site"
git branch -M main
git remote add origin https://github.com/aschleigh/aschleigh.github.io.git
git push -u origin main
```

If you'd rather use a normal repo name (e.g. `site`), everything works the same but the URL
becomes `https://aschleigh.github.io/site/`.

## Before you push — replace these

In `index.html`:

- `aschleigh` in every GitHub and LinkedIn URL
- `you@example.com`
- The two `href="#"` placeholders (Tractor escape room, music ML notes)
- Anything in the copy that isn't how you'd actually describe yourself

## How it's put together

- **Palette** comes from mule coloring: grulla (mouse-gray), a mealy oat background, a near-black
  dorsal-stripe ink, and brass for tack. Defined as CSS variables at the top of `style.css`.
- **Type** is Saira Condensed for display and Source Serif 4 for body — condensed sans over serif,
  the inverse of the usual arrangement.
- **The trail** down the left edge is a switchback path. The mule walks it as you scroll and turns
  around at each corner. It's hidden below 900px and stays put if the reader has reduced motion on.
- **Margin notes** are the mule facts. Below 1180px they collapse inline above each section.

## Local preview

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.
