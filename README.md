# muzeeb-shaik.github.io

Personal academic website for Muzeeb Shaik (Kelley School of Business, Indiana University). GitHub Pages **user site**, served from the `master` branch at https://muzeeb-shaik.github.io/.

## Publishing a presentation to `/presentations/`

Each talk lives in its own folder under `presentations/`, served at `https://muzeeb-shaik.github.io/presentations/<slug>/`. Follow this convention for every new deck:

1. Render the Quarto deck to a **self-contained** HTML (`self-contained: true`, images embedded). This is the preferred format: one file, nothing to break.
2. Create `presentations/<slug>/`.
3. Copy the rendered deck in as `index.html` so it opens at the folder URL.
4. Also drop the **source `.qmd`** into the same folder (source-alongside convention, matching `tamu-storytelling/` and `isms-2026/`).
   - If a deck is NOT self-contained, also copy its `<deck>_files/` assets folder, `images/`, and any `.scss` it references; otherwise the slides will not render.
5. Add a card to `presentations/index.html`, at the **top** of `.talk-list` (most recent first). Each card needs: `.talk-meta` (venue + date), an `<h2>` title linking to `<slug>/`, a `.coauthors` line, an optional `.description`, and a `.talk-actions` "Open slides" link.
6. Commit and push to `master`. GitHub Pages rebuilds in roughly one to two minutes.

### Current decks

| Slug | Talk | Format |
|------|------|--------|
| `isms-2026/` | Experiential Learning & Gender Stereotypes (ISMS Marketing Science Conference 2026) | self-contained `index.html` + source `.qmd` |
| `experiential-learning-muzeeb/` | Experiential Learning & Gender Stereotypes (IU Brown Bag) | `index.html` + `_files/` + `images/` |
| `tamu-storytelling/` | Writing a Paper Is Telling a Story (Texas A&M) | `index.html` + `_files/` + `images/` + source `.qmd` + `.scss` |
