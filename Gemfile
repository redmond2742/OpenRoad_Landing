source "https://rubygems.org"

gem "jekyll", "~> 4.3"

# Use the sassc backend (jekyll-sass-converter 2.x) instead of sass-embedded.
# sass-embedded downloads a native Dart Sass binary at install time, which
# fails on some CI builders (e.g. Cloudflare Pages). sassc compiles cleanly.
gem "jekyll-sass-converter", "~> 2.2"

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"
  gem "jekyll-seo-tag", "~> 2.8"
  gem "jekyll-sitemap", "~> 1.4"
end

# Ruby 3+ no longer ships webrick, which Jekyll's local server needs.
gem "webrick", "~> 1.8"

# Faster incremental rebuilds on macOS.
gem "jekyll-watch", "~> 2.2"
