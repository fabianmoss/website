# AGENTS.md

Hugo site for Fabian C. Moss's academic website, built with Wowchemy Academic v5. Content lives in Markdown/YAML; there is no `package.json`, test suite, linter, or Node build step. `hugo` is the only build tool.

## Build and verify

```bash
./view.sh                                  # hugo server --disableFastRender --printI18nWarnings
hugo server                                # plain dev server
hugo --renderToMemory --quiet              # quick validation without touching public/
hugo --gc --minify                         # production build (CI runs `hugo mod tidy` first)
hugo --gc --minify --buildFuture           # include future-dated pages
hugo list future                           # show pages the default build excludes
hugo list drafts                           # show draft pages
```

- Use Hugo **extended** v0.120.0; CI pins that version and the theme needs extended/SCSS support.
- There are no tests or lint. Verify by running a full build and checking the affected page in `hugo server`; confirm no Hugo warnings, broken links, or missing images.
- `public/`, `resources/`, `jsconfig.json`, and `node_modules/` are gitignored build artifacts. Do not edit them.
- The dev server occasionally goes stale after many content edits (`Hugo cannot find a Widget Page at /home/index.md`). Restart it rather than debugging the content.

## Deployment

- Push to `main` runs `.github/workflows/deploy.yml` and deploys to **GitHub Pages** with `hugo mod tidy && hugo --gc --minify`.
- The custom domain comes from `CNAME` (`fabian-moss.de`).
- There is no `netlify.toml`; despite Netlify mentions in `README.md` and `update_wowchemy.sh`, deployment is GitHub Pages.

## Configuration and theme

- Site config is YAML in `config/_default/` (`config.yaml`, `params.yaml`, `menus.yaml`, `languages.yaml`), not a root `hugo.toml`.
- Main navigation is in `config/_default/menus.yaml`. Homepage links use `#<widget filename>` (e.g. `#research-areas`).
- Wowchemy is pinned as Hugo modules in `go.mod` and the `theme:` list in `config.yaml` (both at `v5.0.0-20211231...`). `hugo mod get -u ./... && hugo mod tidy` (or `bash update_wowchemy.sh`) updates them; review the diff, since v5 is legacy and updates can change layouts.
- `themes/` is a tracked vendored copy. **Do not edit it.** Overrides belong in `layouts/` (see the inventory below).
- Do not run `scripts/init_kickstart.sh`; it resets the site to the starter template.
- Do not add npm/Node tooling; this site is Hugo-only.
- Dark mode is enabled (`day_night: true`). `layouts/partials/hooks/footer.html` replaces the theme dropdown with a single sun/moon toggle while keeping Wowchemy’s storage/highlighting handlers.
- `profile: false` in `params.yaml` hides the author box on content pages (single-author site).

## Design system

- `assets/scss/custom.scss` holds all site-level styling; it is imported last by the theme. It is organised in numbered sections: tokens, typography, links, research cards, navbar, hero, videos, publications, footer, teaching, talks, vertical rhythm, experience, research pages, project pages, motion.
- Design tokens are CSS variables (`--fc-*`) for colour, spacing, radius, shadow and accent. Prefer them over hard-coded values. A dark palette is keyed to `body.dark`.
- Typography: **H1 and H2 are serif** (Source Serif Pro); H3–H6 and body text are Inter. Fonts are self-hosted (see below) and declared with `@font-face` at the top of `custom.scss`.
- Colour and accessibility: text pairs meet WCAG AA in both themes; prose links are underlined as well as accent-coloured; role colours (professor/postdoc/doctoral) differ in lightness as well as hue, and research-area colours are always paired with labels and icons, so colour is never the only cue. `prefers-contrast: more` strengthens muted text and borders.
- The homepage has a **single H1** (the hero name). Section titles are H2 via `layouts/partials/widget_page.html`; keep that invariant when changing headings.

## Homepage composition

