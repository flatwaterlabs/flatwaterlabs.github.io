# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview
Flatwater Labs is a modern data science and machine learning consultancy focused on rowing analytics. The static website is built with Jekyll 4.4.1 and uses a simplified version of the Airspace Jekyll theme, customized for the rowing analytics space.

## Commands

### Development
```bash
# Install dependencies
bundle install

# Build and serve the site locally (default: http://localhost:4000)
bundle exec jekyll serve

# Build site to _site/ directory (production)
bundle exec jekyll build

# Build with live reload for development
bundle exec jekyll serve --livereload
```

### Common Jekyll Options
- `--drafts` - Include draft posts in `_drafts/` directory
- `--watch` - Watch for file changes and rebuild automatically (enabled by default with `serve`)
- `--baseurl ''` - Override baseurl from `_config.yml`

## Architecture

### Jekyll Site Structure
This is a standard Jekyll static site with the following architecture:

**Layouts** (`_layouts/`):
- `default.html` - Base layout with head, header, content, and footer includes
- `page.html` - Wraps content in default layout (used for static pages)
- `post.html` - Blog post layout with title, author, date, and back-to-blog link

**Includes** (`_includes/`):
- `head.html` - Meta tags, CSS/JS includes, theme metadata
- `header.html` - Navigation bar with logo and menu links
- `footer.html` - Footer with navigation and copyright

**Content**:
- `index.html` - Homepage with hero, about, and services sections
- `contact.html` - Contact page with form
- `_posts/` - Blog posts directory (for future use)

**Data** (`_data/`):
- `funfacts.yml` - Statistics for homepage (currently commented out)
- `testimonials.yml` - Testimonials (currently commented out)

**Assets**:
- `css/` - Stylesheets (Bootstrap, FontAwesome, Ionicons, custom)
- `js/` - JavaScript libraries and custom scripts
- `img/` - Images and graphics
- `fonts/` - Web fonts

### Configuration
Site settings are in `_config.yml`:
- Title: "Flatwater Labs"
- Subtitle: "Rowing Data Science & Analytics"
- URL: https://flatwaterlabs.com
- Markdown renderer: kramdown
- Excluded files: vendor, Gemfile, README, LICENSE, gemspecs

### Theme Customization
The site uses a heavily customized version of the Airspace theme:
- CSS files in `css/` can be edited directly
- Main custom styles in `css/style.css` and `css/airspace.css`
- JavaScript customizations in `js/main.js`

### Adding Content

**Update homepage**:
- Edit `index.html` directly to modify hero text, about section, or services
- Update `_data/funfacts.yml` to add statistics (uncomment and customize)
- Update `_data/testimonials.yml` to add client testimonials (uncomment and customize)

**Update contact page**:
- Edit `contact.html` to modify form or contact information

## Notes
- The site is Git-tracked; built files in `_site/` are included in the repository
- Theme originally designed by ThemeFisher, ported to Jekyll by Andrew Lee
- Uses jQuery 1.10.2, Bootstrap, Owl Carousel for UI components
