# CLAUDE.md - AI Assistant Guide for zevlo.github.io

## Project Overview

This is a **Jekyll-based personal blog and portfolio** hosted on GitHub Pages. The site showcases blog posts, projects, and thoughts with a clean, minimalist design using a warm beige color scheme.

**Live URL**: https://zevlo.github.io
**Platform**: GitHub Pages + Jekyll
**Hosting**: GitHub Pages (automatic deployment on push to main branch)

## Project Type & Technology Stack

- **Static Site Generator**: Jekyll (GitHub Pages compatible)
- **Templating Language**: Liquid (Jekyll templates)
- **Content Format**: Markdown with YAML frontmatter
- **Styling**: Pure CSS (no frameworks)
- **Deployment**: Automatic via GitHub Pages (1-2 minute build time)

## Repository Structure

```
zevlo.github.io/
├── _config.yml              # Jekyll configuration (site metadata, collections)
├── _layouts/
│   ├── default.html         # Base layout with header, nav, and footer
│   └── post.html            # Post/project/thought layout (extends default)
├── _posts/                  # Blog posts (Markdown files)
│   └── YYYY-MM-DD-title.md  # Naming convention: date prefix required
├── _projects/               # Project portfolio items (Markdown files)
│   └── project-name.md      # Naming: no date prefix required
├── _thoughts/               # Short thoughts/reflections (Markdown files)
│   └── YYYY-MM-DD-title.md  # Naming convention: date prefix required
├── index.html               # Home page (Liquid template)
├── posts.html               # Lists all posts from _posts collection
├── projects.html            # Lists all projects from _projects collection
├── thoughts.html            # Lists all thoughts from _thoughts collection
├── style.css                # Global styles (warm beige theme)
├── README.md                # User-facing README
├── HOWTO.md                 # Comprehensive user guide for writing content
└── CLAUDE.md                # This file (AI assistant guide)
```

## Content Collections

The site uses three Jekyll collections defined in `_config.yml`:

### 1. Posts (`_posts/`)
- **Purpose**: Long-form blog posts
- **Filename Format**: `YYYY-MM-DD-title-slug.md` (date prefix REQUIRED)
- **Permalink**: `/posts/:title/`
- **Required Frontmatter**:
  ```yaml
  ---
  layout: post
  title: "Your Post Title"
  date: YYYY-MM-DD
  ---
  ```

### 2. Projects (`_projects/`)
- **Purpose**: Portfolio/project showcase
- **Filename Format**: `project-name.md` (no date prefix)
- **Permalink**: `/projects/:title/`
- **Required Frontmatter**:
  ```yaml
  ---
  layout: post
  title: "Project Name"
  date: YYYY-MM-DD
  description: "Short description"  # Optional but recommended
  github_url: "https://github.com/..." # Optional
  demo_url: "https://..."              # Optional
  ---
  ```

### 3. Thoughts (`_thoughts/`)
- **Purpose**: Short reflections, observations, quick thoughts
- **Filename Format**: `YYYY-MM-DD-title.md` (date prefix REQUIRED)
- **Permalink**: `/thoughts/:title/`
- **Required Frontmatter**:
  ```yaml
  ---
  date: YYYY-MM-DD
  ---
  ```
  (Note: No `layout` or `title` field needed, more minimal than posts)

## Key Files & Their Purposes

### Configuration
- **`_config.yml`**: Jekyll configuration
  - Site title: "Zachary's Blog"
  - Defines collections (posts, projects, thoughts)
  - Markdown processor: kramdown with GFM (GitHub Flavored Markdown)
  - Syntax highlighter: rouge

### Layouts
- **`_layouts/default.html`**: Base layout (lines 1-24)
  - Contains `<header>` with site title and navigation
  - Navigation links: Home, Posts, Projects, Thoughts
  - Active state highlighting based on current page URL
  - Renders `{{ content }}` in `<main>` tag

- **`_layouts/post.html`**: Content layout (lines 1-9)
  - Extends `default` layout
  - Displays post title (`page.title`)
  - Shows formatted date (`page.date`)
  - Renders markdown content

### Content Pages
- **`index.html`**: Home page
  - Personal introduction section (`.intro`)
  - Social links (GitHub, LinkedIn)

- **`posts.html`**: Auto-generated list of blog posts
  - Iterates through `site.posts` collection
  - Displays date and title in grid layout

- **`projects.html`**: Auto-generated list of projects
  - Iterates through `site.projects` collection
  - Shows title, description, GitHub/demo links

- **`thoughts.html`**: Auto-generated list of thoughts
  - Iterates through `site.thoughts` collection
  - Displays date and content inline