`content/home/index.md` is a headless `widget_page`. Active widgets, in order:

| Weight | File | What it is |
|---|---|---|
| 1 | `about.md` | Hero (author `admin`) |
| 2 | `research-areas.md` | `{{< research_areas >}}` |
| 3 | `experience.md` | Experience lanes + education |
| 4 | `videos.md` | `{{< video_grid >}}` |

Inactive widgets: `publications`, `talks`, `projects`, `posts`, `featured`, `skills`, `accomplishments`, `contact`, `tags`. Publications and talks are browsed through the research areas; the complete archives still exist at `/publication/` and `/event/` but are not in the main menu.

## Content model

- Publications: recent items use `content/publication/<year>/<slug>/index.md`; many older items are flat at `content/publication/<slug>/index.md`. Events use `content/event/<year>/<slug>/index.md`; projects use `content/project/<year>/<slug>/index.md`. Do not reorganise existing folders — the folder path is part of the URL.
- Event permalinks are `/talk/<slug>/` even though content lives under `content/event/` (see `permalinks` in `config.yaml`).
- Teaching is a single page, `content/teaching/index.md`. Semesters are `##` sections containing `<details><summary>` blocks, newest first. `{{< teaching_timeline >}}` builds the year selector; it defaults to the newest year and has no “All” node.
- Research areas live in `content/research/<area>/_index.md` and are driven by `data/research_areas.yaml`. The homepage and `/research/` both render `{{< research_areas >}}`, which builds cards (image, icon, counts, Explore link) from that data file.
- `content/research/_index.md` + `layouts/research/list.html` render the research landing page; `content/project/_index.md` renders the projects index.
- Author id is `admin`: `content/authors/admin/_index.md` is the profile (`superuser: true`), and content uses `authors: [admin]`. `content/admin/index.md` is a separate Wowchemy CMS config page, not the author profile.
- `content/journal-club/index.md` is a standalone page; its menu entry is commented out.
- Drafts currently kept: `content/post/babysteps-google-cloud`, `content/post/new-position-wue`. `privacy.md` and `terms.md` were removed; do not reintroduce placeholder legal pages.

## Custom shortcodes and partials

Shortcodes (`layouts/shortcodes/`):

- `publications_list.html` — publications list, year timeline, five-per-year cap, type/accepted labels, venue links to DOI/PDF. Optional `tag=` filters by research area and `heading=` adds a section title; used on the homepage and inside research areas.
- `talks_list.html` — talks list, year timeline, date badge, speakers, attachment pills. Same optional `tag=` / `heading=` parameters as `publications_list`.
- `research_areas.html` — research cards from `data/research_areas.yaml`, including live counts.
- `research_intro.html` — intro text block for research-area pages (no figure; figures live on the project cards and homepage research cards).
- `video_grid.html` — click-to-play video cards from `data/videos.yaml`; embeds YouTube only on click.
- `teaching_timeline.html` — year selector for the teaching page.
- `list_by_tag.html` — project cards for a research area; matches `tags`/`categories` case-insensitively by substring. Supports `type=` (default `project`) and `heading=`.

Partials / templates (`layouts/`):

- `partials/widget_page.html` — section titles as H2.
- `partials/widgets/about.html` — hero name as H1; optional widget title as H2.
- `partials/widgets/experience.html` — institution lanes on a shared year axis, one bar per role with the role name in the column beside it, plus a compact Education block. Reads `positions:` (`institution`, `company_logo`, `company_url`, `location`, `roles` with `title`/`date_start`/`date_end`, optional `type` (`professor`/`postdoc`/`doctoral`, drives the bar colour) and per-role `markers`) and `education:` from `content/home/experience.md`; the chart scrolls horizontally on mobile.
- `partials/site_footer.html` — brand, social, legal/credit row; no duplicate menu.
- `partials/search.html` — search heading as H2.
- `partials/hooks/footer.html` — sun/moon theme toggle.
- `partials/functions/filter_by_tag.html` — shared tag/category matching for research lists, card counts and the filtered widgets.
- `partials/functions/count_by_tag.html` — counts for research cards.
- `partials/functions/publication_type.html` — numeric type → icon/label, with `publication_type_label`/`publication_type_icon` overrides.
- `research/list.html` — research landing page.

