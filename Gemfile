# Local development for the andybateman.com site.
#
# GitHub Pages builds and deploys the live site itself (server-side), so this
# Gemfile is for building, serving and linting locally. We use modern Jekyll
# rather than the legacy `github-pages` gem, which pins a very old Jekyll that
# no longer runs on current Ruby. Output is equivalent for this site; the
# enabled plugins are declared in _config.yml.
#
# Needs Ruby 3.x+. On this Mac the Homebrew Ruby works; put it on PATH first:
#   export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
#   bundle install
#   bundle exec jekyll serve            # http://localhost:4000
#   bundle exec jekyll build            # outputs to _site/
#
source "https://rubygems.org"

gem "jekyll", "~> 4.3"

# liquid 4.0.3 calls String#tainted? (removed in Ruby 3.2+); 4.0.4 fixed it.
gem "liquid", "~> 4.0.4"

group :jekyll_plugins do
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
  gem "jekyll-redirect-from"
end

# Required to `jekyll serve` on Ruby 3.0+ (webrick is no longer bundled).
gem "webrick", "~> 1.8"

# Linting: checks built HTML for broken internal links, images and anchors.
#   bundle exec htmlproofer _site --disable-external --no-enforce-https
gem "html-proofer", group: :development

# Standard-library gems unbundled in Ruby 3.4 / 4.0.
gem "csv"
gem "base64"
gem "bigdecimal"
gem "logger"
