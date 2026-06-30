# AGENTS.md - Guidelines for Agentic Coding in This Repository

This repository is a Hugo-based academic website (Wowchemy Academic Theme v5) for Fabian C. Moss's personal academic website. The site is deployed via Netlify and built using Hugo. There are **no automated tests, no linter, and no package.json** in this project.

## Build Commands

### Local Development
```bash
hugo server                              # Live reload at http://localhost:1313
hugo server --disableFastRender           # Faster startup, no live reload
```

### Production Build
```bash
hugo --gc --minify                        # Full production build
hugo --gc --minify --buildFuture          # Include future-dated content
```

### Deployment (Netlify)
Auto-deploys on push to `main`. Build command: `hugo --gc --minify -b $URL`

### Updating Hugo Modules
```bash
hugo mod get -u ./... && hugo mod tidy    # Update Wowchemy to latest
bash ./update_wowchemy.sh                 # Or use the provided script
```

### Validation (No Formal Linting)
```bash
hugo config                               # Validate Hugo configuration
hugo --verbose                            # Verbose build output for debugging
```
- Validate YAML/TOML syntax (no tabs, proper indentation)
- Check for broken links with external tools like `lychee`

### Testing
No automated tests. Manual testing only:
1. `hugo server` and visually verify the site
2. Check for Hugo warnings in output
3. Verify links work (DOIs, external links)
4. Confirm featured images and media display

## Code Style Guidelines

### General Principles
- This is a **content-driven website**, not a software project
- Most changes involve Markdown content or YAML/TOML configuration
- Avoid introducing custom JavaScript or complex build steps
- No custom CSS should be added unless absolutely necessary

### Editor Configuration
The project uses `.editorconfig`:
- **Charset**: UTF-8
- **Line endings**: LF (Unix)
- **Indentation**: 2 spaces (no tabs)
- **Final newline**: Yes (except `layouts/shortcodes/*.html`)
- **TOML files**: Max line length 100
- **Markdown files**: Do not trim trailing whitespace

### File Organization
```
content/
├── authors/         # Author profiles (one folder per author ID)
├── event/           # Talks and events
├── home/            # Homepage widgets
├── post/            # Blog posts
├── project/         # Research projects
├── publication/    # Academic publications
├── research/       # Research areas (_index.md per area)
├── slides/         # Presentation slides
└── teaching/       # Teaching materials (single index.md)

assets/
└── media/          # Images, icons, media files
  ├── icons/brands/ # Institution logos (SVG)
  └── albums/       # Photo albums

static/
└── uploads/        # Files for download (e.g., CV PDF)

layouts/
└── shortcodes/     # Custom Hugo shortcodes
```

### Content Directory Conventions
- **Publications, events, projects** use year-based subdirectories: `content/publication/2026/title/index.md`
- **Year subdirectories** should be 4 digits (e.g., `2026`, `2025`, `2024`)
- **Teaching** uses a single `content/teaching/index.md` with `<details><summary>` HTML blocks per semester
- **Research areas** go in `content/research/<area>/_index.md`

### Naming Conventions
- **Folders**: kebab-case (e.g., `content/post/my-new-post/`)
- **Images**: descriptive names in the same folder as content
- **Authors**: Define in `content/authors/admin/` — `admin` is the site owner's ID
- **Year prefixes**: Front matter `date` uses ISO 8601 format

### Front Matter Conventions (Ordered by Importance)
```yaml
title: "Page Title"
subtitle: "Optional subtitle"           # post only
summary: "Short description"
authors: [admin]                         # array of author IDs
date: 2024-01-26T00:00:00Z               # ISO 8601
lastmod: 2024-01-26T00:00:00Z            # optional, post only
publishDate: 2024-01-26T00:00:00Z        # for scheduled content
draft: false                             # true hides from production
featured: false                          # show in Featured widget
tags: [tag1, tag2]
categories: []
projects: []
```

### Publications (`content/publication/*/index.md`)
- `publication_types: ["2"]` — legend: 0=Uncategorized, 1=Conf paper, 2=Journal, 3=Preprint, 4=Report, 5=Book, 6=Book section, 7=Thesis, 8=Patent
- `publication`, `publication_short`, `doi`, `abstract`, `url_pdf`, `url_code`, `url_dataset`

### Events (`content/event/*/index.md`)
- `event`, `event_url`, `location`, `address` (street/city/region/postcode/country)
- `date`, `date_end`, `all_day: true`

### Section index pages (`content/event/_index.md`, `content/publication/_index.md`)
- `cms_exclude: true`, `view: 2` (1=List, 2=Compact, 3=Card, 4=Citation)

### Hugo Shortcodes
- **Built-in**: `{{< figure src="image.png" title="Caption" >}}`, `{{< gist user id >}}`
- **Custom** (`layouts/shortcodes/`): `{{< list_by_tag tag="topic" type="publication" >}}` lists content by tag
- LaTeX math: `$...$` (inline), `$$...$$` (display) — enabled via `math: true` in params

### Markdown Content Rules
- Each content item gets its own folder with `index.md`
- Featured image: `featured.jpg` or `featured.png` in the content folder
- Use standard Markdown; raw HTML (`<details>`, `<summary>`, `<a>`) is accepted in Markdown
- Citations use Hugo-style `{{< cite >}}` or plain Markdown links
- Links to internal pages use relative paths: `teaching/`, `../publication/...`

### Images and Media
- Content-specific images go in the same folder as `index.md`
- Global media (logos, icons) go in `assets/media/`
- Downloadable files (CV PDF) go in `static/uploads/`
- Use SVG for logos/icons; JPEG or PNG for photographs

### Error Handling
- Always validate YAML syntax (no tabs, consistent indentation of 2 spaces)
- Test changes locally with `hugo server` before deploying
- Check Hugo output for warnings about missing fields or invalid config
- Strings with special characters (`@`, `:`, `#`) must be quoted in YAML

### What NOT to Do
- Do not modify `go.mod` or `theme.toml` unless upgrading Hugo/Wowchemy
- Do not add JavaScript frameworks, npm packages, or build tools
- Do not change the Wowchemy theme structure (under `themes/`)
- Do not commit large binary files; use Git LFS or external hosting
- Do not set `draft: true` on content intended for publication
- Do not delete commented-out front matter fields — they serve as documentation

## Useful Resources
- Hugo Docs: https://gohugo.io/documentation/
- Wowchemy Docs: https://wowchemy.com/docs/
- Wowchemy Widgets: https://wowchemy.com/docs/page-builder/
- Markdown Writing: https://wowchemy.com/docs/content/writing-markdown-latex/
