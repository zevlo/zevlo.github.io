### Adding Content

**Posts (posts.html):**
```html
<article class="post-item">
    <div class="post-date">Date</div>
    <div class="post-title">
        <a href="posts/your-post.html">Post Title</a>
    </div>
</article>
```

**Projects (projects.html):**
```html
<article class="project-item">
    <h2><a href="#">Project Name</a></h2>
    <p>Description</p>
    <div class="project-links">
        <a href="#" target="_blank">GitHub</a>
        <a href="#" target="_blank">Live Demo</a>
    </div>
</article>
```

**Thoughts (thoughts.html):**
```html
<article class="thought-item">
    <div class="thought-date">Date</div>
    <div class="thought-content">
        <p>Your thought or observation</p>
    </div>
</article>
```

### Customizing Colors

Edit `style.css` to change colors:
- Background: `background-color: #f5eed6;` (line 12)
- Text: `color: #2b2b2b;` (line 13)
- Links and borders can be adjusted throughout the file

## Adding Individual Blog Posts

Create a folder called `posts/` and add HTML files for each post:

1. Create `posts/` directory
2. Create a new HTML file for each post (e.g., `my-first-post.html`)
3. Use this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Post Title - Your Name's Blog</title>
    <link rel="stylesheet" href="../style.css">
</head>
<body>
    <header>
        <h1>Your Name's Blog</h1>
        <nav>
            <a href="../index.html">Home</a>
            <a href="../posts.html">Posts</a>
            <a href="../projects.html">Projects</a>
            <a href="../thoughts.html">Thoughts</a>
        </nav>
    </header>

    <main>
        <article>
            <h2>Your Post Title</h2>
            <p class="post-date">Date</p>
            
            <!-- Your content here -->
            <p>Your post content...</p>
        </article>
    </main>
</body>
</html>
```

4. Link to it from posts.html

## File Structure

```
zevlo.github.io/
├── index.html          # Home page
├── posts.html          # Blog posts listing
├── projects.html       # Projects showcase
├── thoughts.html       # Random thoughts/notes
├── style.css           # All styling
├── posts/             # Individual blog post files (create this)
│   └── post-1.html
└── README.md          # This file
```
