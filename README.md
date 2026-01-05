# My Zola Blog

A static blog built with [Zola](https://www.getzola.org/) and automatically deployed using GitHub Actions.

## Features

- **Fast static site generation** with Zola
- **Automatic deployment** to GitHub Pages on push to main
- **PR previews** - Review HTML output before merging
- **Clean, responsive design**
- **Syntax highlighting** for code blocks
- **Tag and category support**

## Local Development

### Prerequisites

Install Zola:
- **macOS**: `brew install zola`
- **Linux**: Download from [GitHub releases](https://github.com/getzola/zola/releases)
- **Windows**: `choco install zola` or `scoop install zola`

### Running locally

```bash
# Clone the repository
git clone https://github.com/kain88-de/Pages.git
cd Pages

# Serve the site locally
zola serve

# Build the site
zola build
```

The site will be available at `http://127.0.0.1:1111`

## Writing Posts

Create a new post in `content/blog/`:

```markdown
+++
title = "My New Post"
date = 2026-01-05
description = "A short description"
[taxonomies]
tags = ["tag1", "tag2"]
categories = ["category"]
+++

# Your content here

Write your post content in Markdown.
```

## GitHub Actions Workflows

### Deploy to GitHub Pages

- **Trigger**: Push to `main` branch
- **Action**: Builds the site and deploys to GitHub Pages
- **URL**: https://kain88-de.github.io/Pages

### PR Preview

- **Trigger**: Pull request opened/updated
- **Action**: Builds the site and uploads HTML as an artifact
- **Review**: Download the artifact from the workflow run to review the HTML output

## Project Structure

```
.
├── config.toml          # Site configuration
├── content/             # Markdown content
│   ├── _index.md       # Homepage content
│   └── blog/           # Blog posts
├── templates/          # HTML templates
│   ├── base.html      # Base template
│   ├── index.html     # Homepage template
│   ├── page.html      # Single page template
│   └── section.html   # Section/list template
├── static/            # Static assets (CSS, images, etc.)
└── .github/
    └── workflows/     # GitHub Actions workflows
```

## License

See [LICENSE](LICENSE) file.
