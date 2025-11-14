# How to Write and Publish Content

Your site is now powered by Jekyll! This means you can write content in **Markdown** instead of HTML, and Jekyll will automatically convert it and update your site.

## Quick Start

### Writing a Blog Post

1. Create a new file in `_posts/` directory
2. Name it: `YYYY-MM-DD-title-slug.md` (e.g., `2025-11-14-my-first-post.md`)
3. Add frontmatter and content:

```markdown
---
layout: post
title: "Your Post Title"
date: 2025-11-14
---

Your content here in **markdown**!

## A Subheading

- List item 1
- List item 2

Write as much as you want!
```

4. Commit and push - that's it! Jekyll builds automatically on GitHub Pages.

### Publishing a Project

1. Create a new file in `_projects/` directory
2. Name it: `project-name.md` (e.g., `my-awesome-app.md`)
3. Add frontmatter and content:

```markdown
---
layout: post
title: "Project Name"
date: 2025-11-14
description: "Short description of the project"
github_url: "https://github.com/username/repo"  # Optional
demo_url: "https://your-demo.com"               # Optional
---

## About

Detailed description of your project...

### Technologies

- React
- Node.js
- MongoDB

### What I Learned

Share your insights...
```

4. Commit and push!

### Adding a Thought

1. Create a new file in `_thoughts/` directory
2. Name it: `YYYY-MM-DD-short-title.md` (e.g., `2025-11-14-interesting-idea.md`)
3. Add minimal frontmatter and content:

```markdown
---
date: 2025-11-14
---

Your quick thought, observation, or reflection goes here.

Keep it concise!
```

4. Commit and push!

## File Structure

```
zevlo.github.io/
├── _config.yml           # Jekyll configuration
├── _layouts/
│   ├── default.html      # Main layout with header/nav
│   └── post.html         # Layout for posts/projects/thoughts
├── _posts/               # Blog posts (markdown files)
│   └── YYYY-MM-DD-title.md
├── _projects/            # Projects (markdown files)
│   └── project-name.md
├── _thoughts/            # Thoughts (markdown files)
│   └── YYYY-MM-DD-title.md
├── index.html            # Home page
├── posts.html            # Auto-lists all posts
├── projects.html         # Auto-lists all projects
├── thoughts.html         # Auto-lists all thoughts
└── style.css             # Your design (unchanged!)
```

## Markdown Syntax Cheatsheet

### Headers
```markdown
# H1
## H2
### H3
```

### Text Formatting
```markdown
**Bold text**
*Italic text*
`Inline code`
```

### Links
```markdown
[Link text](https://url.com)
```

### Images
```markdown
![Alt text](path/to/image.jpg)
```

### Lists
```markdown
Unordered:
- Item 1
- Item 2

Ordered:
1. First
2. Second
```

### Code Blocks
````markdown
```python
def hello():
    print("Hello!")
```
````

### Quotes
```markdown
> This is a quote
```

## Publishing Workflow

1. **Write** your content in markdown
2. **Save** the file in the appropriate directory (_posts, _projects, or _thoughts)
3. **Commit** your changes:
   ```bash
   git add .
   git commit -m "Add new post: Your Title"
   ```
4. **Push** to GitHub:
   ```bash
   git push
   ```
5. **Wait** ~1-2 minutes for GitHub Pages to rebuild
6. **Visit** your site at https://zevlo.github.io

## Frontmatter Reference

### Posts
```yaml
---
layout: post          # Required
title: "Title"        # Required
date: YYYY-MM-DD      # Required
---
```

### Projects
```yaml
---
layout: post              # Required
title: "Project Name"     # Required
date: YYYY-MM-DD          # Required
description: "Short desc" # Optional (shown in listing)
github_url: "url"         # Optional
demo_url: "url"           # Optional
---
```

### Thoughts
```yaml
---
date: YYYY-MM-DD      # Required
---
```

## Tips

- **Filename format matters!** Posts and thoughts need `YYYY-MM-DD-` prefix
- **The date in frontmatter** determines the display order (newest first)
- **Write in markdown**, not HTML (but HTML works if needed)
- **Preview locally** (optional): Install Jekyll locally and run `bundle exec jekyll serve`
- **Your design is preserved** - Jekyll only handles the content conversion

## Common Issues

### Post not showing up?
- Check the filename format: `YYYY-MM-DD-title.md`
- Make sure frontmatter has `layout: post`
- Verify the date isn't in the future

### Formatting looks wrong?
- Make sure frontmatter is enclosed in `---`
- Check for YAML syntax errors (no tabs, proper spacing)

### Changes not visible?
- Wait 1-2 minutes for GitHub Pages to rebuild
- Check the Actions tab in GitHub for build status
- Clear your browser cache

## Need Help?

- [Markdown Guide](https://www.markdownguide.org/basic-syntax/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages + Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll)

---

Happy writing! ✍️
