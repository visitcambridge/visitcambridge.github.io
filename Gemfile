source "https://rubygems.org"

# Specify Ruby version
ruby "3.3.5"

# Jekyll
gem "jekyll", "~> 4.3.2"

# Theme
gem "minima", "~> 2.5"

# Plugins
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.15"
  gem "jekyll-haml-markup", "~> 0.1.5"
  gem "jekyll-sitemap", "~> 1.4"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :install_if => Gem.win_platform?

# Add these lines to ensure compatibility
gem "ffi", "~> 1.17.0"
gem "sassc", "~> 2.4.0"

gem "webrick", "~> 1.8"
gem "base64", "~> 0.2.0"
gem "bigdecimal", "~> 3.1.4"
gem "csv", "~> 3.2.7"
gem "logger", "~> 1.6.0"