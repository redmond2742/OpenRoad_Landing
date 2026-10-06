# OpenRoad — Landing Site

Marketing and informational site for **OpenRoad**, an iOS app that turns everyday trips into
structured roadway data. Built with **Jekyll** and designed for **GitHub Pages**.

> Collect → Process → Review → Map → Export

## Run locally

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000>.

## Project structure

```
_config.yml          Site config, nav, and drop-in slots (see below)
_layouts/            default, page, post, home
_includes/           header, footer, logo, workflow, supported-data,
                     citizen-science, cta, icon, head-meta
_posts/              Blog articles (Markdown)
assets/css/main.scss Single processed stylesheet
assets/img/          favicon + a place to drop real images
index.html           Home
app.md               App
csv-builder.md       Asset CSV Builder
about.md             About
blog.html            Blog index
```

## Things to fill in later

All of these live in `_config.yml`, so you never touch the templates:

| Setting | What it does |
| --- | --- |
| `app_store_url` | Leave `""` to show a "Coming soon" button; set the App Store URL to make every CTA live. |
| `csv_builder_url` | Set to the external Asset CSV Builder web app URL. While it's `""` or `"#"`, the page shows a "coming soon" button. |
| `url` | Your production domain (used by SEO tags and the sitemap). |
| `twitter_username` / `github_username` | Optional, used by `jekyll-seo-tag`. |

### Swappable image assets

Real placeholder images live in `assets/img/` and are wired into the site through the
`images:` map in `_config.yml` and the `_includes/image.html` helper. There are **two ways
to swap any of them**:

1. **Replace the file** — drop your own image at the same path, keeping the filename
   (e.g. overwrite `assets/img/screen-process.webp` with a new screenshot). Nothing else to change.
2. **Repoint the config** — change the path in `_config.yml` to your new file. Setting a value
   to `""` hides that (optional) image entirely.

| Asset | File | Used on |
| --- | --- | --- |
| Home hero screenshot | `assets/img/hero-app.webp` | Home hero (`images.hero`) |
| App "Process" screen | `assets/img/screen-process.webp` | App page gallery (`images.app_process`) |
| App "Review" screen | `assets/img/screen-review.webp` | App page gallery (`images.app_review`) |
| App "Map" screen | `assets/img/screen-map.jpg` | App page gallery (`images.app_map`) |
| App "What it detects" screen | `assets/img/screen-detects.webp` | App page gallery (`images.app_detects`) |
| Standalone wordmark | `assets/img/logo.svg` | optional (`images.logo`) |
| Social / SEO preview | `assets/img/og-image.svg` | `og:image` via `image:` — replace with a **1200×630 PNG/JPG** for best support |
| Favicon | `assets/img/favicon.svg` | browser tab |

**Swapping in a different file type** (e.g. a `.png` screenshot): drop the new file in
`assets/img/` and update its path in `_config.yml` — the extension can differ from the old one.
The header/footer logo is still inline SVG (no file needed); the gallery images are real screenshots.

To place an image anywhere in a page:

```liquid
{% include image.html src="/assets/img/my-photo.png" alt="Description" caption="Optional caption" %}
```

## Deployment (GitHub Pages)

This is configured as a **user/org site** (`baseurl: ""`), served at your domain root.

- **User/org site:** push to the `main` branch of `USERNAME.github.io`. Enable Pages in repo settings.
- **Project site instead?** Set `baseurl: "/REPO_NAME"` in `_config.yml`. Every internal link already
  uses `relative_url`, so this one change is all that's needed.

Because the site uses only GitHub-Pages-safe plugins (`jekyll-feed`, `jekyll-seo-tag`,
`jekyll-sitemap`), it builds cleanly on GitHub Pages or via a GitHub Actions Jekyll workflow.
