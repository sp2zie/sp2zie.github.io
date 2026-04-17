# AGENTS.md - Guidelines for AI Coding Agents

This is a Jekyll-based static website for the amateur radio club SP2ZIE "Szkuner" in Gdynia, Poland.

## Build Commands

```bash
# Install dependencies
bundle install

# Build the site (development)
bundle exec jekyll build

# Serve locally with auto-regeneration
bundle exec jekyll serve

# Build for production (GitHub Pages)
JEKYLL_ENV=production bundle exec jekyll build
```

## Test Commands

No test suite is configured for this project. The site is tested manually and through GitHub Pages deployment.

## Lint Commands

No linting tools are currently configured. HTML/CSS/JS validation should be done manually or via browser dev tools.

## Project Structure

- `_config.yml` - Jekyll configuration
- `_layouts/` - HTML templates (Liquid)
- `_includes/` - Reusable HTML components
- `_posts/` - Blog posts in Markdown with YAML front matter
- `assets/` - Static assets (images, CSS, JS)
- `_site/` - Generated output (gitignored)

## Code Style Guidelines

### HTML/Liquid Templates
- Use 4-space indentation
- Include Bootstrap components via CDN (Bootstrap 5.3.8)
- Use semantic HTML5 elements
- Polish language content
- Escape dynamic content: `{{ variable | escape }}`
- Use includes for reusable components: `{% include filename.html %}`

### CSS
- Inline styles in `<style>` tags within layouts
- Bootstrap classes preferred for layout
- Custom CSS for club branding colors:
  - `--sp-blue: #0a78b8`
  - `--sp-yellow: #f4c400`

### Markdown Content
- YAML front matter required with `layout`, `title`, and optional `author`
- Use Polish language for all content
- Posts use date prefix: `YYYY-MM-DD-title-slug.md`
- Use Bootstrap classes in HTML within markdown

### File Naming
- Lowercase with hyphens: `my-file-name.md`
- Polish characters allowed in content but avoid in filenames
- Images: descriptive names, lowercase, hyphens

### Git Workflow
- Main branch: `main`
- GitHub Actions auto-deploys on push to main
- No pre-commit hooks configured

## Dependencies

- Ruby 3.4.8 (see `.ruby-version`)
- Jekyll (latest via Gemfile)
- Bootstrap 5.3.8 (CDN)
- Bootstrap Icons 1.11.3 (CDN)

## Deployment

Automatic deployment via GitHub Actions to GitHub Pages on every push to `main` branch.

## Notes

- This is a content-focused site with minimal interactivity
- Search functionality implemented client-side via JavaScript
- Site uses Polish language exclusively
- Club specializes in satellite communications and maritime radio
