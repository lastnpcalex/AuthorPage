# AUTHOR-NODE // Static Template

distributed consciousness interface for GitHub Pages

```
all boundaries are negotiations
all systems leak
```

---

## DEPLOYMENT PROTOCOL

### 1. Fork/Clone

```bash
git clone https://github.com/yourusername/author-node.git
cd author-node
```

### 2. Configure

Edit the `CONFIG` object in `index.html` (around line 380):

```javascript
const CONFIG = {
  author: {
    handle: 'YOUR_HANDLE',           // displayed in header
    name: 'Your Name',               // main title
    tagline: 'your ;; tagline ;; here',
    bio: `your bio text here.
can be multiline.`,
    avatar: '◬'                      // single character/emoji
  },
  links: [
    { 
      id: 'unique-id',
      label: 'LINK LABEL',           // uppercase recommended
      url: 'https://...',
      icon: '◈',                     // geometric symbols work well
      desc: 'description text'
    },
    // ... add more links
  ],
  posts: [
    {
      slug: 'url-friendly-slug',     // used in URL hash
      title: 'POST TITLE',
      date: '2025.03.14',            // format as you prefer
      excerpt: 'preview text...',
      tags: ['tag1', 'tag2'],
      file: 'posts/your-post.md'     // path to markdown file
    },
    // ... add more posts
  ]
};
```

### 3. Add Posts

Create markdown files in `/posts/` directory:

```
author-node/
├── index.html
├── README.md
└── posts/
    ├── your-first-post.md
    ├── another-post.md
    └── ...
```

### 4. Deploy to GitHub Pages

1. Push to GitHub
2. Go to Settings → Pages
3. Select branch (usually `main`) and root folder
4. Save

Your site will be live at `https://yourusername.github.io/author-node/`

---

## MARKDOWN FEATURES

The template supports standard markdown with styled output:

### Headers

```markdown
# H1 - Cyan glow, large
## H2 - Purple with left border
### H3 - Cyan, medium
```

### Text Formatting

```markdown
**bold** - cyan glow
*italic* - dimmed
`code` - green, monospace
```

### Code Blocks

~~~markdown
```
code blocks get
panel treatment
```
~~~

### Blockquotes

```markdown
> blockquotes have
> purple left border
```

### Lists

```markdown
- unordered items
- are cyan colored

1. ordered items
2. also work
```

### Links

```markdown
[link text](url) - cyan with purple underline
```

### Horizontal Rules

```markdown
---
gradient divider line
```

### Images

```markdown
![alt text](image.jpg)
purple border applied
```

---

## CUSTOMIZATION

### Colors

Edit CSS variables in `<style>`:

```css
:root {
  --cyan: #00ffff;
  --purple: #bf00ff;
  --magenta: #ff00ff;
  --green: #00ff88;
  --pink: #ff0099;
  --dark: #05050a;
  --panel: rgba(5, 5, 15, 0.92);
}
```

### Icons

Recommended geometric symbols for links:

```
◈ ◉ ◫ ⬡ ⎔ ◇ ◬ ⬢ ◎ ⬟ ◆ ▣ ⬡ ◐ ◑
```

### Disabling Effects

To reduce visual intensity, comment out in JavaScript:

```javascript
// initBinaryRain();      // disable binary rain
// initNetworkCanvas();   // disable network visualization  
// initGlitchEffect();    // disable glitch effect
```

---

## FILE STRUCTURE

```
author-node/
├── index.html          # main template (all CSS/JS inline)
├── README.md           # this file
└── posts/              # markdown content
    ├── post-one.md
    ├── post-two.md
    └── ...
```

All assets are inline or loaded from CDN. No build step required.

---

## URL ROUTING

The template uses hash-based routing:

- `yoursite.com/` - index view
- `yoursite.com/#post/slug-name` - post view

Direct links to posts work and are shareable.

---

## DEPENDENCIES

Loaded from CDN (no installation needed):

- [Marked.js](https://marked.js.org/) - markdown parsing
- [Google Fonts](https://fonts.google.com/) - Orbitron, Share Tech Mono, Space Mono, VT323

---

## LOCAL DEVELOPMENT

For local testing, you need a server (due to fetch() for .md files):

```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve

# PHP
php -S localhost:8000
```

Then open `http://localhost:8000`

---

## LICENSE

MIT // do what you want // credit appreciated but not required

---

```
signal ends
noise continues
```

*template by void_prophet // 2025*
