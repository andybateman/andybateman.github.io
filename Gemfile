# Local development for the andybateman.com GitHub Pages site.
#
# GitHub Pages builds and deploys the live site itself; this Gemfile just
# lets you build, serve and lint locally with the same pinned versions GitHub
# Pages uses, so problems show up before you push.
#
#   bundle install
#   bundle exec jekyll serve            # http://localhost:4000
#   bundle exec jekyll build            # outputs to _site/
#
source "https://rubygems.org"

# The github-pages gem pins Jekyll and all supported plugins (jekyll-seo-tag,
# jekyll-sitemap, jekyll-redirect-from, ...) to match the GitHub Pages build.
gem "github-pages", group: :jekyll_plugins

# Required to `jekyll serve` on Ruby 3.0+ (webrick is no longer bundled).
gem "webrick", "~> 1.8"
