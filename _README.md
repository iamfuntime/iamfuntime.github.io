# Personal Cybersecurity Professional Website

A modern, professional website built with Hugo static site generator for GitHub Pages hosting. Features a clean design optimized for cybersecurity professionals with easy content management through Markdown files.

## 🚀 Quick Start

### Prerequisites
- [Hugo Extended](https://gohugo.io/installation/) v0.120+ 
- [Git](https://git-scm.com/downloads)
- [Node.js](https://nodejs.org/) (optional, for advanced customization)

### Local Development
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/yourusername.github.io.git
   cd yourusername.github.io
   ```

2. Start the Hugo development server:
   ```bash
   hugo server -D
   ```

3. Open your browser to `http://localhost:1313`

### Deploy to GitHub Pages
1. Push changes to the `main` branch
2. GitHub Actions will automatically build and deploy your site
3. Your site will be available at `https://yourusername.github.io`

## 📁 Project Structure

```
/
├── content/                 # All your content (Markdown files)
│   ├── _index.md           # Homepage content
│   ├── resume.md           # Resume page
│   └── blog/               # Blog posts
│       ├── _index.md       # Blog section page
│       └── *.md            # Individual blog posts
├── layouts/                # HTML templates
│   ├── _default/           # Default page templates
│   ├── partials/           # Reusable template components
│   └── index.html          # Homepage template
├── static/                 # Static assets
│   ├── css/style.css       # Main stylesheet
│   └── js/main.js          # JavaScript functionality
├── hugo.toml               # Hugo configuration
└── README.md               # This file
```

## ✏️ Content Management

### Updating Personal Information

#### Site Configuration
Edit `hugo.toml` to update:
- Site title and description
- Your name
- Contact information in the footer

#### About Me Page
Edit `content/_index.md` and `layouts/index.html` to update:
- Personal information
- Areas of expertise
- Recent highlights
- Skills sections

#### Resume Page
Edit `content/resume.md` to update:
- Professional experience
- Education
- Certifications
- Publications and speaking

### Adding Blog Posts

#### Creating a New Blog Post
1. Create a new Markdown file in `content/blog/`:
   ```bash
   hugo new blog/your-post-title.md
   ```

2. Edit the file with your content:
   ```markdown
   ---
   title: "Your Post Title"
   date: 2024-01-15
   description: "Brief description for SEO and previews"
   tags: ["security", "leadership", "cloud"]
   readingTime: 5
   ---

   # Your Post Title

   Your content here...
   ```

#### Front Matter Options
- `title`: Post title (required)
- `date`: Publication date (required)
- `description`: SEO description and preview text
- `tags`: Array of tags for categorization
- `readingTime`: Estimated reading time in minutes
- `draft`: Set to `true` to hide from production

#### Writing Tips
- Use descriptive headings (H2, H3) for better structure
- Include code examples in fenced code blocks
- Add relevant tags for categorization
- Keep paragraphs concise for web readability

## 🎨 Customization

### Colors and Branding
Edit the CSS custom properties in `static/css/style.css`:

```css
:root {
  --color-primary: #1a2332;        /* Main brand color */
  --color-secondary: #2563eb;      /* Accent color */
  --color-accent: #10b981;         /* Success/highlight color */
  /* ... more colors ... */
}
```

### Typography
The site uses Inter for body text and JetBrains Mono for code. To change fonts, update the Google Fonts link in `layouts/_default/baseof.html` and the CSS variables in `style.css`.

### Layout Modifications
- **Header/Navigation**: Edit `layouts/partials/header.html`
- **Footer**: Edit `layouts/partials/footer.html`
- **Homepage**: Edit `layouts/index.html`
- **Blog Layout**: Edit `layouts/blog/list.html`

## 🔧 GitHub Pages Setup

### Repository Configuration
1. Create a repository named `yourusername.github.io`
2. Go to Settings > Pages
3. Set Source to "GitHub Actions"

### GitHub Actions Workflow
Create `.github/workflows/hugo.yml`:

```yaml
name: Deploy Hugo site to Pages

on:
  push:
    branches: ["main"]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

defaults:
  run:
    shell: bash

jobs:
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.120.4
    steps:
      - name: Install Hugo CLI
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb
          sudo dpkg -i ${{ runner.temp }}/hugo.deb
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v4
      - name: Build with Hugo
        env:
          HUGO_ENVIRONMENT: production
          HUGO_ENV: production
        run: |
          hugo \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v2
        with:
          path: ./public

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v3
```

## 📝 Content Writing Guidelines

### Blog Post Structure
1. **Hook**: Start with an engaging opening
2. **Context**: Provide background and why this matters
3. **Main Content**: Break into digestible sections with clear headings
4. **Actionable Advice**: Include practical takeaways
5. **Conclusion**: Summarize key points and encourage engagement

### SEO Best Practices
- Use descriptive titles (50-60 characters)
- Write compelling meta descriptions (150-160 characters)
- Include relevant keywords naturally
- Use proper heading hierarchy (H1 > H2 > H3)
- Add internal and external links

### Professional Tone
- Write in first person when sharing experiences
- Use active voice
- Keep sentences concise
- Explain technical concepts for broader audience
- Include real-world examples and lessons learned

## 🛠️ Advanced Features

### Analytics (Optional)
Add Google Analytics or privacy-focused alternatives by editing `layouts/_default/baseof.html`.

### Search Functionality
Consider adding search with:
- Fuse.js for client-side search
- Algolia for advanced search features
- Simple site search with grep-like functionality

### Comments System
Add comments using:
- Disqus (traditional)
- Utterances (GitHub-based)
- Giscus (GitHub Discussions-based)

## 🚨 Security Considerations

### Content Security
- Never commit sensitive information
- Use environment variables for API keys
- Review all content before publishing
- Keep dependencies updated

### GitHub Security
- Enable two-factor authentication
- Use branch protection rules
- Review workflow permissions
- Monitor security advisories

## 📱 Mobile Optimization

The site is fully responsive and optimized for mobile devices:
- Touch-friendly navigation
- Readable typography on small screens
- Fast loading times
- Progressive enhancement

## 🔍 SEO Features

- Semantic HTML structure
- Open Graph meta tags
- Twitter Card support
- Structured data markup
- RSS feed generation
- Sitemap generation
- Fast loading speeds

## 🆘 Troubleshooting

### Common Issues

#### Hugo Build Errors
- Check Hugo version (requires Extended v0.120+)
- Verify file paths and naming conventions
- Check front matter syntax

#### GitHub Pages Deployment Issues
- Ensure repository name matches `yourusername.github.io`
- Check GitHub Actions workflow logs
- Verify Pages settings in repository

#### Content Not Appearing
- Check file location and naming
- Verify front matter format
- Ensure `draft: false` or remove draft parameter

### Getting Help
- [Hugo Documentation](https://gohugo.io/documentation/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Hugo Community Forum](https://discourse.gohugo.io/)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🤝 Contributing

If you find issues or have suggestions for improvements, please:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

---

*Built with [Hugo](https://gohugo.io/) and deployed on [GitHub Pages](https://pages.github.com/)*