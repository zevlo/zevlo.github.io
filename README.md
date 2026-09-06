# My Blog

A personal blog about learning and building. Live at [zevlo.github.io](https://zevlo.github.io).

Built with [Jekyll](https://jekyllrb.com) and plain CSS.

## Run locally

```sh
jekyll serve
```

Then open http://127.0.0.1:4000.

## Structure

| Directory | Purpose |
| --- | --- |
| `_posts/` | Blog posts |
| `_thoughts/` | Short quotes and one-line thoughts |
| `_projects/` | Project pages |
| `_drafts/` | Unpublished content (not built) |
| `_layouts/` | HTML layouts |

## Adding content

Create a markdown file named `YYYY-MM-DD-slug.md` in the relevant collection directory. Minimal frontmatter:

```yaml
---
date: 2025-11-21
---
```

Layouts are applied automatically via `_config.yml` defaults.

## Deployment

Push to `main` — GitHub Pages builds and deploys automatically.