### Styling
- **`style.css`**: Complete site styles (lines 1-261)
  - Color scheme: Warm beige (#ffedd4 background, #2b2b2b text)
  - Typography: Georgia serif for body, Courier New for post titles
  - Responsive design (mobile breakpoint at 768px)
  - Max content width: 55% on desktop, 95% on mobile

## Development Workflow

### Adding New Content

**When creating blog posts:**
1. Create file in `_posts/` with format: `YYYY-MM-DD-title-slug.md`
2. Add required frontmatter (layout, title, date)
3. Write content in Markdown below frontmatter
4. Commit and push to main branch
5. GitHub Pages rebuilds automatically (1-2 minutes)

**When creating projects:**
1. Create file in `_projects/` with format: `project-name.md`
2. Add required frontmatter (include description, github_url, demo_url if applicable)
3. Write project documentation in Markdown
4. Commit and push

**When creating thoughts:**
1. Create file in `_thoughts/` with format: `YYYY-MM-DD-title.md`
2. Add minimal frontmatter (just date)
3. Write brief thought content
4. Commit and push

### Git Workflow
- **Main branch**: Production (auto-deploys to GitHub Pages)
- **Feature branches**: Use `claude/` prefix for AI-assisted development
- **Commit messages**: Descriptive (e.g., "Add new post: Understanding React Hooks")

### Build & Deployment
- GitHub Pages builds automatically on push to main
- Build time: ~1-2 minutes
- No local build required (but can run `bundle exec jekyll serve` locally)
- Check build status in GitHub Actions tab if issues occur

## Coding Conventions & Best Practices

### Markdown Standards
- Use GitHub Flavored Markdown (GFM)
- Code blocks: Use triple backticks with language identifier
- Headers: Use `##` for main sections (not `#`, reserved for page title)
- Links: Use reference style for readability when many links present
- Images: Include descriptive alt text

### Frontmatter Rules
- **YAML format**: Must be enclosed in `---` delimiters
- **Indentation**: Use spaces, NOT tabs
- **Dates**: Format as `YYYY-MM-DD` (ISO 8601)
- **Quotes**: Use double quotes for strings with special characters

### File Naming
- **Posts & Thoughts**: MUST start with `YYYY-MM-DD-`
- **Projects**: Use lowercase with hyphens (e.g., `my-awesome-app.md`)
- **Avoid**: Spaces, special characters, uppercase in filenames

### CSS Conventions
- Class naming: Use hyphen-separated lowercase (e.g., `.post-item`)
- Organization: Grouped by component/section
- Responsive: Mobile-first approach with `@media` queries
- Colors: Use existing palette (defined in style.css:8-11)

## Common Tasks for AI Assistants

### Creating a New Blog Post
```bash
# 1. Create the file
# File: _posts/2025-11-14-my-new-post.md

# 2. Add frontmatter and content:
---
layout: post
title: "My New Post Title"
date: 2025-11-14
---

Your markdown content here...
```

### Creating a New Project
```bash
# File: _projects/my-project.md
---
layout: post
title: "My Project"
date: 2025-11-14
description: "A cool project I built"
github_url: "https://github.com/zevlo/my-project"
---

## About
Project details here...
```

### Modifying Styles
- Edit `style.css` directly
- Maintain existing color scheme unless explicitly requested
- Test responsive behavior (check mobile breakpoint at 768px)
- Keep specificity low (avoid over-nested selectors)

### Troubleshooting Build Issues

**Post not appearing?**
- Verify filename format: `YYYY-MM-DD-title.md`
- Check frontmatter has required fields
- Ensure date is not in the future
- Verify YAML syntax (no tabs, proper spacing)

**Formatting broken?**
- Check frontmatter delimiters (`---`)
- Validate YAML syntax
- Look for unclosed HTML tags in markdown

**Changes not visible?**
- Wait 1-2 minutes for GitHub Pages rebuild
- Check GitHub Actions for build errors
- Clear browser cache
- Verify changes were pushed to main branch

## Important Constraints & Limitations

### What NOT to Do
1. **Don't modify** `_config.yml` without explicit request (breaks site)
2. **Don't add** build dependencies or Gemfile (GitHub Pages constraints)
3. **Don't use** Jekyll plugins not supported by GitHub Pages
4. **Don't create** HTML files for content (use Markdown + frontmatter)
5. **Don't change** color scheme without explicit approval
6. **Don't add** JavaScript unless specifically requested (currently no JS)

### GitHub Pages Limitations
- Limited to supported Jekyll plugins
- No server-side processing
- Build timeout: ~10 minutes
- Repository size limit: 1GB recommended
- Bandwidth: Soft limit of 100GB/month

## Testing & Validation

### Before Committing
1. Verify frontmatter syntax (YAML linter)
2. Check markdown rendering (preview tool)
3. Validate filename format matches collection requirements
4. Ensure dates are in correct format (YYYY-MM-DD)
5. Review for spelling/grammar

### After Pushing
1. Wait for GitHub Actions build to complete
2. Check build status (should be green checkmark)
3. Visit live site to verify changes
4. Test on mobile (responsive design)

## Security & Privacy

- No sensitive data in repository (public GitHub repo)
- No authentication/backend (static site)
- No form submissions (no server-side processing)
- External links use `target="_blank"` (see index.html:16-17)

## Design Philosophy

### Visual Style
- Minimalist, clean design
- Warm, inviting color palette (beige/cream tones)
- Serif typography (Georgia) for readability
- Monospace (Courier) for post titles (personality)
- Ample whitespace and breathing room

### User Experience
- Simple, intuitive navigation
- Fast loading (no JavaScript, minimal CSS)
- Mobile-responsive
- Accessible (semantic HTML)
- Focus on content readability

## References & Resources

- **Jekyll Docs**: https://jekyllrb.com/docs/
- **Liquid Templating**: https://shopify.github.io/liquid/
- **Markdown Guide**: https://www.markdownguide.org/
- **GitHub Pages**: https://docs.github.com/en/pages
- **User Guide**: See `HOWTO.md` in this repository

## Quick Reference Commands

### Local Development (Optional)
```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Build site
bundle exec jekyll build
```

### Git Operations
```bash
# Add new content
git add _posts/2025-11-14-new-post.md
git commit -m "Add new post: Title"
git push origin main

# Create feature branch
git checkout -b claude/feature-name
git push -u origin claude/feature-name
```

## Contact & Ownership

- **Owner**: Zachary (zevlo)
- **GitHub**: https://github.com/zevlo
- **Repository**: https://github.com/zevlo/zevlo.github.io

---

**Last Updated**: 2025-11-14
**Claude.md Version**: 1.0
**Maintained by**: AI assistants working with repository owner