If Wowchemy is updated, re-check these overrides against the new theme partials.

## Data files

- `data/research_areas.yaml` — research-area cards: `key`, `title`, `description`, `icon`, `image`, `url`. Images are figures from Fabian’s own publications/projects, stored in `assets/media/research/`.
- `data/videos.yaml` — homepage videos: `youtube_id`, `title`, `short_title`, optional `source`, optional `thumbnail`.
- `data/fonts/modern.toml` — font set (`google_fonts = ""` because fonts are self-hosted).

## Images, fonts, assets

- Research figures live in `assets/media/research/<area>.jpg`; shortcodes resize them to WebP (640 px cards, 900 px intro). Prefer this over linking raw images.
- Page bundle images live next to `index.md` (`featured.jpg`/`featured.png` for listings).
- Brand logos/icons: `assets/media/icons/brands/`. Global images: `assets/media/`.
- Self-hosted fonts: `static/fonts/` (`inter-var.woff2`, `source-serif-pro-{400,600,700}.woff2`), declared in `custom.scss`. Do not reintroduce Google Fonts links.
- Downloads such as the CV go in `static/uploads/`.

## Front matter conventions

- `date` is the displayed and sorted date; `publishDate` controls publication. Future-dated pages are excluded unless built with `--buildFuture`; `draft: true` excludes them entirely.
- **DOIs must be stored as bare DOIs** (e.g. `10.1234/abc`), never full URLs — the theme prepends `https://doi.org/`. Publication cards link the venue to the DOI (or `url_pdf` if no DOI).
- `publication_types` is numeric: `0` uncategorized/publication, `1` conference paper, `2` journal article, `3` preprint, `4` report, `5` book, `6` book chapter, `7` thesis, `8` patent. Keep the numeric value for Wowchemy, then optionally add `publication_type_label` and `publication_type_icon` for custom labels (datasets, blog posts, book reviews).
- `accepted: true` marks accepted/in-press publications; the cards show an “Accepted” chip and the venue should not contain “(accepted)”.
- Keep `publication` venue strings plain text (no Markdown emphasis); the card styles them italic. Use `publication_short` for abbreviations.
- Events use `event`, `event_url`, `location`, `address` (`street`/`city`/`region`/`postcode`/`country`), `date`, `date_end`, and `all_day`.
- Section indexes: `content/publication/_index.md` uses `view: 4` (citation); `content/event/_index.md` and `content/post/_index.md` use `view: 2` (compact).
- Leave commented-out front-matter template fields in place; they document optional keys.

## Adding or changing a research area

1. Add an entry to `data/research_areas.yaml` (`key`, `title`, `description`, `icon`, `image`, `url`).
2. Add `content/research/<key>/_index.md` with the intro paragraph wrapped in `{{< research_intro name="<key>" >}}…{{< /research_intro >}}`, then `Projects` via `{{< list_by_tag tag="<key>" type="project" heading="Projects" >}}` and `Publications` / `Talks` via `{{< publications_list tag="<key>" heading="Publications" >}}` / `{{< talks_list tag="<key>" heading="Talks" >}}`. Empty sections hide themselves.
3. Add an image at `assets/media/research/<key>.jpg` — used by the homepage research card, not by the research-area page.
4. Counts and homepage cards update automatically; do not hard-code cards in `research-areas.md`.
5. Every publication and talk must carry at least one research-area tag (`computational musicology`, `music theory`, `digital humanities`, `cultural evolution`); the research areas are the only browse path now that the homepage lists and menu entries are gone.
