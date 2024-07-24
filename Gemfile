source "https://rubygems.org"

# restrain version of github pages to avoid bugs
gem "github-pages", "=228", group: :jekyll_plugins

# in git ignore, since this is your local project, comment Gemfile.lock
# so that github-pages CI does not crash due to increasing versions of stuff
# reference: https://stackoverflow.com/questions/4151495/should-gemfile-lock-be-included-in-gitignore

gem "tzinfo-data"
gem "wdm", "~> 0.1.0" if Gem.win_platform?

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "webrick"
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-feed"
  gem "jemoji"
  gem "jekyll-include-cache"
  gem "jekyll-algolia"
end
