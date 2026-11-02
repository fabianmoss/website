# AGENTS.md

Hugo site for Fabian C. Moss's academic website, built with Wowchemy Academic v5. Content lives in Markdown/YAML; there is no `package.json`, test suite, linter, or Node build step. `hugo` is the only build tool.

## Build and verify

```bash
./view.sh                                  # hugo server --disableFastRender --printI18nWarnings
hugo server                                # plain dev server
hugo --gc --minify                         # production build (CI runs `hugo mod tidy` first)
hugo --gc --minify --buildFuture           # include future-dated pages
hugo list future                           # show pages the default build excludes
hugo list drafts                           # show draft pages
```

- Use Hugo **extended** v0.120.0; CI pins that version and the theme needs extended/SCSS support.
- There are no tests or lint. Verify by running a full build and checking the affected page in `hugo server`; confirm no Hugo warnings, broken links, or missing images.
- `public/`, `resources/`, `jsconfig.json`, and `node_modules/` are gitignored build artifacts. Do not edit them.

## Deployment

- Push to `main` runs `.github/workflows/deploy.yml` and deploys to **GitHub Pages** with `hugo mod tidy && hugo --gc --minify`.
- The custom domain comes from `CNAME` (`fabian-moss.de`).
- There is no `netlify.toml`; despite Netlify mentions in `README.md` and `update_wowchemy.sh`, deployment is GitHub Pages.

## Configuration and theme

- Site config is YAML in `config/_default/` (`config.yaml`, `params.yaml`, `menus.yaml`, `languages.yaml`), not a root `hugo.toml`.
- Main navigation is in `config/_default/menus.yaml`. Homepage links use `#<widget filename>` (e.g. `#research-areas`); enabling/disabling a home widget usually means editing both its `content/home/*.md` front matter and `menus.yaml`.
- Wowchemy is pinned as Hugo modules in `go.mod` and the `theme:` list in `config.yaml` (both at `v5.0.0-20211231...`). `hugo mod get -u ./... && hugo mod tidy` (or `bash update_wowchemy.sh`) updates them; review the diff, since v5 is legacy and updates can change layouts.
- `themes/` is a tracked vendored copy. Do not edit it; put overrides in `layouts/` (currently only `layouts/shortcodes/list_by_tag.html`).
- Do not run `scripts/init_kickstart.sh`; it resets the site to the starter template.
- Do not add npm/Node tooling; this site is Hugo-only.

## Content model

- Homepage: `content/home/index.md` is a headless `widget_page`. Each section is a separate `content/home/*.md` widget with `active` and `weight`; some widgets are currently inactive (`featured`, `projects`, `posts`, `contact`, `tags`, etc.).
- The About section is filled from `content/authors/admin/_index.md`; `content/home/about.md` only selects `author: admin`.
- Publications: recent items use `content/publication/<year>/<slug>/index.md`; many older items are flat at `content/publication/<slug>/index.md`. Events use `content/event/<year>/<slug>/index.md`; projects use `content/project/<year>/<slug>/index.md`. Do not reorganize existing folders—the folder path is part of the URL.
- Event permalinks are `/talk/<slug>/` even though content lives under `content/event/` (see `permalinks` in `config.yaml`).
- Teaching is a single page, `content/teaching/index.md`. Semesters are `##` sections containing `<details><summary>` blocks, newest first.
- Research areas: `content/research/<area>/_index.md`. Sections are populated by `{{< list_by_tag tag="..." type="..." >}}`, which matches `tags` and `categories` case-insensitively and by substring (not exact match).
- The custom `list_by_tag` filters by Hugo content type. Use `type="event"` for events; the existing `type="talk"` blocks in research pages currently match nothing.
- Adding a research area also requires a hardcoded card and inline CSS in `content/home/research-areas.md`.
- Author id is `admin`: `content/authors/admin/_index.md` is the profile (`superuser: true`), and content uses `authors: [admin]`. `content/admin/index.md` is a separate Wowchemy CMS config page, not the author profile.
- `content/journal-club/index.md` is a standalone page; its menu entry is currently commented out.
- Page bundle images live next to `index.md` (use `featured.jpg`/`featured.png` for thumbnails). Global images/icons go in `assets/media/`; downloads such as the CV go in `static/uploads/`.

## Front matter conventions

- `date` is the displayed and sorted date; `publishDate` controls when Hugo publishes the page. Future-dated pages are excluded unless built with `--buildFuture`; `draft: true` excludes them entirely.
- Publication front matter uses `publication`, `publication_short`, `doi`, `abstract`, and `url_pdf`/`url_code`/`url_dataset`. `publication_types`: `0` uncategorized, `1` conference paper, `2` journal article, `3` preprint, `4` report, `5` book, `6` book section, `7` thesis, `8` patent.
- Events use `event`, `event_url`, `location`, `address` (`street`/`city`/`region`/`postcode`/`country`), `date`, `date_end`, and `all_day`.
- Section indexes: `content/publication/_index.md` uses `view: 4` (citation); `content/event/_index.md` and `content/post/_index.md` use `view: 2` (compact).
- `content/home/publications.md` sets `exclude_featured: true`, and the Featured widget is inactive. Marking content `featured: true` removes it from "Latest publications" without showing it elsewhere unless you activate that widget.
- Leave commented-out front-matter template fields in place; they document optional keys.

## Custom shortcode

`layouts/shortcodes/list_by_tag.html` is the only custom shortcode. It lists `.Site.RegularPages` of a type whose tags/categories contain the requested string, sorted by date descending.
