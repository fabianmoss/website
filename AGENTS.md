# AGENTS.md - Guidelines for Agentic Coding in This Repository

This repository is a Hugo-based academic website (Wowchemy Academic Theme) for Fabian C. Moss's personal academic website. The site is deployed via Netlify and built using Hugo.

## Build Commands

### Local Development
```bash
# Start local Hugo server with live reload
hugo server

# Start local server (faster, no live reload)
hugo server --disableFastRender

# View at http://localhost:1313
```

### Production Build
```bash
# Full production build (minify, garbage collection)
hugo --gc --minify

# Build with future-dated content
hugo --gc --minify --buildFuture
```

### Deployment (Netlify)
The site auto-deploys on push to main. Build command:
```bash
hugo --gc --minify -b $URL
```

### Updating Hugo Modules
```bash
# Update Wowchemy to latest version
hugo mod get -u ./...
hugo mod tidy
```

Or use the provided script:
```bash
bash ./update_wowchemy.sh
```

### Linting/Validation
There is no formal linting for this project. However, you can:
- Validate Hugo configuration: `hugo config`
- Check for broken links: External tools like `lychee` or online YAML syntax in validators
- Verify config files

### Testing
There are no automated tests in this project. Manual testing involves:
1. Running `hugo server` and visually verifying the site
2. Checking that all pages render correctly
3. Verifying that links work

## Code Style Guidelines

### General Principles
- This is primarily a **content-driven website**, not a software project
- Most changes involve Markdown content, YAML front matter, or TOML/YAML configuration
- Avoid introducing custom JavaScript or complex build steps unless absolutely necessary

### Editor Configuration
The project uses `.editorconfig` with these settings:
- **Charset**: UTF-8
- **Line endings**: LF (Unix)
- **Indentation**: 2 spaces (no tabs)
- **Final newline**: Yes (except shortcode HTML files)
- **TOML files**: Max line length 100
- **Markdown files**: Do not trim trailing whitespace

### YAML Configuration (config/_default/)
```yaml
# Example front matter pattern
title: "Page Title"
subtitle: "Optional subtitle"
summary: "Summary for listings and search engines"
date: "2024-01-26T00:00:00Z"
lastmod: "2024-01-26T00:00:00Z"
draft: false
featured: false
authors:
  - admin
projects: []
tags: []
categories: []
```

### Markdown Content Files
- Place in appropriate `content/` subdirectory (post, publication, project, event, slides, teaching)
- Each piece of content gets its own folder with `index.md`
- Use standard Markdown syntax
- LaTeX math is supported via `$...$` (inline) or `$$...$$` (display)
- Hugo shortcodes available: `{{< shortcode >}}`

### Naming Conventions
- **Folders**: Use kebab-case (e.g., `content/post/my-new-post/`)
- **Images**: Use descriptive names, place in the same folder as content
- **Authors**: Define in `content/authors/` with folder named after author ID

### File Organization
```
content/
├── authors/         # Author profiles
├── event/           # Talks and events
├── home/            # Homepage widgets
├── post/            # Blog posts
├── project/         # Research projects
├── publication/    # Academic publications
├── slides/         # Presentation slides
└── teaching/       # Teaching materials
```

### Front Matter Fields
Common fields for content:
- `title` (required): Page title
- `subtitle`: Optional subtitle
- `summary`: Description for search engines/listings
- `date`: Publication date (ISO 8601 format)
- `lastmod`: Last modification date
- `draft`: Set to `true` to hide from production
- `featured`: Show in Featured widget
- `authors`: List of author folder names
- `projects`: Associated projects
- `tags` / `categories`: Taxonomy terms

### Configuration Files
- `config/_default/config.yaml`: Main Hugo configuration
- `config/_default/menus.yaml`: Navigation menus
- `config/_default/params.yaml`: Theme parameters
- `config/_default/languages.yaml`: Language settings

### Error Handling
- Always validate YAML/TOML syntax (no tabs, proper indentation)
- Test changes locally with `hugo server` before deploying
- Check Hugo output for warnings about missing fields or invalid config

### What NOT to Do
- Do not modify go.mod unless upgrading Hugo version is required
- Do not add complex JavaScript frameworks
- Do not change the theme structure without good reason
- Do not commit large binary files (use Git LFS or external hosting)
- Do not set `draft: true` for content that should be published

## Content Types Reference

### Publications
Located in `content/publication/`. Front matter includes:
- `publication_types`: Array (e.g., `[1]` for journal article)
- `doi`, `url`, `arxiv`, `pdf`, `code` links

### Projects
Located in `content/project/`. Front matter includes:
- `external_link`: External project URL

### Events
Located in `content/event/`. Front matter includes:
- `event`: Event name
- `event_url`: Event website

## Useful Resources
- Hugo Docs: https://gohugo.io/documentation/
- Wowchemy Docs: https://wowchemy.com/docs/
- Wowchemy Widgets: https://wowchemy.com/docs/page-builder/
- Markdown Writing: https://wowchemy.com/docs/content/writing-markdown-latex/
