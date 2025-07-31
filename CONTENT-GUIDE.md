# Content Management Guide

This guide provides detailed instructions for updating and maintaining your cybersecurity professional website.

## 📋 Quick Reference

### Common Tasks
- **Add a blog post**: Create new `.md` file in `content/blog/`
- **Update resume**: Edit `content/resume.md`
- **Change personal info**: Edit `hugo.toml` and `content/_index.md`
- **Modify navigation**: Edit `hugo.toml` menu section

### File Locations
- **Homepage content**: `content/_index.md` and `layouts/index.html`  
- **Resume**: `content/resume.md`
- **Blog posts**: `content/blog/*.md`
- **Site config**: `hugo.toml`
- **Styling**: `static/css/style.css`

## ✍️ Writing Blog Posts

### Step 1: Create the File
Create a new Markdown file in the `content/blog/` directory:

```bash
# Example filename: content/blog/incident-response-best-practices.md
```

### Step 2: Add Front Matter
Start your blog post with YAML front matter:

```yaml
---
title: "Incident Response Best Practices: Lessons from 100+ Breaches"
date: 2024-01-30
description: "Essential incident response strategies learned from managing cybersecurity incidents across multiple industries"
tags: ["incident-response", "security", "best-practices", "leadership"]
readingTime: 6
---
```

#### Front Matter Fields Explained
- `title`: The blog post title (required)
- `date`: Publication date in YYYY-MM-DD format (required)
- `description`: Brief summary for SEO and social sharing (recommended)
- `tags`: Array of relevant tags for categorization (optional)
- `readingTime`: Estimated reading time in minutes (optional)
- `draft`: Set to `true` to hide from production (optional)

### Step 3: Write Your Content
Use standard Markdown syntax:

```markdown
# Main Heading (H1)

Your introduction paragraph here...

## Section Heading (H2)

Content with **bold text** and *italic text*.

### Subsection (H3)

- Bullet point one
- Bullet point two
- Bullet point three

#### Technical Details (H4)

Code example:
```bash
# Example command
sudo nmap -sS -O target.com
```
```

### Step 4: Preview and Publish
1. Run `hugo server -D` to preview locally
2. Remove `draft: true` from front matter when ready
3. Commit and push to publish

## 🏷️ Tagging Strategy

Use consistent tags to help readers find related content:

### Primary Categories
- `security` - General cybersecurity topics
- `leadership` - Team management and leadership
- `architecture` - Security architecture and design
- `incident-response` - Incident handling and forensics
- `risk-management` - Risk assessment and GRC
- `compliance` - Regulatory and compliance topics

### Technology Tags
- `cloud` - Cloud security topics
- `aws` / `azure` / `gcp` - Cloud platform specific
- `zero-trust` - Zero Trust architecture
- `automation` - Security automation and tools

### Format Tags
- `case-study` - Real-world examples
- `tutorial` - How-to guides
- `lessons-learned` - Experience-based insights
- `best-practices` - Recommended approaches

## 📄 Updating Your Resume

Edit `content/resume.md` using standard Markdown:

### Adding New Experience
```markdown
### New Job Title
**Company Name** | *Start Date - End Date*

- Achievement or responsibility one
- Achievement or responsibility two
- Key metrics or results

**Key Achievements:**
- Specific accomplishment with measurable impact
- Another significant result
```

### Adding Certifications
```markdown
- **CISSP** - Certified Information Systems Security Professional *(Year)*
- **CISM** - Certified Information Security Manager *(Year)*
```

### Adding Publications
```markdown
### Publications
- **"Article Title"** - *Publication Name*, Year
- **"Another Article"** - *Another Publication*, Year
```

## 🎨 Customizing Appearance

### Changing Colors
Edit CSS custom properties in `static/css/style.css`:

```css
:root {
  --color-primary: #1a2332;      /* Main dark blue */
  --color-secondary: #2563eb;    /* Accent blue */
  --color-accent: #10b981;       /* Green for highlights */
}
```

### Updating Personal Information
Edit `hugo.toml`:

```toml
title = 'Your Name - Cybersecurity Professional'

[params]
  description = "Personal website description"
  author = "Your Full Name"
```

### Modifying Navigation
Edit the menu section in `hugo.toml`:

```toml
[menu]
  [[menu.main]]
    name = "About"
    url = "/"
    weight = 1
  [[menu.main]]
    name = "Resume"
    url = "/resume/"
    weight = 2
```

## 📱 Content Best Practices

### Writing Style
- **Be conversational**: Write like you're talking to a colleague
- **Use active voice**: "I implemented" vs "was implemented"
- **Include examples**: Real-world scenarios resonate with readers
- **Keep paragraphs short**: 2-4 sentences for web readability

### Professional Tone
- Share experiences without revealing confidential information
- Focus on lessons learned rather than specific client details
- Use "we" when discussing team accomplishments
- Be humble about successes, honest about failures

### SEO Optimization
- Include target keywords naturally in titles and headings
- Write descriptive meta descriptions (150-160 characters)
- Use internal links to connect related posts
- Include relevant external links to authoritative sources

### Technical Content
- Explain acronyms on first use
- Provide context for technical concepts
- Include practical takeaways
- Use code blocks for commands and examples

## 🖼️ Adding Images

### Image Storage
Place images in `static/images/` directory:
```
static/
└── images/
    ├── blog/
    │   └── post-name/
    │       └── diagram.png
    └── profile.jpg
```

### Including Images in Posts
```markdown
![Alt text](/images/blog/post-name/diagram.png)
```

### Image Optimization Tips
- Use WebP format when possible
- Compress images before uploading
- Include descriptive alt text for accessibility
- Keep file sizes under 500KB for web performance

## 🔍 SEO Checklist

### For Each Blog Post
- [ ] Descriptive, keyword-rich title (50-60 characters)
- [ ] Compelling meta description (150-160 characters)
- [ ] Relevant tags and categories
- [ ] Internal links to related posts
- [ ] External links to authoritative sources
- [ ] Proper heading structure (H1 > H2 > H3)
- [ ] Alt text for all images

### Site-Wide SEO
- [ ] Updated sitemap (auto-generated by Hugo)
- [ ] RSS feed (auto-generated)
- [ ] Social media meta tags (included in templates)
- [ ] Fast loading times (optimized CSS/JS)

## 📊 Content Calendar Ideas

### Monthly Topics
- **January**: Year-end security reviews, predictions
- **February**: Love for security awareness, team building
- **March**: Spring cleaning for security policies
- **April**: Tax season phishing awareness
- **May**: Mental health in cybersecurity
- **June**: Conference season insights
- **July**: Summer intern security training
- **August**: Back-to-school security for education
- **September**: Cybersecurity Awareness Month prep
- **October**: Halloween security horror stories
- **November**: Thanksgiving for security community
- **December**: Holiday security tips, year-end wrap-up

### Content Types to Rotate
- **Case studies**: Real-world problem-solving examples
- **Tutorials**: Step-by-step how-to guides
- **Industry analysis**: Commentary on security trends
- **Leadership insights**: Team building and management
- **Technical deep dives**: Advanced security concepts
- **Book/tool reviews**: Recommendations for the community

## 🚀 Publishing Workflow

### Pre-Publication Checklist
1. **Content review**: Grammar, spelling, accuracy
2. **Technical review**: Verify all commands and examples
3. **Legal review**: Ensure no confidential information
4. **SEO check**: Title, description, tags optimized
5. **Preview**: Test on mobile and desktop

### Publication Process
1. Create branch for new post (optional but recommended)
2. Write and review content
3. Test locally with `hugo server -D`
4. Remove `draft: true` from front matter
5. Commit and push to main branch
6. Verify deployment on live site

### Post-Publication
- Share on LinkedIn and other professional networks
- Engage with comments and feedback
- Update internal links in future posts
- Monitor analytics for performance insights

## 🛠️ Troubleshooting

### Common Issues

#### Post Not Appearing
- Check file is in `content/blog/` directory
- Verify front matter is valid YAML
- Ensure `draft: false` or remove draft parameter
- Check date isn't in the future

#### Formatting Issues
- Validate Markdown syntax
- Check for unclosed code blocks
- Verify heading hierarchy (don't skip levels)
- Test with different devices/browsers

#### Build Errors
- Check Hugo version (`hugo version`)
- Validate YAML front matter syntax
- Look for special characters in filenames
- Review error messages in terminal

### Getting Help
- Hugo documentation: https://gohugo.io/documentation/
- Markdown guide: https://www.markdownguide.org/
- GitHub support: https://support.github.com/

---

*Remember: Great content takes time. Focus on providing value to your readers rather than publishing frequently. Quality over quantity always wins in professional blogging.*